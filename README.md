# Douglas Elliman (douglas-elliman)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
