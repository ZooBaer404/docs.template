<!--
START OF: rate-limiting.md
Purpose: Define rate limits to prevent abuse and manage load.
Update Frequency: When throttling policies change.
Location: docs/api/rate-limiting.md
-->

# API Rate Limiting Policy

## Default Limits
| Type  | Limit    | Window      |
|-------|----------|-------------|
| User  | 1000 req | per 15 mins |
| IP    | 5000 req | per hour    |
| Token | 200 req  | per minute  |

## Throttling Response
```json
{
  "status": "error",
  "code": 429,
  "message": "Rate limit exceeded. Try again in 30 seconds."
}
```

## Best Practices

- Use retries with backoff.
- Cache results to avoid over-fetching.

<!-- END OF: rate-limiting.md -->
