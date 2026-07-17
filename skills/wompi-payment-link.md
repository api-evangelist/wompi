---
name: Create and track a payment link
description: Create a hosted Wompi payment link for a fixed or open amount and retrieve it.
api: openapi/wompi-openapi.yml
operations: [createPaymentLink, getPaymentLink]
---

# Create and track a Wompi payment link

Grounded in real operationIds from `openapi/wompi-openapi.yml`. Payment links are a no-code hosted checkout at `checkout.wompi.co/l/...`.

## Steps

1. **Create the link** — `createPaymentLink` (`POST /payment_links`) with the PRIVATE key. Body: `name`, `description`, `single_use` (bool), `currency: COP`, `amount_in_cents` (omit for an open amount), optional `collect_shipping`. Read `data.id` and `data.url`.
2. **Share the URL** — send `data.url` (e.g. `https://checkout.wompi.co/l/abc123XYZ`) to the buyer.
3. **Retrieve / track** — `getPaymentLink` (`GET /payment_links/{id}`, PRIVATE key). Resulting payments arrive as normal transactions; listen for the `transaction.updated` webhook (`asyncapi/wompi-webhooks.yml`) to reconcile.

## Rules
- Requires the PRIVATE key (`prv_...`), server-side only.
- Amounts are integer COP cents (`amount_in_cents`); no decimals (`conventions/wompi-conventions.yml`).
- Prefer the Widget or Web Checkout components (`components/wompi-components.yml`) when embedding checkout in your own page instead of sharing a link.
