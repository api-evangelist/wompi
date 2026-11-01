# Wompi

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Wompi is the payment gateway of Grupo Bancolombia, serving Colombia (COP). Its REST API creates and tracks transactions across local payment methods - CARD, NEQUI (mobile wallet), PSE (online bank debit), and Bancolombia Transfer / Collect - plus card and Nequi tokenization, reusable payment sources, and hosted payment links. Public-key endpoints are browser-safe; private-key endpoints are server-side.

**Areas:** Payments · Fintech · Colombia · Latin America · Payment Gateway · PSE · Nequi

## Wompi on APIs.io

Everything profiled for Wompi is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/wompi/](https://apis.io/providers/wompi/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [Wompi Events (Webhooks)](https://apis.io/apis/wompi/wompi-events-webhooks/) — Server-to-server webhook notifications (HTTP POST) for transaction and payment-source state changes, validated with an asymmetric integrity checksum carried…
- [Wompi Merchants API](https://apis.io/apis/wompi/wompi-merchants-api/) — Merchant info and presigned acceptance tokens.
- [Wompi Payment Links API](https://apis.io/apis/wompi/wompi-payment-links-api/) — Hosted, shareable payment links.
- [Wompi Payment Sources API](https://apis.io/apis/wompi/wompi-payment-sources-api/) — Reusable payment sources for recurring charges.
- [Wompi PSE API](https://apis.io/apis/wompi/wompi-pse-api/) — PSE financial institution catalog.
- [Wompi Tokenization API](https://apis.io/apis/wompi/wompi-tokenization-api/) — Tokenize cards and Nequi accounts.
- [Wompi Transactions API](https://apis.io/apis/wompi/wompi-transactions-api/) — Create and track payment transactions.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Wompi Webhooks](https://apis.io/asyncapis/wompi/wompi-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [wompi](https://apis.io/servers/wompi/wompi/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Wompi Agentic Access](https://apis.io/agentic-access/wompi/wompi-agentic-access/)

#### Collections (12)

Postman and Open Collection request collections.

- [Wompi Merchants API](https://apis.io/collections/wompi/open-wompi-merchants-api/)
- [Wompi Merchants Payment Links API](https://apis.io/collections/wompi/open-wompi-payment-links-api/)
- [Wompi Merchants Payment Sources API](https://apis.io/collections/wompi/open-wompi-payment-sources-api/)
- [Wompi Merchants PSE API](https://apis.io/collections/wompi/open-wompi-pse-api/)
- [Wompi Merchants Tokenization API](https://apis.io/collections/wompi/open-wompi-tokenization-api/)
- [Wompi Merchants Transactions API](https://apis.io/collections/wompi/open-wompi-transactions-api/)
- [Wompi Merchants API](https://apis.io/collections/wompi/postman-wompi-merchants-api/)
- [Wompi Merchants Payment Links API](https://apis.io/collections/wompi/postman-wompi-payment-links-api/)
- [Wompi Merchants Payment Sources API](https://apis.io/collections/wompi/postman-wompi-payment-sources-api/)
- [Wompi Merchants PSE API](https://apis.io/collections/wompi/postman-wompi-pse-api/)
- [Wompi Merchants Tokenization API](https://apis.io/collections/wompi/postman-wompi-tokenization-api/)
- [Wompi Merchants Transactions API](https://apis.io/collections/wompi/postman-wompi-transactions-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Wompi Openapi Overlay](https://apis.io/overlays/wompi/wompi-openapi-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Wompi Authentication](https://apis.io/security/wompi/wompi-authentication/)
- [Wompi Domain Security](https://apis.io/security/wompi/wompi-domain-security/)
- [Wompi Trust Center](https://apis.io/security/wompi/wompi-trust-center/)
- [Wompi Vulnerability Disclosure](https://apis.io/security/wompi/wompi-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Wompi Plans Pricing](https://apis.io/plans/wompi/wompi-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Wompi Rate Limits](https://apis.io/rate-limits/wompi/wompi-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Wompi Finops](https://apis.io/finops/wompi/wompi-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://wompi.co/)
- [Documentation](https://docs.wompi.co/)
- [Getting started](https://docs.wompi.co/en/docs/colombia/inicio-rapido/)
- [API reference](https://docs.wompi.co/en/docs/colombia/referencia/)
- [Sign up](https://comercios.wompi.co/)
- [Terms of service](https://wompi.co/es/co/terminos-y-condiciones)
- [Status](https://wompi.statuspage.io/)

## API Evangelist rating

**Kin Score 44.4** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 55.7 |
| Contract governance | 4.5 |
| Operational transparency | 39.5 |
| Developer ergonomics | 50.6 |
| Access clarity | 31.6 |

**Agent readiness 28.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 35.7** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/wompi/](https://apis.io/providers/wompi/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Wompi: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/wompi/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
