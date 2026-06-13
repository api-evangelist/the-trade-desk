# The Trade Desk API FinOps

## Overview

The Trade Desk operates as an enterprise demand-side platform (DSP) where API access costs are layered on top of media spend and platform fees. There is no publicly advertised API pricing — all costs are negotiated through account management as part of a commercial agreement.

## Cost Structure

### Platform Spend
The Trade Desk earns revenue primarily as a percentage of media spend flowing through the platform. Advertisers pay for:
- CPM (cost per thousand impressions) on purchased inventory
- Data segment fees when activating third-party audience data
- Technology fees as a percentage of spend

### API Enablement Fees
Practitioner reports indicate API access may carry:
- **One-time enablement fee** for activating API access on an account
- **Recurring monthly API fees** in addition to standard platform spend
- Specific amounts are not publicly disclosed and vary by account size and usage

### Additional Fees Documentation
The Trade Desk documents additional fees for API usage at:
https://partner.thetradedesk.com/v3/portal/api/area/Additional%20Fees

### Third-Party Data Rates
When using third-party audience data through the Data API, data segment fees are charged per impression. Rates vary by data provider and data type and are documented at:
https://partner.thetradedesk.com/v3/portal/data/doc/DataRatesOverview

## Cost Optimization Strategies

### Minimize API Call Volume
- Use incremental/delta sync patterns for reporting (only pull changed data)
- Cache authentication tokens; do not re-authenticate per request
- Use GraphQL to retrieve only required fields rather than full resource representations
- Batch operations where supported to reduce total request count

### Reporting Efficiency
- Align reporting sync frequency to business needs (3-hour default vs. 15-minute high-frequency)
- High-frequency reporting syncs may increase API consumption; use only where real-time decisions justify it
- Request specific metrics and dimensions rather than full data dumps

### Audience Data Management
- Plan segment uploads carefully to stay above the 1,500-user minimum threshold
- Batch contact list uploads to maximize efficiency of signed S3 URL generation
- Monitor third-party data segment activation costs against campaign ROI

### Monitoring Spend
- The Trade Desk platform provides campaign-level spend reporting accessible via the Reporting API
- Integrate reporting data into internal FinOps dashboards to track API-driven campaign spend versus manual campaign spend
- Set budget caps at the campaign and ad group level via Platform API to prevent overspend

## Enterprise Integrations That May Affect Cost

- **Snowflake Connector App** — may involve Snowflake compute costs in addition to TTD fees
- **Audience Unlimited** — extended data activation may carry additional data fees
- **OpenSincera** — transparent data from 300,000+ publishers; data costs apply based on data used

## Financial Reporting Context

The Trade Desk (NASDAQ: TTD) reported Q1 2026 revenue of $689 million (+12% YoY), reflecting the scale of the platform. Enterprise customers represent the majority of this spend.

## Negotiation Points

When negotiating API access with your TTD account team, consider:
- Total committed media spend on the platform
- API use case scope (read-only reporting vs. full campaign management)
- Number of advertiser seats requiring API access
- Integration volume (number of API calls per day/month)
- SCIM / user management needs (enterprise contract required)

## Contact

For pricing and FinOps planning, contact your Trade Desk account representative through:
- **Enterprise APIs:** https://www.thetradedesk.com/us/our-platform/enterprise-apis
- **Partner Portal:** https://partner.thetradedesk.com
