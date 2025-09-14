<!--
START OF: error-handling.md
Purpose: Document error codes, messages, and client expectations.
Update Frequency: When error responses are updated.
Location: docs/api/error-handling.md
-->

# API Error Handling Guide

## Error Structure
```json
{
  "status": "error",
  "code": 401,
  "message": "Unauthorized"
}
```


## Common HTTP Errors

| Code | Meaning             | Description                    |
|------|---------------------|--------------------------------|
| 400  | Bad Request         | Invalid data format            |
| 401  | Unauthorized        | Missing or invalid token       |
| 403  | Forbidden           | Access denied                  |
| 404  | Not Found           | Resource does not exist        |
| 500  | Internal Server Err | Something went boom on our end |

<!-- END OF: error-handling.md -->
