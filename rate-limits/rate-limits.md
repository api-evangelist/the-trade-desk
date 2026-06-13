# The Trade Desk API Rate Limits

## Overview

The Trade Desk API enforces rate limits on a per-partner and per-advertiser account basis. Specific numeric thresholds are not publicly disclosed and are determined by your agreement with The Trade Desk. Partners should contact their TTD account manager for partner-specific rate limit details.

**Official Rate Limits Documentation:** https://partner.thetradedesk.com/v3/portal/api/doc/RateLimits

## General Behavior

- Rate limits are scoped per partner/advertiser account, not globally across all API consumers
- When a rate limit is exceeded, the API returns an HTTP 429 Too Many Requests response
- Retry logic with exponential backoff is recommended for production integrations

## Authentication Token Management

- Tokens expire and must be refreshed by re-authenticating via POST to `/v3/authentication`
- When a 401 Unauthorized response is received, re-authenticate and retry the original request
- Tokens should be cached and reused across requests rather than generated per request

## Pagination

- The API uses offset-based pagination
- Maximum page size: **100 records** per request
- Clients should paginate through large result sets rather than requesting all records in a single call

## Reporting Sync Frequency

- Standard reporting data sync: **3-hour increments**
- High-frequency refresh option: **15-minute cycles** (availability may vary by account)
- Incremental sync pattern recommended — only request changed data since last sync timestamp

## Audience Data Upload Limits

- Minimum unique users per segment: **1,500**
- Recommended maximum records per upload: **500 million**
- Contact list uploads are performed via signed S3 URLs (not directly through the API rate limit pool)

## Webhook Availability

- Webhooks are **not available** in The Trade Desk Platform API
- Clients must use polling patterns (e.g., periodic POST to `/v3/user/query`) to detect changes
- Plan polling intervals carefully to avoid hitting rate limits

## Best Practices

1. Cache authentication tokens and refresh only on 401 responses
2. Implement exponential backoff with jitter for 429 responses
3. Use incremental/delta sync patterns for reporting to reduce call volume
4. Batch operations where the API supports it rather than making individual per-resource calls
5. Use the GraphQL API for complex queries that would otherwise require multiple REST roundtrips
6. Contact your TTD account manager to understand your specific rate limit allocation

## Third-Party Rate Limit Management

Third-party integration platforms (e.g., Improvado) report that The Trade Desk API rate limits are manageable with proper request queuing and retry logic built into integration workflows.
