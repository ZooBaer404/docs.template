<!--
START OF: request-format.md
Purpose: Define expected format and headers for all API requests.
Update Frequency: When request formats are modified.
Location: docs/api/request-format.md
-->

# Request Format

## Required Headers
```http
Content-Type: application/json
Authorization: Bearer <token>
```

## Common Request Format

```json
{
  "data": {
    "type": "user",
    "attributes": {
      "name": "Zubair",
      "email": "zubair@example.com"
    }
  }
}

```

## Special Considerations

- Use camelCase for keys.
- Timestamps must be in ISO 8601.

<!-- END OF: request-format.md -->
