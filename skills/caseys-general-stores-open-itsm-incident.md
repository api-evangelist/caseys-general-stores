---
generated: '2026-09-05'
method: generated
name: Open and update an ITSM incident
description: Create an incident in Casey's IT service management tool, update it, and attach a file.
api: openapi/caseys-general-stores-itsm-api-openapi.yml
operations: [createIncident, updateIncidentById, addAttachment, getHeartbeatV1]
source: >-
  Generated from openapi/caseys-general-stores-itsm-api-openapi.yml, harvested from the Casey's
  Azure API Management catalogue. operationIds verified verbatim in that document.
---

# Open and update an ITSM incident

## Base URL
`https://esl.caseys.io/itsmapi`

## Auth
`Ocp-Apim-Subscription-Key` header.

## Steps
1. **Create** — `createIncident` (`POST /v1/incidents`) with a `createIncidentParameterModel` body (`requestedByModel`, `assignedToModel`, description and comment fields). Capture the returned incident id.
2. **Update** — `updateIncidentById` (`PUT /v1/incidents`) with an `updateIncidentParameterModel` body.
3. **Attach** — `addAttachment` (`POST /v1/incidents/attachments`) with an `attachmentParameterModel` body. `413 Payload Too Large` is declared — check the size before sending.

## Agent safety
- **Not idempotent.** A retried `createIncident` opens a second ticket. There is no `Idempotency-Key` header and no client-supplied dedupe key in the request model.
- **Not reversible.** No close, cancel or delete operation is published. An incident opened in error must be closed by a human in the ITSM tool.
- Send `x-correlation-id` on every call — it is declared on this API and is your only trace handle.

## Errors
This API is the best-documented in the estate for failures: it ships worked `400` examples (`createIncidentBadRequestExample`, `updateIncidentBadRequestExample`, `addAttachmentBadRequestExample`). See `errors/caseys-general-stores-problem-types.yml`.
