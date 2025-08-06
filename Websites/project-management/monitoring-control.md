<!--
START OF: monitoring-control.md
Purpose: This document defines how project progress, quality, and risks will be monitored and controlled throughout the lifecycle.
It aligns with best practices described in "Software Project Management" by Bob Hughes et al.
Update Frequency: Update this document at the beginning of every major milestone and after key reviews (weekly, bi-weekly, etc.)
Location: docs/project-management/monitoring-control.md
-->

# Monitoring & Control Strategy

---

## Key Performance Indicators (KPIs)

| Metric               | Target Value     | Tool/Source                | Update Frequency |
|----------------------|------------------|----------------------------|------------------|
| Feature Completion % | 100% by deadline | Issue Tracker (e.g., Jira) | Weekly           |
| Bug Fix Rate         | ≥ 90%            | QA Reports                 | Per Sprint       |
| Deployment Frequency | ≥ 1/week         | CI/CD Logs                 | Weekly           |
| Build Success Rate   | ≥ 95%            | CI Pipeline                | Daily            |

---

## Escalation Criteria

If any of the following occur, the issue must be **escalated immediately**:

- KPIs drop below 70% for 2 consecutive sprints.
- Security vulnerabilities with CVSS score ≥ 8.
- Budget overrun projected > 20%.
- Stakeholder dissatisfaction flagged twice in feedback.

---

## Tools for Monitoring

| Tool               | Purpose                      | Owner/Operator |
|--------------------|------------------------------|----------------|
| Prometheus         | System metrics monitoring    | DevOps Team    |
| Grafana Dashboards | Visual analytics             | PM & Tech Lead |
| Sentry             | Error & exception tracking   | Backend Team   |
| GitHub Actions     | CI/CD status & build reports | Developers     |

---

## Change Control Process

> Changes happen. Let’s not panic. Let’s manage them like grownups.

| Step                      | Description                                                            |
|---------------------------|------------------------------------------------------------------------|
| 1. Change Request         | Logged by team or stakeholder in `change-requests.md`                  |
| 2. Impact Analysis        | Project Manager evaluates cost, time, risk                             |
| 3. Approval/Denial        | Decision by PM or Steering Committee (if major)                        |
| 4. Communication          | All stakeholders notified via `docs/meetings/README.md` or update memo |
| 5. Implementation         | Work item created, tracked under roadmap/issue tracker                 |
| 6. Post-change Monitoring | Review KPIs to ensure stabilization post-change                        |

---

## Monitoring Schedule

| Activity                 | Frequency | Owner        | Notes                    |
|--------------------------|-----------|--------------|--------------------------|
| Sprint Review            | Bi-weekly | Scrum Master | Track progress, blockers |
| Burndown Chart Update    | Weekly    | PM           | Auto-generated preferred |
| Stand-up Summaries       | Daily     | All teams    | Optional doc updates     |
| Budget & Resource Review | Monthly   | Finance + PM | Part of Steering Reports |


## Historical Monitoring Records

| Review Date      | Reviewed By  | Summary of Findings              | Actions Taken               |
|------------------|--------------|----------------------------------|-----------------------------|
| <2025-06-27 Fri> | PM, Dev Lead | API performance lagging by 300ms | Refactored DB calls         |
| <2025-06-27 Fri> | QA Team      | Test coverage dropped to 60%     | Wrote 12 missing unit tests |
| <2025-06-27 Fri> | DevOps       | CI build failure rate > 10%      | Added pre-commit            |

---

### Risk Control

Risks will be:
- Reviewed bi-weekly using the [risk-management.md](risk-management.md)
- Assigned an owner via [roles-and-assignees.md](roles-and-assignees.md)
- Escalated if severity increases beyond threshold

---

## Reporting

| Report Name      | Owner           | Frequency   | Distribution Method |
|------------------|-----------------|-------------|---------------------|
| Status Report    | Project Manager | Weekly      | Email, Teams        |
| Sprint Report    | Scrum Master    | Bi-weekly   | Jira, Notion        |
| QA Summary       | QA Lead         | Per release | GitHub Wiki         |
| Financial Report | Project Manager | Monthly     | Excel Sheet, PDF    |

---

## Responsibilities

- **Project Manager**: Overall monitoring, reporting, and escalation
- **Team Leads**: Task-level tracking and technical control
- **QA Lead**: Quality metrics and testing coverage
- **Product Owner**: Scope and feature readiness control

---

## Tools Used

- Jira / GitHub Projects
- Excel / Google Sheets
- Slack / Teams
- Jenkins / GitHub Actions (for CI/CD monitoring)
- Grafana (for real-time metrics, if infra involved)

---

## References

- [roles-and-assignees.md](roles-and-assignees.md)
- [risk-management.md](risk-management.md)
- [milestones.md](milestones.md)

<!-- END OF monitoring-control.md -->
