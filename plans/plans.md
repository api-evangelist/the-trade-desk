# The Trade Desk API Plans

## Access Model

The Trade Desk API does not offer self-serve public access. All API access is gated through an existing commercial relationship with The Trade Desk and must be provisioned by a TTD account representative.

## Requirements for API Access

- Active Trade Desk seat or partner agreement
- Explicit API enablement by your TTD account team
- API-specific credentials issued separately from platform login credentials
- Contractual agreement covering API usage terms

## Partner Portal Access

Once provisioned, partners access documentation and token generation at:
- **Partner Portal:** https://partner.thetradedesk.com
- **Token Generation:** https://partner.thetradedesk.com/v3/portal/tokens

## API Tiers

### Platform API (REST + GraphQL)
- Full campaign management: advertisers, campaigns, ad groups, creatives, bid lists
- Frequency cap configuration
- Activity logging
- GraphQL access for campaign creation and management
- Requires partner enablement

### Data API
- Audience segment creation and management
- First-party CRM data uploads (email/phone hashing via SHA-256)
- Third-party data integration
- Commerce solutions API access
- Data rate visibility

### Reporting API
- 200+ metrics and dimensions
- Campaign, ad group, ad, and creative performance
- Incremental sync (only changed data)
- 3-hour sync increments with 15-minute refresh availability

### Real-Time Conversions API
- Server-side conversion event ingestion
- Cross-device attribution
- Unified ID 2.0 compatibility

### SCIM / User Management
- SCIM 2.0 support available at enterprise tier only
- Requires custom contract negotiation through account management
- Standard user management available via REST API

## Pricing

Pricing is not publicly advertised. API enablement may carry:
- One-time enablement fees (reported by practitioners)
- Recurring monthly API costs on top of existing platform spend
- Additional fees documented at: https://partner.thetradedesk.com/v3/portal/api/area/Additional%20Fees

Contact your Trade Desk account manager for partner-specific pricing details.

## Data Limits

- Audience segment uploads: minimum 1,500 unique users
- Maximum 500 million records per upload (recommended)
- Pagination: maximum page size of 100 records per request

## Enterprise Integrations

- **Snowflake Connector App** — direct data pipeline integration
- **Audience Unlimited** — scaled data activation across stakeholders
- **OpenPass** — email-based sign-on (48-hour deployment)
- **OpenSincera** — transparent publisher data access (300,000+ publishers)
- **Unified ID 2.0** — identity resolution standard
