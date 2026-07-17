---
name: Store a payment source and charge it
description: Turn a card token into a reusable Wompi payment source and charge it server-side later.
api: openapi/wompi-openapi.yml
operations: [tokenizeCard, createPaymentSource, createTransaction, getTransaction]
---

# Store a payment source and charge it later

Grounded in real operationIds from `openapi/wompi-openapi.yml`. Use this for recurring / merchant-initiated charges where the customer is not re-entering card data.

## Steps

1. **Tokenize the card** — `tokenizeCard` (`POST /tokens/cards`, PUBLIC key). Read the `tok_...` id.
2. **Get an acceptance token** — from `getMerchant` (`GET /merchants/{public_key}`) as in the card-charge skill.
3. **Create the payment source** — `createPaymentSource` (`POST /payment_sources`) with the PRIVATE key. Body: `type: CARD` (or `NEQUI`), `token`, `customer_email`, `acceptance_token`. Read `data.id` (integer) and `data.status` (`AVAILABLE`).
4. **Charge the source** — `createTransaction` (`POST /transactions`) passing `payment_source_id` instead of an inline `payment_method`, plus `amount_in_cents`, `currency: COP`, a unique `reference`, and the integrity `signature`.
5. **Confirm** — `getTransaction` (`GET /transactions/{id}`) or the `transaction.updated` webhook to a final status.

## Rules
- Payment sources require the PRIVATE key (`prv_...`) — server-side only (`authentication/wompi-authentication.yml`).
- Each charge still needs a unique `reference` and a fresh integrity signature (`conventions/wompi-conventions.yml`).
- For a Nequi source, tokenize with `tokenizeNequi` and poll `getNequiToken` to `APPROVED` before creating the source.
