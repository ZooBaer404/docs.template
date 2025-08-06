<!--
START OF: quality-management.md
Purpose: This document outlines the processes and standards for ensuring software quality during the project lifecycle. It aligns with industry QA practices and draws from "Software Project Management" by Bob Hughes et al.
Update Frequency: Update this document at the start of each sprint and after major test cycles or reviews.
Location: docs/project-management/quality-management.md
-->

# Quality Management Plan

---

## Quality Metrics

| Metric                   | Target Value    | Tool/Source           | Review Cycle |
|--------------------------|-----------------|-----------------------|--------------|
| Unit Test Coverage       | ≥ 85%           | Jest / NUnit / Pytest | Per Sprint   |
| Integration Success Rate | ≥ 95%           | CI/CD Logs            | Weekly       |
| Defect Density           | < 0.8/KLOC      | QA Reports            | Per Release  |
| Mean Time to Resolve Bug | < 48 hours      | Issue Tracker         | Weekly       |
| Regression Count         | ≤ 2 per release | Manual/Auto Tests     | Per Sprint   |

---

## Quality Assurance Activities

| Activity                   | Description                                  | Frequency      |
|----------------------------|----------------------------------------------|----------------|
| Code Reviews               | Peer-reviewed for logic, security, standards | Every PR       |
| Static Code Analysis       | Automated linting and style checks           | CI Pipeline    |
| Manual Testing             | Exploratory and edge-case verification       | Pre-release    |
| Automated Testing          | Unit, integration, E2E via test suite        | Continuous     |
| Regression Testing         | Ensures no old features are broken           | Per Sprint     |
| Load & Performance Testing | Stress-test under simulated real-world usage | Pre-deployment |

---

## Tools Used

- ESLint, StyleCop, Pylint (code standards)
- Jest / NUnit / JUnit (unit testing)
- Postman / Newman / Cypress (API/E2E testing)
- SonarQube (static analysis)
- GitHub Actions / Jenkins (CI)
- Jira / GitHub Projects (QA tracking)

---

## Acceptance Criteria

> "If it ain’t passing these, it ain’t shippin’."

1. All unit and integration tests pass with target coverage.
2. No critical or high-severity bugs remain unresolved.
3. Functionality matches signed-off feature specs.
4. Performance meets non-functional requirements.
5. All deliverables approved by QA lead and Product Owner.

---

## Roles & Responsibilities

| Role           | Responsibility                                   |
|----------------|--------------------------------------------------|
| QA Lead        | Owns QA process and defines test strategy        |
| Developers     | Write and maintain unit tests; fix reported bugs |
| Test Engineers | Execute manual and automated test cases          |
| PM             | Ensures quality is aligned with timeline/scope   |
| Product Owner  | Final acceptance of feature readiness            |

---

## Continuous Improvement

- Retrospectives after each sprint to identify QA gaps
- Periodic audits of test effectiveness
- Bug root cause analysis (RCA) for high-severity issues

---

## Historical QA Records

| Date             | Reviewed By | QA Activity        | Key Findings                           | Actions Taken          |
|------------------|-------------|--------------------|----------------------------------------|------------------------|
| <2025-06-27 Fri> | QA Lead     | Regression Testing | 3 legacy functions broke               | Added regression suite |
| <2025-06-27 Fri> | Dev + QA    | Unit Test Review   | Coverage dropped to 76% in module X    | Added 5 test cases     |
| <2025-06-27 Fri> | QA Team     | Load Testing       | API failed under 1000 concurrent users | Optimized DB queries   |

---

## References

- [test-plan.md](../qa/test-plan.md)
- [manual-tests.md](../qa/manual-tests.md)
- [roles-and-assignees.md](roles-and-assignees.md)
- [risk-management.md](risk-management.md)

<!-- END OF quality-management.md -->
