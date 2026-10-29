# Casey's General Stores

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

Casey's General Stores (NASDAQ: CASY) is one of the largest convenience-store chains in the United States, operating more than 2,900 stores selling fuel, made-from-scratch pizza, prepared food and convenience items, primarily in small midwestern communities. Behind the consumer brand Casey's runs a B2B API estate on Azure API Management at esl.caseys.io: 21 published OpenAPI 3.0.1 contracts and 158 operations covering stores and the division/region/district hierarchy, the Item Master (Pricebook), fuel pricing, per-store tax configuration, fuel tank telemetry, suppliers, vendor check-in, kitchen production planning, shelf-label printing, in-store messaging and IT service-management incidents — plus Conexxus POS Back Office Interface document ingestion carrying Conexxus Open Retailing identifiers. Access is by Azure APIM subscription key requested through the developer portal at developer.esl.caseys.io; a UAT environment mirrors the estate. No pricing, rate limits, SDKs, status page, changelog, deprecation policy or MCP server are published.

**Areas:** Azure API Management · Conexxus · Convenience Stores · Food Service · Fortune 500 · Fuel Pricing · Fuel Retail · GraphQL · Item Data · Loyalty · OpenAPI · Pizza

## Casey's General Stores on APIs.io

Everything profiled for Casey's General Stores is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/caseys-general-stores/](https://apis.io/providers/caseys-general-stores/)** — or go straight to one of the APIs or properties below.

### APIs (41)

- [Casey's ItemApi](https://apis.io/apis/caseys-general-stores/caseys-itemapi/) — Item Master (Pricebook) API. Returns up-to-date item data for a store, related items by UPC, and an unbuffered variant of the store-items read, alongside a…
- [Casey's StoreApi](https://apis.io/apis/caseys-general-stores/caseys-storeapi/) — The Store API represents key points of information about Casey's stores. Thirty-seven operations cover stores, store hours, amenities, brands, locations,…
- [Casey's SupplierApi](https://apis.io/apis/caseys-general-stores/caseys-supplierapi/) — Returns the list of suppliers for a given store and exposes a GraphQL endpoint for supplier data, plus a v1 heartbeat health check.
- [Casey's General Stores Brands API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-brands-api/) — The brands API from Casey's General Stores — 2 operation(s) for brands.
- [Casey's General Stores Caseys.Store API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-caseys-storeapi-api/) — The Caseys.StoreApi API from Casey's General Stores — 1 operation(s) for caseys.storeapi.
- [Casey's General Stores Caseys.Store Number Generator.Api API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-caseys-storenumbergenerator-api-api/) — The Caseys.StoreNumberGenerator.Api API from Casey's General Stores — 2 operation(s) for caseys.storenumbergenerator.api.
- [Casey's General Stores Districts API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-districts-api/) — The Districts API from Casey's General Stores — 2 operation(s) for districts.
- [Casey's General Stores Divisions API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-divisions-api/) — The Divisions API from Casey's General Stores — 2 operation(s) for divisions.
- [Casey's General Stores Health API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-health-api/) — The Health API from Casey's General Stores — 1 operation(s) for health.
- [Casey's General Stores Heartbeat API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-heartbeat-api/) — The heartbeat API from Casey's General Stores — 2 operation(s) for heartbeat.
- [Casey's General Stores Hours API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-hours-api/) — The hours API from Casey's General Stores — 4 operation(s) for hours.
- [Casey's General Stores Incident API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-incident-api/) — The incident API from Casey's General Stores — 2 operation(s) for incident.
- [Casey's General Stores Location API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-location-api/) — The Location API from Casey's General Stores — 2 operation(s) for location.
- [Casey's General Stores organization hierarchy API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-organization-hierarchy-api/) — The organization hierarchy API from Casey's General Stores — 12 operation(s) for organization hierarchy.
- [Casey's General Stores Organizational API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-organizational-api/) — The Organizational API from Casey's General Stores — 3 operation(s) for organizational.
- [Casey's General Stores Print API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-print-api/) — The Print API from Casey's General Stores — 1 operation(s) for print.
- [Casey's General Stores Pull API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-pull-api/) — The pull API from Casey's General Stores — 2 operation(s) for pull.
- [Casey's General Stores Push API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-push-api/) — The push API from Casey's General Stores — 3 operation(s) for push.
- [Casey's General Stores Regions API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-regions-api/) — The Regions API from Casey's General Stores — 2 operation(s) for regions.
- [Casey's General Stores Register API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-register-api/) — The Register API from Casey's General Stores — 2 operation(s) for register.
- [Casey's General Stores Registrations API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-registrations-api/) — The Registrations API from Casey's General Stores — 1 operation(s) for registrations.
- [Casey's General Stores Store Amenities API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-storeamenities-api/) — The StoreAmenities API from Casey's General Stores — 1 operation(s) for storeamenities.
- [Casey's General Stores Store Organizational API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-storeorganizational-api/) — The StoreOrganizational API from Casey's General Stores — 2 operation(s) for storeorganizational.
- [Casey's General Stores Stores API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-stores-api/) — The Stores API from Casey's General Stores — 6 operation(s) for stores.
- [Casey's General Stores Swagger API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-swagger-api/) — The Swagger API from Casey's General Stores — 1 operation(s) for swagger.
- [Casey's General Stores Tank Levels API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-tanklevels-api/) — The tankLevels API from Casey's General Stores — 2 operation(s) for tanklevels.
- [Casey's General Stores Taxes API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-taxes-api/) — The Taxes API from Casey's General Stores — 1 operation(s) for taxes.
- [Casey's General Stores Unbuffered Store Items API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-unbuffered-store-items-api/) — The Unbuffered Store Items API from Casey's General Stores — 1 operation(s) for unbuffered store items.
- [Casey's General Stores V1 Store By ID API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-v1storebyid-api/) — The V1StoreById API from Casey's General Stores — 1 operation(s) for v1storebyid.
- [Casey's General Stores V1 Store Hours API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-v1storehours-api/) — The V1StoreHours API from Casey's General Stores — 1 operation(s) for v1storehours.
- [Casey's General Stores V1 Store Hours By Store Number API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-v1storehoursbystorenumber-api/) — The V1StoreHoursByStoreNumber API from Casey's General Stores — 1 operation(s) for v1storehoursbystorenumber.
- [Casey's General Stores V1 Stores API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-v1stores-api/) — The V1Stores API from Casey's General Stores — 1 operation(s) for v1stores.
- [Casey's General Stores Version API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-version-api/) — The Version API from Casey's General Stores — 1 operation(s) for version.
- [Casey's General Stores Deprecated API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-deprecated-api/) — The deprecated API from Casey's General Stores — 12 operation(s) for deprecated.
- [Casey's General Stores Region API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-region-api/) — The region API from Casey's General Stores — 1 operation(s) for region.
- [Casey's General Stores Relateditems API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-relateditems-api/) — The Relateditems API from Casey's General Stores — 1 operation(s) for relateditems.
- [Casey's General Stores Store Number API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-storenumber-api/) — The StoreNumber API from Casey's General Stores — 1 operation(s) for storenumber.
- [Casey's General Stores Upc API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-upc-api/) — The upc API from Casey's General Stores — 1 operation(s) for upc.
- [Casey's General Stores Fuel Prices API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-fuel-prices-api/) — The Fuel Prices API from Casey's General Stores — 1 operation(s) for fuel prices.
- [Casey's General Stores Graph QL API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-graph-ql-api/) — The Graph QL API from Casey's General Stores — 1 operation(s) for graph ql.
- [Casey's General Stores Open API](https://apis.io/apis/caseys-general-stores/caseys-general-stores-open-api-api/) — The Open API API from Casey's General Stores — 2 operation(s) for open api.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [caseys-general-stores-mcp.yml](https://apis.io/servers/caseys-general-stores/caseys-general-stores-mcp-yml/)

#### Overlays (21)

OpenAPI overlays, including conversational phrasing for each operation.

- [Caseys General Stores Cas Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-cas-api-overlay/)
- [Caseys General Stores Cas Gateway Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-cas-gateway-api-overlay/)
- [Caseys General Stores Devops Metrics Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-devops-metrics-api-overlay/)
- [Caseys General Stores Digital Production Planner Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-digital-production-planner-api-overlay/)
- [Caseys General Stores Fuel Price Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-fuel-price-api-overlay/)
- [Caseys General Stores Item Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-item-api-overlay/)
- [Caseys General Stores Itsm Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-itsm-api-overlay/)
- [Caseys General Stores Kitchen Supply Ordering Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-kitchen-supply-ordering-api-overlay/)
- [Caseys General Stores Old Store Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-old-store-api-overlay/)
- [Caseys General Stores Power Inventory Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-power-inventory-api-overlay/)
- [Caseys General Stores Production Planner Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-production-planner-api-overlay/)
- [Caseys General Stores Shelf Label Print Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-shelf-label-print-api-overlay/)
- [Caseys General Stores Store Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-store-api-overlay/)
- [Caseys General Stores Store Details Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-store-details-api-overlay/)
- [Caseys General Stores Store Messaging Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-store-messaging-api-overlay/)
- [Caseys General Stores Store Number Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-store-number-api-overlay/)
- [Caseys General Stores Supplier Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-supplier-api-overlay/)
- [Caseys General Stores Tank Level Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-tank-level-api-overlay/)
- [Caseys General Stores Tax Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-tax-api-overlay/)
- [Caseys General Stores Team Member Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-team-member-api-overlay/)
- [Caseys General Stores Vendor Checkin Api Overlay](https://apis.io/overlays/caseys-general-stores/caseys-general-stores-vendor-checkin-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Caseys General Stores Authentication](https://apis.io/security/caseys-general-stores/caseys-general-stores-authentication/)
- [Caseys General Stores Domain Security](https://apis.io/security/caseys-general-stores/caseys-general-stores-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Caseys General Stores Plans Pricing](https://apis.io/plans/caseys-general-stores/caseys-general-stores-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Caseys General Stores Rate Limits](https://apis.io/rate-limits/caseys-general-stores/caseys-general-stores-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.caseys.com)
- [Getting started](https://developer.esl.caseys.io/)
- [Terms of service](https://www.caseys.com/terms-of-use)
- [Privacy policy](https://www.caseys.com/privacy-policy)

## API Evangelist rating

**Kin Score 38.1** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 72.3 |
| Contract quality | 45.0 |
| Contract governance | 18.2 |
| Operational transparency | 0.0 |
| Developer ergonomics | 42.3 |
| Access clarity | 27.6 |

**Agent readiness 29.7** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/caseys-general-stores/](https://apis.io/providers/caseys-general-stores/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Casey's General Stores: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/caseys-general-stores/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
