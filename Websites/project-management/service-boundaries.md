<!--
START OF: service-boundaries.md
Purpose: Define which components own which responsibilities in a modular/microservice setup.
Update Frequency: When service responsibilities shift or are refactored.
Location: docs/project-management/service-boundaries.md
-->

# Service Boundaries

---

## Core Services

| Service              | Responsibility                     |
|----------------------|------------------------------------|
| `plagiarism-core`    | Handles detection logic, ML models |
| `user-management`    | Registration, login, roles         |
| `submission-service` | File uploads, pre-processing       |
| `report-service`     | Generates plagiarism reports       |

---

## Don’t Cross These Lines

- `submission-service` should *not* talk directly to `user-management`. It gets only an ID via the token.
- `report-service` consumes data via an internal API — not DB peeking.

---

>  Add new services here when they’re born, not after they grow up and go rogue.

<!-- END OF: service-boundaries.md -->
