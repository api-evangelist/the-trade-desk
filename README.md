# The Trade Desk

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

The Trade Desk is a global programmatic advertising platform and demand-side platform (DSP) that enables advertisers, agencies, and media buyers to plan, manage, and optimize digital advertising campaigns across connected TV, display, video, audio, native, and mobile channels. The platform provides REST and GraphQL APIs for managing advertisers, campaigns, ad groups, creatives, targeting, bidding strategies, audience data segments, and campaign performance reporting at scale.

**Website:** https://www.thetradedesk.com  
**Partner Portal:** https://partner.thetradedesk.com  
**Enterprise APIs:** https://www.thetradedesk.com/us/our-platform/enterprise-apis  
**GitHub:** https://github.com/thetradedesk  

## APIs

- **Platform API (REST + GraphQL)** — Campaign, ad group, creative, and advertiser management; bid lists; frequency caps; activity logs
- **Data API** — Audience segment management, CRM data uploads, third-party data integration, commerce solutions
- **Real-Time Conversions API** — Server-side conversion event ingestion for attribution and measurement
- **Reporting API** — Campaign performance data with 200+ metrics and dimensions

## Base URL

```
https://api.thetradedesk.com/v3
```

## Authentication

Token-based authentication via POST to `/v3/authentication`. The token is passed in subsequent requests using the `TTD-Auth` header. Tokens expire and must be refreshed on 401 responses. Long-lived tokens can also be generated at https://partner.thetradedesk.com/v3/portal/tokens.

## Access

API access requires an existing Trade Desk seat or partner agreement. Access is provisioned by a TTD account representative and is not available for self-serve registration.

## Resources

- [plans/plans.md](plans/plans.md) — Access model and API tier details
- [rate-limits/rate-limits.md](rate-limits/rate-limits.md) — Rate limit guidance and best practices
- [finops/finops.md](finops/finops.md) — Cost structure and optimization strategies
- [apis.yml](apis.yml) — APIs.json 0.19 provider catalog
