---
name: Place and manage a limit order
description: Place a LIMIT order on One Trading and track it to fill or cancellation using a caller-supplied client_id.
api: openapi/one-trading-fast-openapi.yml
base_url: https://api.onetrading.com/fast
auth: Bearer API token with the TRADE scope
operations: [getInstruments, createOrder, getOrderByClientId, cancelOrderByClientId, getTradesForOrder]
---

# Place and manage a limit order

One Trading only supports `LIMIT` orders via the REST API. Prices and amounts are
decimal **strings**, not numbers.

## Prerequisites
- An API token generated in the One Trading UI with the **Trade** permission.
- Send it on every request as `Authorization: Bearer <token>`.

## Steps

1. **Resolve the market.** Call `getInstruments` (`GET /v1/instruments`) and pick
   the `instrument_code` you want (e.g. `BTC_USDC`). Note its `amount_precision`,
   `market_precision`, and `min_size` so your order passes validation.

2. **Generate a client_id.** Create a UUID and use it as `client_id`. This is the
   idempotency key: it de-duplicates the submission and lets you look the order up
   or cancel it without knowing the exchange `order_id`.

3. **Create the order.** Call `createOrder` (`POST /v1/account/orders`) with:
   `instrument_code`, `type: LIMIT`, `side` (`BUY`/`SELL`), `amount` (string),
   `price` (string), your `client_id`, and optionally `time_in_force`
   (`GOOD_TILL_CANCELLED` default, `IMMEDIATE_OR_CANCELLED`, `FILL_OR_KILL`,
   `POST_ONLY`). The response echoes `order_id` and `status`.
   - `400 Bad Request` / `422 Unprocessable Entity` return `{"error":"<CODE>"}` —
     usually precision or `min_size` violations. Fix and retry with the SAME
     `client_id`.

4. **Track it.** Poll `getOrderByClientId`
   (`GET /v1/account/orders/client/{client_id}`) for `status`, and
   `getTradesForOrder` (`GET /v1/account/orders/{order_id}/trades`) for fills.

5. **Cancel if needed.** Call `cancelOrderByClientId`
   (`DELETE /v1/account/orders/client/{client_id}`).

## Rules
- Errors carry a single machine-readable code on the `error` field (not RFC 9457).
- Reuse the client_id on retries so you never double-submit an order.
