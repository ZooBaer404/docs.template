<!--
START OF: resource-management.md
Purpose: This document defines how human, technical, and financial resources will be planned, allocated, tracked, and optimized throughout the project.
Update Frequency: Update this document during project planning and revise quarterly or when major shifts occur.
Location: docs/project-management/resource-management.md
-->

# Resource Management Plan

---

## Human Resource Allocation

| Team Member | Role              | Assigned Tasks             | % Allocation | Backup       |
|-------------|-------------------|----------------------------|--------------|--------------|
| A. Rahmani  | Frontend Dev      | UI Implementation, Reviews | 80%          | B. Faizi     |
| L. Hamdard  | QA Lead           | Manual/Auto Tests, Reviews | 100%         | TBA          |
| Z. Khanzada | DevOps Engineer   | CI/CD, Monitoring Setup    | 60%          | N. Kohistani |
| S. Faqiri   | Backend Developer | API Design & Integration   | 100%         | K. Yousufi   |
| N. Popal    | PM                | Coordination, Reporting    | 100%         | None         |

---

## Infrastructure & Tooling Resources

| Resource/Tool      | Purpose                     | Owner      | License/Cost         | Renewal Date |
|--------------------|-----------------------------|------------|----------------------|--------------|
| GitHub Enterprise  | Source Control + CI/CD      | Dev Team   | $XX/month            | 2026-01-01   |
| Jira               | Project & Issue Tracking    | PM         | $YY/month            | 2026-01-01   |
| Postman Pro        | API Testing                 | QA Team    | $ZZ/year             | 2026-03-15   |
| AWS EC2 (t3.large) | Hosting APIs, microservices | DevOps     | On-demand            | -            |
| Notion             | Docs and collaboration      | Whole Team | Free Plan (upgrade?) | -            |

---

## Time Breakdown (Milestone-Level)

| Milestone              | Duration  | Resources Involved  |
|------------------------|-----------|---------------------|
| Requirements Gathering | 2 weeks   | PM, Product Owner   |
| Design Phase           | 1.5 weeks | Dev Team, UI/UX     |
| Implementation Phase   | 6 weeks   | All Developers      |
| QA & Stabilization     | 2 weeks   | QA Team, Developers |
| Deployment             | 3 days    | DevOps, PM          |

---

## Skills Inventory

| Team Member | Core Skills            | Training Needed         | Assigned Mentor |
|-------------|------------------------|-------------------------|-----------------|
| A. Rahmani  | React, Redux           | Docker Basics           | Z. Khanzada     |
| L. Hamdard  | Manual/Auto Testing    | Cypress Deep Dive       | Self-paced      |
| Z. Khanzada | AWS, CI/CD, Monitoring | Load Testing Techniques | L. Hamdard      |

---

## Utilization Tracking

| Team          | Ideal Load | Current Load | Notes                          |
|---------------|------------|--------------|--------------------------------|
| Frontend Team | 80%        | 90%          | Might need 1 more FE dev       |
| Backend Team  | 100%       | 100%         | Sustainable                    |
| QA Team       | 100%       | 80%          | Idle cycles; can assist DevOps |
| DevOps        | 70%        | 65%          | Room to help in performance    |

---

## Resource Contingency Plan

> If someone gets sick, goes rogue, or a server explodes, here’s how we bounce back.

- Maintain at least **1 backup** per key resource
- Cross-train Devs and QA in minimal tasks
- Pre-allocate **buffer time** in critical sprints
- Maintain a pool of **freelancers** or interns (if budget allows)

---

## Historical Resource Adjustments

| Date             | Change Made                       | Reason                        | Impact                   |
|------------------|-----------------------------------|-------------------------------|--------------------------|
| <2025-06-27 Fri> | Added backup FE developer         | Rahmani going on leave        | Sprint 3 shifted by 2d   |
| <2025-06-27 Fri> | Removed redundant Docker instance | Cost optimization             | Saved $50/month          |
| <2025-06-27 Fri> | Reallocated QA to assist DevOps   | Testing tasks completed early | Helped with test metrics |

---

## Responsibilities

| Role            | Responsibility                          |
|-----------------|-----------------------------------------|
| Project Manager | Maintains this doc, updates allocations |
| Team Leads      | Request updates based on sprint needs   |
| DevOps          | Tracks infrastructure changes           |
| QA Lead         | Ensures test environments are stable    |

---

## References

- [roles-and-assignees.md](roles-and-assignees.md)
- [estimation.md](estimation.md)
- [buffer.md](buffer.md)
- [monitoring-control.md](monitoring-control.md)

<!-- END OF resource-management.md -->
