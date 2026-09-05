---
generated: '2026-09-05'
method: generated
name: Submit a Conexxus POS activity report or journal
description: Publish POS Activity Report and POSJournal documents to Casey's under the Conexxus POS Back Office Interface standard, and retrieve a stored journal document.
api: openapi/caseys-general-stores-cas-gateway-api-openapi.yml
operations: [post-reports, post-journal, post-journalreconciliation, get-cpjr-document, get-reports]
source: >-
  Generated from openapi/caseys-general-stores-cas-gateway-api-openapi.yml and
  openapi/caseys-general-stores-cas-api-openapi.yml, harvested from the Casey's Azure API Management
  catalogue. operationIds and header names verified verbatim in those documents.
---

# Submit a Conexxus POS activity report or journal

This is the machine-to-machine ingestion surface for Casey's point-of-sale estate. It implements the **Conexxus POS Back Office Interface** and the **Conexxus POS Activity Reporting API** standard; the API major version mirrors the standard's major version. See `conformance/caseys-general-stores-conformance.yml`.

## Base URLs
- `https://esl.caseys.io/casgatewayapi` (POSJournal documents)
- `https://esl.caseys.io/casapi` (POS Activity Report documents)

## Required headers on every operation
- `Ocp-Apim-Subscription-Key` — APIM subscription key.
- `openretailing-organization-id` — Conexxus Open Retailing organization identifier.
- `openretailing-store-location-id` — Conexxus Open Retailing store location identifier.
- `x-correlation-id` — quote this value to Casey's support when a submission fails. Nothing else in the estate gives you a trace handle.

## Steps
1. **Post a report** — `post-reports` (`POST /report`).
2. **Post a journal** — `post-journal` (`POST /journal`).
3. **Post a reconciliation** — `post-journalreconciliation` (`POST /journal/reconciliation`). This reconciles a journal; it is **not** a reversal of a previous submission and the contract does not describe it as one.
4. **Retrieve a stored document** — `get-cpjr-document` (`GET /journal/{storeNumber}/{reportType}/{documentId}`).

## Before you retry
- **There is no idempotency mechanism.** No `Idempotency-Key` header is declared on any of these operations. If a POST times out you cannot safely replay it — reconcile with `get-cpjr-document` first where you have the document id, and involve Casey's with the `x-correlation-id` otherwise.
- **There is no reversal.** No delete, void or correction operation exists. A duplicate document must be resolved out of band.
- **413 is declared.** Oversized documents are rejected with `413 Payload Too Large`; chunk before you send.

## Response envelope
`statusReturn` `{timestamp, result, message}` where `result` is an integer enum 0–12. **The meaning of each value is not documented in the contract.** Do not branch on a guessed mapping — read `message`, and ask Casey's for the enum table.
