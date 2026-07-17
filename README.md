# Wompi (wompi)

Wompi is the payment gateway of Grupo Bancolombia, serving Colombia (COP). Its REST API creates and tracks transactions across local payment methods — CARD, NEQUI (mobile wallet), PSE (online bank debit), and Bancolombia Transfer / Collect — plus card and Nequi tokenization, reusable payment sources, and hosted payment links. Public-key endpoints are browser-safe; private-key endpoints are server-side.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/wompi/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/wompi/refs/heads/main/apis.yml)

## Tags

- Payments
- Fintech
- Colombia
- LatAm
- Payment Gateway
- PSE
- Nequi

## Timestamps

- **Created:** 2026-07-17
- **Modified:** 2026-07-17

## APIs

### Wompi Transactions API

Creates and tracks payment transactions in COP across CARD, NEQUI, PSE, and Bancolombia Transfer/Collect methods. Transactions require an acceptance token and integrity signature; they start PENDING and settle to APPROVED, DECLINED, VOIDED, or ERROR.

- **Human URL:** [https://docs.wompi.co/en/docs/colombia/transacciones/](https://docs.wompi.co/en/docs/colombia/transacciones/)
- **Base URL:** `https://production.wompi.co/v1`

#### Tags

- Payments
- Transactions
- Checkout

#### Properties

- [Documentation](https://docs.wompi.co/en/docs/colombia/transacciones/)
- [API Reference](https://docs.wompi.co/en/docs/colombia/inicia-una-transaccion-desde-cero/)
- [OpenAPI](openapi/wompi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wompi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Wompi Tokenization API

Exchanges raw card data for single-use card tokens (public-key, browser-safe) and enrolls Nequi accounts for tokenized charging, with status polling for in-app approval.

- **Human URL:** [https://docs.wompi.co/en/docs/colombia/fuentes-de-pago/](https://docs.wompi.co/en/docs/colombia/fuentes-de-pago/)
- **Base URL:** `https://production.wompi.co/v1`

#### Tags

- Tokenization
- Cards
- Nequi

#### Properties

- [Documentation](https://docs.wompi.co/en/docs/colombia/fuentes-de-pago/)
- [OpenAPI](openapi/wompi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wompi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Wompi Payment Sources API

Stores a card or approved Nequi token as a reusable payment source so a customer can be charged later without re-entering data. Requires the private key and a presigned acceptance token.

- **Human URL:** [https://docs.wompi.co/en/docs/colombia/fuentes-de-pago/](https://docs.wompi.co/en/docs/colombia/fuentes-de-pago/)
- **Base URL:** `https://production.wompi.co/v1`

#### Tags

- Payment Sources
- Recurring
- Subscriptions

#### Properties

- [Documentation](https://docs.wompi.co/en/docs/colombia/fuentes-de-pago/)
- [OpenAPI](openapi/wompi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wompi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Wompi PSE API

Returns the PSE (Pagos Seguros en Línea / online bank debit) financial institution catalog that customers pick from when paying directly from a Colombian savings or checking account.

- **Human URL:** [https://docs.wompi.co/en/docs/colombia/metodos-de-pago/](https://docs.wompi.co/en/docs/colombia/metodos-de-pago/)
- **Base URL:** `https://production.wompi.co/v1`

#### Tags

- PSE
- Bank Transfer
- ACH

#### Properties

- [Documentation](https://docs.wompi.co/en/docs/colombia/metodos-de-pago/)
- [OpenAPI](openapi/wompi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wompi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Wompi Payment Links API

Creates hosted, shareable payment links (checkout.wompi.co/l/...) for fixed or open amounts. Requires the private key.

- **Human URL:** [https://docs.wompi.co/en/docs/colombia/links-de-pago/](https://docs.wompi.co/en/docs/colombia/links-de-pago/)
- **Base URL:** `https://production.wompi.co/v1`

#### Tags

- Payment Links
- Hosted Checkout
- No Code

#### Properties

- [Documentation](https://docs.wompi.co/en/docs/colombia/links-de-pago/)
- [OpenAPI](openapi/wompi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wompi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Wompi Merchants & Acceptance Tokens API

Returns merchant configuration, accepted methods/currencies, and the mandatory presigned acceptance tokens (end-user policy + personal-data authorization) used when creating transactions and payment sources.

- **Human URL:** [https://docs.wompi.co/en/docs/colombia/tokens-de-aceptacion/](https://docs.wompi.co/en/docs/colombia/tokens-de-aceptacion/)
- **Base URL:** `https://production.wompi.co/v1`

#### Tags

- Merchants
- Acceptance Tokens

#### Properties

- [Documentation](https://docs.wompi.co/en/docs/colombia/tokens-de-aceptacion/)
- [OpenAPI](openapi/wompi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wompi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Wompi Events (Webhooks)

Server-to-server webhook notifications (HTTP POST) for transaction and payment-source state changes, validated with an asymmetric integrity checksum carried in the X-Event-Checksum header and the event signature object.

- **Human URL:** [https://docs.wompi.co/en/docs/colombia/eventos/](https://docs.wompi.co/en/docs/colombia/eventos/)
- **Base URL:** `https://production.wompi.co/v1`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://docs.wompi.co/en/docs/colombia/eventos/)

## Common Properties

- [Website](https://wompi.co/)
- [Documentation](https://docs.wompi.co/)
- [Authentication](authentication/wompi-authentication.yml)
- [Domain Security](security/wompi-domain-security.yml)
- [Trust Center](security/wompi-trust-center.yml)
- [Vulnerability Disclosure](security/wompi-vulnerability-disclosure.yml)
- [Agentic Access](agentic-access/wompi-agentic-access.yml)
- [Plans](plans/wompi-plans-pricing.yml)
- [Rate Limits](rate-limits/wompi-rate-limits.yml)
- [Fin Ops](finops/wompi-finops.yml)

## Notes

- **Ownership:** Wompi is part of Grupo Bancolombia (Colombia's largest bank). Merchants settle directly in Colombian Pesos (COP).
- **Regions:** Wompi also operates in Panamá (docs.wompi.co/en/docs/panama) and El Salvador (docs.wompi.sv). This descriptor covers the Colombia surface.
- **Spec provenance:** No first-party OpenAPI is published; `openapi/wompi-openapi.yml` is modeled from the public docs at docs.wompi.co.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
