<!--
START OF: response-format.md
Purpose: Standardize all API responses for clients.
Update Frequency: When structure or keys change.
Location: docs/api/response-format.md
-->

# Response Format

## Success Response
```json
{
  "status": "success",
  "data": { /* resource object */ }
}
```

## Error Response

```json
{
  "status": "error",
  "message": "Invalid credentials"
}
```

## Meta & Pagination

```json
{
  "meta": {
    "page": 1,
    "per_page": 10,
    "total": 100
  }
}
```

<!-- END OF: response-format.md -->
