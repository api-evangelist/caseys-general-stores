---
generated: '2026-09-05'
method: generated
name: Read fuel prices and tank levels
description: Fetch current fuel prices for a set of Casey's stores and the most recent fuel tank level readings.
api: openapi/caseys-general-stores-fuel-price-api-openapi.yml
operations: [getFuelPricesByStoreNumbers, getMostRecentTankLevels, postTankLevels]
source: >-
  Generated from openapi/caseys-general-stores-fuel-price-api-openapi.yml and
  openapi/caseys-general-stores-tank-level-api-openapi.yml, harvested from the Casey's Azure API
  Management catalogue. operationIds verified verbatim in those documents.
---

# Read fuel prices and tank levels

Two APIs, two subscription keys.

## Base URLs
- Fuel prices: `https://esl.caseys.io/fuelpriceapi`
- Tank levels: `https://esl.caseys.io/tanklevelapi`

## Auth
`Ocp-Apim-Subscription-Key` header, one key per API product. See `authentication/caseys-general-stores-authentication.yml`.

## Steps
1. **Resolve store numbers** — use `get-v1-stores` on StoreApi first if you only have names or locations.
2. **Fetch fuel prices** — `getFuelPricesByStoreNumbers` (`POST /fuelprices`) with a body of `{"storeId":[<store numbers>]}`. This is a POST-shaped read: it changes nothing.
3. **Fetch tank levels** — `getMostRecentTankLevels` (`GET /v1/tanklevel/getmostrecentreadings`). Page with `Limit` and `Offset` — note the capitalised parameter names here, which differ from StoreApi's lowercase `limit`/`offset`.

## Writing a tank reading
`postTankLevels` (`POST /v1/tanklevel/addlevels`) appends readings.

- **No idempotency.** No `Idempotency-Key` header exists on this operation. A retry after a timeout can duplicate a reading.
- **No reversal.** There is no delete, void or correction operation anywhere in this estate. A submitted reading cannot be taken back through the API.

## Health
Each API exposes `getHeartbeatV1` (`GET /v1/heartbeat`), which returns `{"status": "..."}` and 503 when a dependency check fails. It requires a subscription key like every other operation — there is no anonymous status endpoint and no status page.
