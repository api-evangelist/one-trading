---
name: Monitor and manage a futures portfolio
description: Read One Trading futures positions, portfolio equity/margin and funding payments.
api: openapi/one-trading-fast-openapi.yml
base_url: https://api.onetrading.com/fast
auth: Bearer API token with the READ scope
operations: [getFuturesSummary, getFuturesOpenPositions, getCurrentFundingRate, getFuturesFundingPayments]
---

# Monitor and manage a futures portfolio

One Trading offers crypto, index and equity futures. Funding on perpetual/futures
instruments is recalculated every minute and settled every 4 hours (00:00, 04:00,
08:00, 12:00, 16:00, 20:00 UTC).

## Steps

1. **Portfolio summary.** Call `getFuturesSummary`
   (`GET /v1/account/futures/summary`) for real-time equity, margin and position
   totals (updated every minute).

2. **Open positions.** Call `getFuturesOpenPositions`
   (`GET /v1/account/futures/positions`) for size, direction, entry price and
   realised PnL per position.

3. **Funding cost.** Call `getCurrentFundingRate`
   (`GET /v1/funding-rate`, public) for the current preliminary rate, and
   `getFuturesFundingPayments` (`GET /v1/account/futures/funding-payments`) for the
   funding cashflows already applied (paginated, sorted descending by timestamp,
   optionally filtered by `instrument_code`).

4. **History.** Use `GET /v1/account/futures/positions-history` for closed
   positions in a date range, and
   `GET /v1/account/futures/positions/{position_id}/funding-payments` for a single
   position's funding history.

## Rules
- Numeric values are decimal strings.
- A negative `funding_rate` means shorts pay longs; positive means longs pay shorts.
