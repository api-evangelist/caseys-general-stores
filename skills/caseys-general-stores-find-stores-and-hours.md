---
generated: '2026-09-05'
method: generated
name: Find Casey's stores and their hours
description: Locate stores in the Casey's estate, read one store's detail, and read opening hours for one store or all stores.
api: openapi/caseys-general-stores-store-api-openapi.yml
operations: [get-v1-stores, get-v1-stores-storenumber, get-v1-stores-storenumber-hours, get-v1-stores-hours, get-v1-brands]
source: >-
  Generated from openapi/caseys-general-stores-store-api-openapi.yml (harvested from the Casey's
  Azure API Management catalogue at developer.esl.caseys.io). Every operationId below was verified
  verbatim in that document. Cross-cutting rules cite conventions/, errors/ and authentication/.
---

# Find Casey's stores and their hours

Read-only. Nothing in this skill changes state.

## Base URL
`https://esl.caseys.io/storeapi`

## Auth
- Azure API Management subscription key in the `Ocp-Apim-Subscription-Key` request header (or `subscription-key` query parameter).
- Keys are per API product. A StoreApi key does not authorise ItemApi or FuelPriceApi. See `authentication/caseys-general-stores-authentication.yml`.

## Steps
1. **List stores** — `get-v1-stores` (`GET /v1/stores`). Page with `limit` and `offset`. Filter with `storeName`, `storeBrand`, `propertyStatus` where you need a subset.
2. **Read one store** — `get-v1-stores-storenumber` (`GET /v1/stores/{storeNumber}`). `storeNumber` is the join key for every other API in this estate.
3. **Read hours** — `get-v1-stores-storenumber-hours` (`GET /v1/stores/{storeNumber}/hours`) for one store, or `get-v1-stores-hours` (`GET /v1/stores/hours`) for all stores.
4. **Resolve the brand** — `get-v1-brands` (`GET /v1/brands`) to map a store's brand code to a brand name.

## Do not call the v0 surface
`getAllStoresV0`, `getStoreByIdV0`, `getHoursByStoreV0`, `getAllStoreHoursV0` and `getBrandsV0` are marked **deprecated** in the contract. No Sunset header and no retirement date is published, so treat them as removable without notice. See `lifecycle/caseys-general-stores-lifecycle.yml`.

## Pagination
Offset-based: `limit` + `offset`. Responses are bare arrays — there is no total or next-cursor field, so page until a short page comes back.

## Errors
`apiError` `{code, message}` under `application/json`. 401 means a missing or invalid subscription key; the gateway answers `{"statusCode":401,"message":"Unauthorized. Access token is missing or invalid."}` before the API is reached. See `errors/caseys-general-stores-problem-types.yml`.
