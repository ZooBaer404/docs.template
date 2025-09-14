<!--
START OF: env-validator.md
Purpose: Documents the internal tool used to validate required environment variables.
Update Frequency: Update whenever a new required environment variable is added/changed/removed.
Location: docs/internal-tools/env-validator.md
-->

# Environment Validator

## Overview
This tool checks for the presence and correctness of all required environment variables. It's especially useful before deployments and during CI runs.

---

## Setup

```bash
# Example: Node.js-based validator
npm install
node env-validator.js
```

---

## Expected Variables

| Variable Name  | Description                   | Required | Default |
|----------------|-------------------------------|----------|---------|
| `DATABASE_URL` | Connection string for main DB | yes      | N/A     |
| `JWT_SECRET`   | Secret key for token signing  | yes      | N/A     |
| `LOG_LEVEL`    | Application log level         | no       | `info`  |

---

## Output Example

[ERROR] Missing required variable: DATABASE_URL
[OK] LOG_LEVEL = info

---

## Maintainer Notes

- Configurations are pulled from .env.example
- Extend the tool to check types and ranges if needed

<!-- END OF: env-validator.md -->
