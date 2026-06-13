# The Trade Desk

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
