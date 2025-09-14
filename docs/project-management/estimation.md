<!--
START OF: estimation.md
Purpose: This document provides a detailed outline of estimation techniques used for cost, effort, and time in the project.
Based on principles from Software Project Management by Bob Hughes et al.
Update Frequency: Whenever a major estimation is performed or recalibrated during planning or re-planning phases.
Location: docs/project-management/estimation.md
-->


# Project Estimation

---

## Time Breakdown Table

Module-wise or task-wise breakdown (include diagrams or Gantt chart if needed).

| Task/Feature        | Estimated Time (hrs) | Allocated Time (hrs) | Start Date       | End Date         |
|---------------------|----------------------|----------------------|------------------|------------------|
| Authentication Flow | 30                   | 35                   | <2025-06-27 Fri> | <2025-07-02 Wed> |
| UI Prototype Design | 20                   | 25                   | <2025-06-27 Fri> | <2025-06-28 Sat> |
| API Rate Limiting   | 15                   | 20                   | <2025-06-27 Fri> | <2025-06-27 Fri> |
| Bug Fixing Sprint 1 | 10                   | 15                   | <2025-06-27 Fri> | <2025-06-29 Sun> |

---

## Effort Estimate

In person-hours or person-months. Mention the allocation of devs, testers, PMs.


| Feature/Module   | Estimated Effort (hrs) | Actual Effort (hrs) | Variance |
|------------------|------------------------|---------------------|----------|
| Auth System      | 40                     | 48                  | +8       |
| API Gateway      | 50                     | 44                  | -6       |
| DB Schema Design | 35                     | 32                  | -3       |

---

## Cost Estimate

Use effort × hourly/daily rate. Include hardware, cloud, licenses, and hidden costs.

| Module/Phase        | Est. Cost (\$) | Actual Cost (\$) | Variance (\$) | Justification                  |
|---------------------|----------------|------------------|---------------|--------------------------------|
| Backend Development | 1200           | 1300             | +100          | Extra effort due to DB rewrite |
| UI/UX Design        | 800            | 800              | 0             | Within planned hours           |
| Testing & QA        | 600            | 500              | -100          | Automated test reuse           |
| DevOps Setup        | 1000           | 1100             | +100          | Unexpected infra change        |

---

## Buffer Allocation Table

Add a % for unknowns, e.g., "15% contingency".

| Phase/Task           | Base Estimate (hrs) | Buffer % | Buffer Time (hrs) | Final Allocated Time (hrs) |
|----------------------|---------------------|----------|-------------------|----------------------------|
| Core Feature Dev     | 80                  | 20%      | 16                | 96                         |
| Infrastructure Setup | 50                  | 10%      | 5                 | 55                         |
| Testing Cycle        | 40                  | 15%      | 6                 | 46                         |
| Code Review & Merge  | 25                  | 25%      | 6.25              | 31.25                      |


---

## Review Process Table

Mention estimation review meetings or peer reviews.

| Item                | Reviewed By      | Review Date      | Type of Review   | Notes                    |
|---------------------|------------------|------------------|------------------|--------------------------|
| Architecture Doc    | Tech Lead        | <2025-06-27 Fri> | Technical        | Approved, minor edits    |
| Feature Estimations | PM & Dev Lead    | <2025-06-28 Sat> | Estimation Check | Adjusted API timeline    |
| UI Mockups          | Product Owner    | <2025-06-29 Sun> | Design Review    | Color tweaks recommended |
| Deployment Strategy | DevOps & QA Lead | <2025-06-30 Mon> | Risk Review      | Add rollback steps       |

---

## Notes

- Round all time to the nearest 2 hours for planning simplicity
- Use confidence intervals (best, worst, most likely) for risky components

---

## References

- [milestones.md](milestones.md)
- [design-decision.md](design-decision.md)
- [Project Management](README.md)

<!-- END OF: estimation.md -->
