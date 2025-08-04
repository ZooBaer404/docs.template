<!--
START OF: risk-management.md
Purpose: This document outlines the risk identification, analysis, mitigation, and review processes across the project lifecycle. It is aligned with the methodology described in "Software Project Management" by Bob Hughes, Mike Cotterell, and Rajib Mall.
Update Frequency: Reviewed bi-weekly during sprint planning, milestone evaluations, or if any critical risk arises.
Location: docs/project-management/risk-management.md
-->

# Risk Management Strategy

---

## Risk Identification

> "If it has failed in someone else's project, it can fail in yours too. Learn, don't guess."

| Risk ID | Category    | Description                     | Likelihood | Impact   | Owner         |
|---------|-------------|---------------------------------|------------|----------|---------------|
| RSK-001 | Technical   | Third-party API deprecation     | High       | High     | Backend Lead  |
| RSK-002 | Financial   | Budget cut from stakeholders    | Medium     | High     | PM            |
| RSK-003 | Resource    | Key developer unavailability    | High       | Medium   | HR / PM       |
| RSK-004 | Scope Creep | Last-minute feature addition    | Medium     | High     | Product Owner |
| RSK-005 | Security    | Credential leak via Git commits | Low        | Critical | DevOps        |

---

## Risk Analysis Matrix

| Likelihood → / Impact ↓ | Low      | Medium   | High             | Critical         |
|-------------------------|----------|----------|------------------|------------------|
| Low                     | Ignore   | Monitor  | Monitor          | Escalate         |
| Medium                  | Monitor  | Mitigate | Escalate         | Escalate         |
| High                    | Escalate | Escalate | Immediate Action | Immediate Action |

---

## Mitigation Strategies

| Risk ID | Mitigation Plan                                                                   | Status      |
|---------|-----------------------------------------------------------------------------------|-------------|
| RSK-001 | Monitor API deprecation notices; implement abstraction layer                      | In Progress |
| RSK-002 | Define MVP scope early, prioritize features, have stakeholder checkpoints         | Planned     |
| RSK-003 | Cross-train team members, maintain redundancy                                     | In Progress |
| RSK-004 | Strict change-control policy (see [monitoring-control.md](monitoring-control.md)) | Enforced    |
| RSK-005 | Use Git hooks + secret scanners; enforce `.env` policy                            | Enforced    |

---

## Historical Risk Reviews

| Date             | Reviewed By     | New Risks Found | Major Updates Made                           |
|------------------|-----------------|-----------------|----------------------------------------------|
| <2025-06-27 Fri> | PM + Tech Leads | RSK-004 added   | Change control tightened                     |
| <2025-06-27 Fri> | Security Lead   | RSK-005 added   | Secret scanning integrated with CI           |
| <2025-06-27 Fri> | PM, QA, DevOps  | No new risks    | RSK-001 mitigation started (API abstraction) |

---

## Responsibilities

- **Project Manager**: Overall risk documentation, tracking, escalation.
- **Team Leads**: Identify and log technical/operational risks.
- **QA Lead**: Report recurring defects as project risks.
- **Product Owner**: Control scope creep and stakeholder expectation risks.
- **Security Officer** *(if exists)*: Monitor vulnerabilities, enforce response.

---

## Key Risk Indicators (KRIs)

| Indicator Name         | Description                            | Threshold          | Tool                     |
|------------------------|----------------------------------------|--------------------|--------------------------|
| API Failure Rate       | Frequency of 3rd-party API errors      | > 3% requests fail | Logs / Postman Monitors  |
| Scope Change Frequency | No. of new feature requests mid-sprint | > 2 per sprint     | Jira / Roadmap logs      |
| Build Breakage Rate    | % failed CI/CD builds                  | > 15% per week     | GitHub Actions / Jenkins |
| Team Availability      | # of critical staff unavailable        | > 2 per week       | HR Calendar              |

---

## Risk Review Process

> “Plan for risk. If it doesn’t show up — great. If it does — you’re not screwed.”

| Step                 | Description                                                 |
|----------------------|-------------------------------------------------------------|
| 1. Identification    | Risks logged in `risk-register.md` by any contributor       |
| 2. Classification    | Categorized by likelihood and impact                        |
| 3. Response Planning | Mitigation, contingency, and communication steps drafted    |
| 4. Monitoring        | KPIs and KRIs tracked (see above)                           |
| 5. Escalation        | Triggered based on matrix or owner recommendation           |
| 6. Retrospective     | Add to [lessons-learned.md](lessons-learned.md) if critical |

---

## References

- [monitoring-control.md](monitoring-control.md)
- [roles-and-assignees.md](roles-and-assignees.md)
- [closure.md](closure.md)
- [risk-register.md](risk-register.md)

<!-- END OF risk-management.md -->
