---
name: Stream real-time market data
description: Subscribe to One Trading order book, price ticks and book ticker over WebSocket.
api: asyncapi/one-trading-streams-asyncapi.yml
ws_url: wss://streams.fast.onetrading.com
auth: none for public market data; AUTHENTICATE for private trading events
operations: [getInstruments, getOrderBook, getMarketTicker]
---

# Stream real-time market data

One Trading exposes a single multiplexed WebSocket at
`wss://streams.fast.onetrading.com`. Every message carries a `type`
discriminator.

## Steps

1. **Pick instruments.** Call `getInstruments` (`GET /v1/instruments`) over REST to
   get valid `instrument_code` values.

2. **(Optional) Seed a snapshot.** Fetch `getOrderBook`
   (`GET /v1/order-book/{instrument_code}`) and `getMarketTicker` over REST so you
   have a baseline before the stream starts.

3. **Connect and subscribe.** Open the WebSocket and send a `SUBSCRIBE` message for
   the channels you want:
   - `ORDER_BOOK_SNAPSHOT` + `ORDER_BOOK_UPDATE` — full book then incremental diffs.
   - `PRICE_TICK` — trade prints.
   - `BOOK_TICK` — best bid/ask.

4. **Keep alive.** Send `PING`; the server replies `PONG`.

5. **(Private) Authenticate for trading events.** To also receive `ORDER_BOOKED`,
   `ORDER_FULLY_FILLED`, `TRADE_EXECUTED`, `SETTLEMENT`, `FUNDING_PAYMENT`, and
   `BALANCE_ADJUSTMENT`, send `{"type":"AUTHENTICATE","api_token":"<token>"}` first
   (token needs the Trade permission). Success replies `{"type":"AUTHENTICATED"}`;
   failure replies `{"error":"AUTHENTICATION_FAILED"}`.

## Rules
- Apply `ORDER_BOOK_UPDATE` diffs on top of the last `ORDER_BOOK_SNAPSHOT`.
- Errors arrive as `{"error":"<CODE>"}`.
