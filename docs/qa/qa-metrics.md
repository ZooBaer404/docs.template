<!--
START OF: qa-metrics.md
Purpose: Track and report quality metrics to evaluate software health and QA effectiveness.
Update Frequency: Monthly or after major releases.
Location: docs/qa/qa-metrics.md
-->

# QA Metrics Dashboard

| Metric               | Description                                 | Target / Threshold | Current Status (Last Month) | Owner   |
|----------------------|---------------------------------------------|--------------------|-----------------------------|---------|
| Test Coverage        | % of code covered by automated tests        | ≥ 80%              | 75%                         | QA Lead |
| Defect Density       | Bugs per KLOC (thousand lines of code)      | ≤ 0.5              | 0.7                         | QA Lead |
| Bug Reopen Rate      | % of bugs reopened after being marked fixed | ≤ 5%               | 3%                          | QA Lead |
| Test Execution Rate  | % of planned tests executed                 | 100%               | 90%                         | QA Team |
| Critical Bugs Found  | Number of critical bugs found per release   | 0                  | 2                           | QA Team |
| Automation Pass Rate | % of automated tests passing                | ≥ 95%              | 98%                         | QA Team |

---

## Notes

- Use metrics to identify bottlenecks and areas needing improvement.
- Discuss metrics in sprint retrospectives and QA reviews.
- Always dig deeper if targets are not met.

---

> *Metrics don't lie, but they might hide when you ignore them.*

<!-- END OF: qa-metrics.md -->
