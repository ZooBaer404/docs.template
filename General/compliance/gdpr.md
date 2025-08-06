<!--
START OF: gdpr.md
Purpose: Provides info on whether or how the project implements General Data Protection Regulation.
Update Frequency: Each time a new observation is discovered on GDPR.
Location: docs/compliance/gdpr.md
-->

# GDPR Compliance Summary

## What We Collect

- Email, name, usage logs
- Only stored with user consent (see onboarding flow)

## User Rights

- [X] Right to be forgotten → `DELETE /user/account`
- [X] Data export → `GET /user/data`

## Data Storage

- Encrypted at rest (AES-256)
- Retained for 90 days after deletion

> Contact `privacy@example.com` for GDPR requests.

<!-- END OF: gdpr.md -->
