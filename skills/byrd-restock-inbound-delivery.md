---
name: Announce an inbound delivery to restock inventory
description: Authenticate, ensure the product exists, announce an inbound delivery of stock to a byrd warehouse, and track the delivery until received.
api: https://api.getbyrd.com
operations: [loginapiv2_post, productsapi_post, deliveriesapi_post, deliveriesapi_get]
---

# Announce an inbound delivery (byrd)

Base URL: `https://api.getbyrd.com`. Send `Content-Type: application/json`, TLS 1.2+, and the required `User-Agent` header.

## Steps

1. **Authenticate** — `POST /v2/login` (`loginapiv2_post`); cache the JWT and send `Authorization: Bearer <JWT>`.
2. **Ensure the product exists** — if the SKU is new, `POST /products` (`productsapi_post`) to create it before announcing stock against it. Existing products can be listed with `productsapi_get`.
3. **Announce the delivery** — `POST /deliveries` (`deliveriesapi_post`) describing the inbound units (products and quantities) and the destination warehouse. This tells byrd to expect and book in the goods.
4. **Track receipt** — `GET /deliveries` (`deliveriesapi_get`), optionally filtered by date, and poll the delivery status until byrd marks it received. Poll hourly (5-minute minimum interval).

## Rules
- No Idempotency-Key header exists; de-duplicate deliveries on your own reference.
- Handle `Authentication.ExpiredJWTToken` by refreshing via `/v2/refresh_token`. Validation failures surface as `Request.InvalidSchema` / `Request.NoInput` in the `{ code, message, errors[] }` envelope.
