# Douglas Elliman (douglas-elliman)

Douglas Elliman Inc. (NYSE: DOUG) is a residential real estate brokerage founded in 1911 and headquartered at 575 Madison Avenue, New York City. It is one of the largest brokerages in the New York metropolitan area and among the largest in the United States, with roughly 6,000 agents across New York, Florida, California, Texas, Colorado, Massachusetts, Connecticut, Nevada, New Jersey, Vermont, the Mid-Atlantic, and international outposts in France and Monaco. Its home market is the United States. In the value chain Douglas Elliman sits on the SELL side as a licensed brokerage and MLS participant — it consumes MLS listing data under IDX and broker agreements rather than originating a syndicated feed — and it extends into development marketing, property management, commercial brokerage, title and escrow (Douglas Elliman Title), relocation, and PropTech venture investment through New Valley Ventures. Its API posture is honest and thin: no developer portal, no published API documentation, no OpenAPI or OData `$metadata` contract, and no published access path of any kind.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/douglas-elliman/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/douglas-elliman/refs/heads/main/apis.yml)

## Tags

- Real Estate
- United States
- Brokerage
- Property Listings
- MLS
- IDX
- RESO
- Rentals
- Commercial Real Estate
- Property Management
- Title
- Escrow
- PropTech
- Luxury Real Estate
- New Development

## Timestamps

- **Created:** 2026-07-26
- **Modified:** 2026-07-26

## APIs

No public, documented APIs are published by Douglas Elliman. The `apis` collection in `apis.yml` is intentionally empty.

## RESO Posture

**RESO member — not RESO certified.**

- "Douglas Elliman Real Estate" appears on the [RESO membership roster](https://www.reso.org/membership/) under Class D Members (Brokers, Agents and Appraisers).
- It does **not** appear in the [RESO certified-organizations directory](https://www.reso.org/certificates/) — a case-insensitive search of the full 416 KB response returned zero matches.
- No RESO Web API certification, no Data Dictionary certification, no RESO Common Format, no Universal Property Identifier (UPI), and no OData `$metadata` document is served.
- The only RESO/RETS-adjacent public artifact is a **fork** of a third-party .NET RETS client library — [`DouglasElliman/RetsConnector`](https://github.com/DouglasElliman/RetsConnector) — which is consumer-side evidence that Elliman pulls MLS data in, not producer-side evidence of anything it exposes.

Membership is a trade-association status. Certification is a tested conformance status. Douglas Elliman holds only the former, and neither one would produce a reachable endpoint here.

## Access Gate

**`none-published`.** There is no developer program, no data-licence page, no IDX/VOW request form, no partner API page, and no API terms. A developer wanting Douglas Elliman listing data does not obtain it from Douglas Elliman — the gate sits one layer upstream at the MLS, and requires joining the relevant MLS or board, signing that MLS's IDX or VOW agreement, or buying a reseller feed (Bridge, Trestle, MLS Grid, Spark).

## Open Data

**None.** No open, unlicensed, publicly callable dataset exists. The Douglas Elliman Market Reports and Research Reports are human-readable publications, not data APIs.

## Auth Model

**None published.** `https://www.elliman.com/.well-known/openid-configuration` returned HTTP 404 when fetched anonymously. No API key issuance, no OAuth2, no OIDC discovery. The agent login is a member web login, not a developer credential path.

## Notable Probes

| URL | Status | Note |
| --- | --- | --- |
| `https://www.elliman.com/` | 200 | Consumer marketing and property search site |
| `https://developer.elliman.com/` | 200 | **False positive** — wildcard catch-all to www, not a portal |
| `https://developers.elliman.com/` | 200 | **False positive** — wildcard catch-all to www, not a portal |
| `https://docs.elliman.com/` | 200 | **False positive** — wildcard catch-all to www, not a portal |
| `https://api.elliman.com/` | 403 | Real IIS/ASP.NET host, forbidden, undocumented |
| `https://api.elliman.com/$metadata` | 404 | No OData/RESO metadata |
| `https://www.elliman.com/openapi.json` | 404 | No OpenAPI |
| `https://www.elliman.com/swagger.json` | 404 | No Swagger |
| `https://www.elliman.com/.well-known/openid-configuration` | 404 | No OIDC discovery |
| `https://www.elliman.com/robots.txt` | 200 | 12 XML sitemap indexes; no API paths |

Full probe log, with HTTP status for every URL, is recorded in [`review.yml`](review.yml).

## Common Properties

- [Website](https://www.elliman.com/)
- [About](https://www.elliman.com/about-us)
- [Investor Relations](https://investors.elliman.com/)
- [Terms of Service](https://www.elliman.com/terms-of-service)
- [Privacy Policy](https://www.elliman.com/privacy-policy)
- [Site Map](https://www.elliman.com/site-map)
- [Press](https://www.elliman.com/press-news)
- [Careers](https://www.elliman.com/careers)
- [Market Reports](https://www.elliman.com/corporate-resources/market-reports)
- [Research Reports](https://www.elliman.com/corporate-resources/research-reports)
- [Guides](https://www.elliman.com/sellers-buyers-renters-guides)
- [GitHub Organization](https://github.com/DouglasElliman)
- [LinkedIn](https://www.linkedin.com/company/douglaselliman/)

## Maintainers

- Kin Lane — kin@apievangelist.com
