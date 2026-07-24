---
name: Announce and track a customer return
description: Authenticate, announce an inbound customer return so byrd can receive and restock it, and list returns to track status via the byrd fulfillment API.
api: https://api.getbyrd.com
operations: [loginapiv2_post, returnshipmentannouncedapi_post, returnshipmentlistapi_get]
---

# Announce and track a return (byrd)

Base URL: `https://api.getbyrd.com`. Send `Content-Type: application/json`, TLS 1.2+, and the required `User-Agent` header.

## Steps

1. **Authenticate** — `POST /v2/login` (`loginapiv2_post`); cache the JWT and send `Authorization: Bearer <JWT>`.
2. **Announce the return** — `POST` the announced-returns endpoint (`returnshipmentannouncedapi_post`) with the original order/shipment reference and the items being returned, so byrd's warehouse expects the inbound return.
3. **Track returns** — `GET` the returns list (`returnshipmentlistapi_get`) and poll for the return's processing/restock status. Poll hourly (5-minute minimum interval).

## Rules
- No Idempotency-Key header; de-duplicate on your return reference.
- Errors follow the `{ code, message, errors[] }` envelope (`application/json`); refresh the JWT on `Authentication.ExpiredJWTToken` and retry. See `errors/byrd-error-codes.yml` and `conventions/byrd-conventions.yml`.
