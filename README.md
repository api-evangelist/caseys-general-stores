# Casey's General Stores (caseys-general-stores)

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

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/caseys-general-stores/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Producing
- **Access:** 3rd-Party

## Tags:

 - APIs, Azure API Management, Conexxus, Convenience Stores, Food Service, Fortune 500, Fuel Pricing, Fuel Retail, GraphQL, Item Data, Loyalty, OpenAPI, Pizza, Point of Sale, Retail, Store Locations, Supply Chain, Tax

## Timestamps

- **Created:** 2026-03-21
- **Modified:** 2026-09-05

## APIs

Casey's publishes 21 OpenAPI 3.0.1 contracts (158 operations) through an Azure API Management gateway at `https://esl.caseys.io`, catalogued on a developer portal at https://developer.esl.caseys.io/. Every call is authorised by an APIM subscription key requested per API from that portal; a UAT environment mirrors the estate at `https://uat.esl.caseys.io` / https://developer-uat.esl.caseys.io/.

- **Casey's CasApi** — `https://esl.caseys.io/casapi` — Stores POS Activity Report documents from Casey's point-of-sale estate, implementing the Conexxus POS Back Office Interface / POS Activity Reporting API standard. Publishes report and journal documents and exposes a heartbeat health check and its own OpenAPI document.
- **Casey's CasGatewayApi** — `https://esl.caseys.io/casgatewayapi` — Gateway for POS POSJournal document management, implementing the Conexxus POS Back Office Interface standard. Accepts journal, report and journal-reconciliation postings and serves individual CPJR documents by store number, report type and document id.
- **Casey's DevOpsMetricsApi** — `https://esl.caseys.io/devopsmetricsapi` — Internal DevOps metrics API. The publicly exported contract exposes only a v1 heartbeat health check and the OpenAPI document; the metrics operations themselves are not present in the published definition.
- **Casey's DigitalProductionPlannerApi** — `https://esl.caseys.io/digitalproductionplannerapi` — GraphQL surface for digital production-planner data used by Casey's kitchen and prepared-food production planning. The published REST contract exposes a single POST /graphql operation plus the OpenAPI document; the schema itself requires an authenticated introspection call.
- **Casey's FuelPriceApi** — `https://esl.caseys.io/fuelpriceapi` — Returns fuel price data for Casey's stores. POST a list of store numbers to /fuelprices to retrieve current fuel pricing per store, with a heartbeat health check.
- **Casey's ItemApi** — `https://esl.caseys.io/itemapi` — Item Master (Pricebook) API. Returns up-to-date item data for a store, related items by UPC, and an unbuffered variant of the store-items read, alongside a GraphQL endpoint for item data.
- **Casey's ItsmApi** — `https://esl.caseys.io/itsmapi` — Creates, updates and attaches files to incidents in Casey's IT service management tool, with a v1 heartbeat health check.
- **Casey's KitchenSupplyOrderingapi** — `https://esl.caseys.io/kitchensupplyorderingapi` — GraphQL surface for kitchen supply ordering data used by Casey's prepared-food kitchens, plus a v1 heartbeat health check.
- **Casey's OldStoreApi** — `https://esl.caseys.io/oldstoreapi` — Legacy store-information API. Twenty-eight operations cover stores, brands, regions, hours and the organization hierarchy; the v0 surface is explicitly tagged deprecated in the published contract in favour of StoreApi and StoreDetailsApi.
- **Casey's PowerInventoryApi** — `https://esl.caseys.io/powerinventoryapi` — GraphQL surface for power inventory data, plus a v1 heartbeat health check.
- **Casey's ProductionPlannerApi** — `https://esl.caseys.io/productionplannerapi` — GraphQL surface for production-planner data driving prepared-food production schedules. The published REST contract exposes POST /graphql and the OpenAPI document only.
- **Casey's ShelfLabelPrintApi** — `https://esl.caseys.io/shelflabelprintapi` — GraphQL surface for shelf-label print data used to drive in-store shelf label printing, plus a v1 heartbeat health check.
- **Casey's StoreApi** — `https://esl.caseys.io/storeapi` — The Store API represents key points of information about Casey's stores. Thirty-seven operations cover stores, store hours, amenities, brands, locations, districts, divisions, regions and the wider organizational hierarchy, in both v0 (deprecated) and v1 shapes.
- **Casey's StoreDetailsApi** — `https://esl.caseys.io/storedetailsapi` — Store detail reads across the Casey's estate — stores, brands, regions, hours and the all-stores organization hierarchy — as a twenty-three operation successor surface to the legacy store API.
- **Casey's StoreMessagingApi** — `https://esl.caseys.io/storemessagingapi` — Allows services running in a Casey's store to receive messages from external sources. Registers store agents (v1 and v2 registration), lists registered services, sends messages to a store, and carries a deprecated order-fulfilment ticket-printing endpoint.
- **Casey's StoreNumberApi** — `https://esl.caseys.io/storenumberapi` — The Store Number Generator API returns available store numbers and version/health information for Casey's store-numbering system.
- **Casey's SupplierApi** — `https://esl.caseys.io/supplierapi` — Returns the list of suppliers for a given store and exposes a GraphQL endpoint for supplier data, plus a v1 heartbeat health check.
- **Casey's TankLevelApi** — `https://esl.caseys.io/tanklevelapi` — Fuel tank telemetry. Reads the most recent tank level readings and accepts new tank level readings for Casey's fuel sites, with a v1 heartbeat health check.
- **Casey's TaxApi** — `https://esl.caseys.io/taxapi` — Tax calculation and configuration for Casey's stores: POST /Taxes for tax calculation, plus per-store tax strategies, tax levels and compound taxes.
- **Casey's TeamMemberApi** — `https://esl.caseys.io/teammemberapi` — Team member information API. The publicly exported contract exposes only the heartbeat health check and the OpenAPI document; the team member reads themselves are not present in the published definition.
- **Casey's VendorCheckinApi** — `https://esl.caseys.io/vendorcheckinapi` — GraphQL surface for vendor check-in data covering deliveries and vendor visits to Casey's stores, plus a v1 heartbeat health check.

Eight of these APIs also expose a `POST /graphql` endpoint. Their schemas are auth-gated (anonymous introspection returns HTTP 401), so no GraphQL SDL is captured here rather than a guessed one.

Two further APIM products — `OrderApi_default` and `BagLabelPrintingApi_default` — are published but their contracts are not visible to unauthenticated visitors, so the estate is at least 23 APIs.

## Common Properties

- [DomainSecurity](security/caseys-general-stores-domain-security.yml)
- [LinkedIn](https://www.linkedin.com/company/caseys)
- [Website](https://www.caseys.com)
- [About](https://www.caseys.com/about-caseys)
- [Careers](https://www.caseys.com/careers)
- [InvestorRelations](https://investor.caseys.com/)
- [Rewards](https://www.caseys.com/rewards)
- [Mobile](https://www.caseys.com/mobile-app)
- [Contact](https://www.caseys.com/contact-us)
- [TermsOfService](https://www.caseys.com/terms-of-use)
- [PrivacyPolicy](https://www.caseys.com/privacy-policy)
- [Accessibility](https://www.caseys.com/accessibility)
- [Sitemap](https://www.caseys.com/sitemap)
- [PressReleases](https://investor.caseys.com/press-releases)
- [DeveloperPortal](https://developer.esl.caseys.io/)
- [GettingStarted](https://developer.esl.caseys.io/)
- [Login](https://developer.esl.caseys.io/signin)
- [Authentication](authentication/caseys-general-stores-authentication.yml)
- [Conventions](conventions/caseys-general-stores-conventions.yml)
- [ErrorCatalog](errors/caseys-general-stores-problem-types.yml)
- [Lifecycle](lifecycle/caseys-general-stores-lifecycle.yml)
- [Conformance](conformance/caseys-general-stores-conformance.yml)
- [DataModel](data-model/caseys-general-stores-data-model.yml)
- [ToolCrosswalk](mcp/caseys-general-stores-tool-crosswalk.yml)
- [X-MCPServerCandidate](mcp/caseys-general-stores-mcp.yml)
- [LLMsTxt](llms/caseys-general-stores-llms.txt)
- [AgentSkill](skills/_index.yml)
- [Sandbox](sandbox/caseys-general-stores-sandbox.yml)
- [Plans](plans/caseys-general-stores-plans-pricing.yml)
- [RateLimits](rate-limits/caseys-general-stores-rate-limits.yml)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
