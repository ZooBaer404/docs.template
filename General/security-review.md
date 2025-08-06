<!--
START OF: security-review.md
Purpose: Provides a quick overview of the security of the app.
Update Frequency: Each time a security-related update takes place in the project.
Location: docs/security-review.md
-->

# Security Review

## Secure Coding Practices

- [x] Input validation (backend & frontend)
- [x] Output escaping (XSS protection)
- [x] JWT token integrity checks
- [x] Encrypted passwords (bcrypt)
- [ ] Rate-limiting sensitive endpoints

---

## Third-Party Audits

- `libcrypto.js` → CVE-free as of <2025-06-27 Fri>

<!-- END OF: security-review.md -->
