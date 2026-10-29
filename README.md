# Byrd

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

byrd is a European e-commerce fulfillment and third-party logistics (3PL) provider operating a network of 25+ fulfillment warehouses across Europe and the UK. It offers multichannel order fulfillment with integrations to the major shop and marketplace platforms (Shopify, Amazon, eBay, WooCommerce, Shopware, PlentyONE, Mirakl and more), inventory and warehouse management, carrier shipping, returns handling, and analytics. byrd exposes a developer REST API (developers.getbyrd.com) for programmatically managing products, deliveries, shipments, and returns, secured with JWT bearer authentication. byrd is a Speedinvest portfolio company.

**Areas:** Company · E-Commerce · Fulfillment · Logistics · 3PL · Shipping · Warehousing · Order Management · Inventory · Returns · Supply Chain

## Byrd on APIs.io

Everything profiled for Byrd is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/byrd/](https://apis.io/providers/byrd/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [Byrd Account API](https://apis.io/apis/byrd/byrd-account-api/) — The warehouses and B2B templates available to your account, and CSV exports of your shipments, returns and inventory.
- [Byrd Authentication API](https://apis.io/apis/byrd/byrd-authentication-api/) — Log in with your API key to get an access token, refresh it, and read or update your account.
- [Byrd Catalog API](https://apis.io/apis/byrd/byrd-catalog-api/) — Products and bundles, their lots, serial numbers and stock, and the dangerous goods limits that apply to them.
- [Byrd Inbound API](https://apis.io/apis/byrd/byrd-inbound-api/) — Deliveries of your stock to a warehouse: announce them, follow them in, and manage their documents.
- [Byrd Shipments API](https://apis.io/apis/byrd/byrd-shipments-api/) — Orders shipped to your customers: create and release them, follow their units and picks, and handle their returns.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [byrd](https://apis.io/servers/byrd/byrd/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Byrd Agentic Access](https://apis.io/agentic-access/byrd/byrd-agentic-access/)

#### JSON Schema (6)

The data models the API reads and writes.

- [Delivery](https://apis.io/schemas/byrd/byrd-delivery/)
- [Delivery create](https://apis.io/schemas/byrd/byrd-delivery-create/)
- [Delivery create request](https://apis.io/schemas/byrd/byrd-delivery-create-request/)
- [Delivery with metrics](https://apis.io/schemas/byrd/byrd-delivery-with-metrics/)
- [Product](https://apis.io/schemas/byrd/byrd-product/)
- [Shipment](https://apis.io/schemas/byrd/byrd-shipment/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Byrd Context](https://apis.io/jsonld/byrd/byrd-context/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Byrd API Rules](https://apis.io/rules/byrd/byrd-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Byrd Authentication](https://apis.io/security/byrd/byrd-authentication/)
- [Byrd Domain Security](https://apis.io/security/byrd/byrd-domain-security/)
- [Byrd Trust Center](https://apis.io/security/byrd/byrd-trust-center/)
- [Byrd Vulnerability Disclosure](https://apis.io/security/byrd/byrd-vulnerability-disclosure/)

#### Rate limits (1)

Published request limits.

- [Byrd Rate Limits](https://apis.io/rate-limits/byrd/byrd-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.getbyrd.com)
- [Documentation](https://developers.getbyrd.com/docs)
- [Getting started](https://developers.getbyrd.com/docs/integration-overview)
- [API reference](https://developers.getbyrd.com/reference)
- [Pricing](https://www.getbyrd.com/preise)
- [Sign up](https://www.getbyrd.com/kontakt)
- [Support](https://support.getbyrd.com/knowledge-base)
- [Changelog](https://developers.getbyrd.com/changelog)
- [Blog](https://blog.getbyrd.com)
- [Security](https://www.getbyrd.com/en/vulnerability-disclosure-program)
- [Trust centre](https://www.getbyrd.com/en/security-startpage)
- [Terms of service](https://www.getbyrd.com/agbs)
- [Privacy policy](https://www.getbyrd.com/privacy)

## API Evangelist rating

**Kin Score 53.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 76.8 |
| Contract quality | 67.2 |
| Contract governance | 22.0 |
| Operational transparency | 39.5 |
| Developer ergonomics | 39.9 |
| Access clarity | 52.6 |

**Agent readiness 27.7** — agent-aware

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
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | yes |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly |

**Regulatory alignment 35.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/byrd/](https://apis.io/providers/byrd/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Byrd: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/byrd/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
