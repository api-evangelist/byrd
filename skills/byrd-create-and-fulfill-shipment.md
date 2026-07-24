---
name: Create and fulfill an outbound shipment
description: Authenticate, confirm product stock, create an outbound shipment for a customer order, release it for fulfillment, and track its status via the byrd fulfillment API.
api: https://api.getbyrd.com
operations: [loginapiv2_post, productsapi_get, shipmentlistapiv3_post, shipmentbatchreleaseapiv3_post, shipmentapiv3_get]
---

# Create and fulfill an outbound shipment (byrd)

Base URL: `https://api.getbyrd.com`. Always send `Content-Type: application/json`, TLS 1.2+, and a `User-Agent` in the form `<company-registered-in-byrd> (tech-contact-email) - <version>`.

## Steps

1. **Authenticate** — `POST /v2/login` (`loginapiv2_post`) with your byrd credentials. Cache the returned JWT and send it as `Authorization: Bearer <JWT>` on every subsequent call. Do not re-login per request (the login endpoint is capped at 5 calls/min per IP/User-Agent); refresh with `POST /v2/refresh_token` before expiry.
2. **Confirm stock** — `GET /products` (`productsapi_get`) to list products and read available stock for the SKUs in the order. Only proceed for items with sufficient on-hand quantity.
3. **Create the shipment** — `POST /v3/shipments` (`shipmentlistapiv3_post`) with `destination_address`, `items` (≥1), `service`, and `warehouse_id`. Tip: send `?validate_only=true` first to dry-run the payload — byrd validates without creating the shipment and returns any `Request.InvalidSchema` / `Request.NoInput` errors. Then repeat without the flag to create it.
4. **Release for fulfillment** — `POST /v3/shipments/.../release` (`shipmentbatchreleaseapiv3_post`) to schedule the created shipment(s) for picking and dispatch.
5. **Track** — `GET /v3/shipments/{shipment_id}` (`shipmentapiv3_get`) and poll `status`. byrd recommends polling no more often than every 5 minutes (hourly is typical).

## Rules
- byrd does **not** support an Idempotency-Key header; use `validate_only=true` to avoid duplicate creates, and de-duplicate on your side by order id.
- Errors are `application/json` with shape `{ code, message, errors[] }`. Handle `Authentication.ExpiredJWTToken` by refreshing the token and retrying; treat `Request.*` codes as caller-fixable validation failures (see `errors/byrd-error-codes.yml`).
