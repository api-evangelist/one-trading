# One Trading

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

One Trading (One Trading Exchange B.V.) is an EU-regulated cryptocurrency and derivatives exchange for retail and institutional traders, positioning itself as "the world's fastest exchange." It offers spot crypto plus crypto futures (up to 10x leverage), index futures and 24/7 equity futures. Its public "Fast API" provides REST market-data and trading endpoints (currencies, instruments, order book, candlesticks, ticker, fees, funding rates, orders, trades, futures positions and subaccount transfers) at https://api.onetrading.com/fast, plus a real-time WebSocket streams API at wss://streams.fast.onetrading.com. Formerly operated as Bitpanda Pro. This profile was surfaced as a Speedinvest portfolio company and enriched by the API Evangelist pipeline from the provider's public documentation and live endpoints.

**Areas:** Company · Cryptocurrency · Cryptocurrency Exchange · Trading · Derivatives · Futures · Financial Services · Market Data · WebSocket · Fintech · Real-Time

## One Trading on APIs.io

Everything profiled for One Trading is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/one-trading/](https://apis.io/providers/one-trading/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [One Trading WebSocket Streams API](https://apis.io/apis/one-trading/one-trading-websocket-streams-api/) — Real-time WebSocket API for market data (order book, price ticks, book ticker) and, after authenticating, private trading events (order lifecycle, trades,…
- [One Trading Funding API](https://apis.io/apis/one-trading/one-trading-funding-api/) — Subaccount balance transfers
- [One Trading Futures API](https://apis.io/apis/one-trading/one-trading-futures-api/) — Futures positions, funding and portfolio endpoints
- [One Trading Public API](https://apis.io/apis/one-trading/one-trading-public-api/) — Public market-data endpoints (no authentication)
- [One Trading API](https://apis.io/apis/one-trading/one-trading-trading-api/) — Account order and trade endpoints (Bearer token, TRADE/READ scope)

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [One Trading WebSocket Streams API](https://apis.io/asyncapis/one-trading/one-trading-streams-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/](https://apis.io/channels/one-trading/untitled/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [one-trading](https://apis.io/servers/one-trading/one-trading/)

#### Collections (4)

Postman and Open Collection request collections.

- [One Trading Fast Funding API](https://apis.io/collections/one-trading/open-one-trading-funding-api/)
- [One Trading Fast Funding Futures API](https://apis.io/collections/one-trading/open-one-trading-futures-api/)
- [One Trading Fast Funding Public API](https://apis.io/collections/one-trading/open-one-trading-public-api/)
- [One Fast Funding Trading API](https://apis.io/collections/one-trading/open-one-trading-trading-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [One Trading Fast Overlay](https://apis.io/overlays/one-trading/one-trading-fast-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [One Trading Authentication](https://apis.io/security/one-trading/one-trading-authentication/)
- [One Trading Domain Security](https://apis.io/security/one-trading/one-trading-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://onetrading.com)
- [Documentation](https://docs.onetrading.com)
- [Getting started](https://support.onetrading.com/hc/en-gb/articles/16357722538129-What-should-I-know-about-One-Trading-API)
- [API reference](https://docs.onetrading.com/rest/public/currencies)
- [Pricing](https://onetrading.com/fees)
- [Support](https://support.onetrading.com/hc/en-gb)
- [Blog](https://onetrading.com/blog)
- [Terms of service](https://onetrading.com/terms)
- [Privacy policy](https://onetrading.com/privacy-policy)
- [GitHub](https://github.com/one-trading)

## API Evangelist rating

**Kin Score 32.4** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 23.9 |
| Contract governance | 4.5 |
| Operational transparency | 10.5 |
| Developer ergonomics | 49.4 |
| Access clarity | 38.2 |

**Agent readiness 28.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 23.1** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/one-trading/](https://apis.io/providers/one-trading/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for One Trading: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/one-trading/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
