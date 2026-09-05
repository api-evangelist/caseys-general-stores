---
generated: '2026-09-05'
method: generated
name: Look up items in a store's pricebook
description: Read Item Master (Pricebook) items for a Casey's store, related items by UPC, and the store's supplier list.
api: openapi/caseys-general-stores-item-api-openapi.yml
operations: [getItemByStoreNumberV2, getRelatedItemsByUpcV2, getItemByStoreNumberUnbuffered, getSuppliersForStore]
source: >-
  Generated from openapi/caseys-general-stores-item-api-openapi.yml and
  openapi/caseys-general-stores-supplier-api-openapi.yml, harvested from the Casey's Azure API
  Management catalogue. operationIds verified verbatim in those documents.
---

# Look up items in a store's pricebook

## Base URLs
- Items: `https://esl.caseys.io/itemapi`
- Suppliers: `https://esl.caseys.io/supplierapi`

## Auth
`Ocp-Apim-Subscription-Key` header, one key per API product.

## Steps
1. **Read the pricebook for a store** — `getItemByStoreNumberV2` (`GET /v2/store-items`). Filter with `ItemStatuses`, `Description`, `PreferredItemsOnly`, `Classification`, `SupplierId`. Page with `Limit`/`Offset`. Returns `storeItem` records carrying `itemCost`, `itemRetailPrice`, `itemStatus`, `itemSupplier` and `restriction`.
2. **Find related items** — `getRelatedItemsByUpcV2` (`GET /v2/related-items`) with `Upc`.
3. **Read the store's suppliers** — `getSuppliersForStore` (`GET /v1/suppliers`) on SupplierApi.

## Buffered vs unbuffered
`getItemByStoreNumberUnbuffered` (`GET /v2/unbuffered-store-items`) returns the same item data without buffering. Prefer the buffered `getItemByStoreNumberV2` unless you specifically need to bypass the cache — the contract does not state the buffer window, so do not assume one.

## GraphQL
ItemApi also exposes `POST /graphql` for item data. The schema is auth-gated — anonymous introspection returns 401 — so the fields are not published. Discover them with an authenticated introspection call; do not assume a shape.

## Errors
`apiError` `{code, message}` under `application/json`. See `errors/caseys-general-stores-problem-types.yml`.
