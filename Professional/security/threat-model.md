<!--
START OF: threat-model.md
Purpose: Provide a model for thread analysis.
Update Frequency: Each time a new threat model is found.
Location: docs/security/threat-model
-->

# Threat Model

## Attack Surfaces

| Vector        | Risk              | Mitigation                      |
|---------------|-------------------|---------------------------------|
| XSS in forms  | High              | Escaped output & CSP headers    |
| SQL Injection | Medium (ORM used) | Query builders, strict schemas  |
| DDoS on API   | High              | Rate-limiting + caching         |
| CSRF          | Low               | SameSite cookies + token checks |

---

## Worst-Case Scenarios

> If attacker gets DB access → no plaintext passwords, thanks bcrypt.

<!-- END OF: threat-model.md -->
