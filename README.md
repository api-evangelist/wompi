# Wompi (wompi)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
