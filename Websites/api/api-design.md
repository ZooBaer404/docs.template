<!--
START OF: api-design.md
Purpose: Describe design decisions, versioning, and error conventions for the API.
Update Frequency: When APIs evolve or new principles adopted.
Location: docs/api/api-design.md
-->

# API Design Philosophy

REST with some brains.

---

## Principles

- **Versioning**: All endpoints use `/v1/` namespace.
- **Consistency**: JSON all the way. Same structure for success & error.
- **Statelessness**: Each request must contain all necessary info.

---

## Endpoint Format

```http
POST /api/v1/detect-plagiarism
Content-Type: application/json

{
  "assignment_id": "abc123",
  "student_id": "xyz789"
}
```

## Error Convention

```json
{
  "status": "error",
  "code": 403,
  "message": "Unauthorized access"
}
```

## Response Convention

```json
{
  "status": "success",
  "data": { ... }
}
```

> Full schema lives in [api/openapi.yaml] or [postman_collection.json]

<!-- END OF: api-design.md -->
