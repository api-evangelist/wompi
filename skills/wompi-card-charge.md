---
name: Charge a card end-to-end
description: Tokenize a card and create a COP card transaction with Wompi, then poll to a final status.
api: openapi/wompi-openapi.yml
operations: [getMerchant, tokenizeCard, createTransaction, getTransaction]
---

# Charge a card with Wompi

Grounded in real operationIds from `openapi/wompi-openapi.yml`. Amounts are integer COP cents (`amount_in_cents`). Use test keys (`pub_test_`/`prv_test_`) against `https://sandbox.wompi.co/v1` first — see `sandbox/wompi-sandbox.yml`.

## Steps

1. **Get the acceptance token** — `getMerchant` (`GET /merchants/{public_key}`) with the PUBLIC key as Bearer. Read `data.presigned_acceptance.acceptance_token`.
2. **Tokenize the card** — `tokenizeCard` (`POST /tokens/cards`) with the PUBLIC key (browser-safe). Body: `number`, `cvc`, `exp_month`, `exp_year`, `card_holder`. Read the token id (`tok_...`). In sandbox, `4242424242424242` → APPROVED, `4111111111111111` → DECLINED.
3. **Compute the integrity signature** — SHA256 of `reference + amount_in_cents + currency + integrity_secret` (the *firma de integridad*). See `conventions/wompi-conventions.yml`.
4. **Create the transaction** — `createTransaction` (`POST /transactions`) with the PUBLIC key. Body: `amount_in_cents`, `currency: COP`, `customer_email`, a unique `reference`, the `acceptance_token`, the `signature`, and `payment_method: { type: CARD, token: tok_..., installments }`. It returns status `PENDING`.
5. **Poll for the result** — `getTransaction` (`GET /transactions/{id}`) until `data.status` is final: `APPROVED`, `DECLINED`, `VOIDED`, or `ERROR`. Prefer the `transaction.updated` webhook (see `asyncapi/wompi-webhooks.yml`) over tight polling.

## Rules
- `reference` must be unique per payment; it is a dedup identifier, not a retry-safe idempotency key (`conventions/wompi-conventions.yml`).
- A decline is HTTP 201 with `status: DECLINED` + `status_message`, not an API error (`errors/wompi-decline-codes.yml`).
- Validation failures return 422 with an `error` envelope (`errors/wompi-problem-types.yml`).
