<!--
START OF: incident-response.md
Purpose: Define standardized procedures to detect, respond to, and recover from production incidents.
Update Frequency: After major outages, postmortems, or quarterly review cycles.
Location: docs/infra/incident-response.md
-->

# Incident Response Plan

## Classification Levels

| Severity | Description                      | Example                               |
|----------|----------------------------------|---------------------------------------|
| SEV-1    | Critical system-wide failure     | Entire API down, data loss            |
| SEV-2    | Major functionality degraded     | Payment service failing, high error % |
| SEV-3    | Minor issue with low user impact | One endpoint slow                     |
| SEV-4    | Cosmetic/UI/Logging bugs         | Typo in UI, log spam                  |

---

## Incident Lifecycle

### 1. **Detection**
- Sources:
  - Monitoring alerts (Prometheus/Grafana)
  - Customer support tickets
  - Internal QA bug reports
- Example alert:
```txt
    High latency on /auth/login | >2s for 95th percentile | Triggered: 2025-06-09 04:31 UTC
```

---

### 2. **Response & Containment**
- Assign an **Incident Commander (IC)**
- Join **#incident-response** Slack channel
- Triage severity level
- Mitigate further damage (e.g., shut down misbehaving services, revert deployments)

---

### 3. **Communication**
| Channel        | Frequency         | Owner            |
|----------------|-------------------|------------------|
| Status Page    | Every 30 mins     | IC               |
| Internal Slack | Real-time updates | IC / Eng on-call |
| Email          | Post-incident     | Support Lead     |

---

### 4. **Resolution**
- Apply patch/fix or rollback
- Validate using automated smoke tests
- Gradually restore affected services

---

### 5. **Postmortem**
- Must be completed within 48 hours of resolution
- Use standard [postmortem template](postmortem-template.md)
- Focus on:
- Timeline of events
- Root cause analysis (RCA)
- Action items with owners and due dates

---

## Roles & Responsibilities

| Role                | Responsibility                              |
|---------------------|---------------------------------------------|
| Incident Commander  | Owns coordination, severity assignment      |
| On-Call Engineer    | Mitigates and resolves technical issues     |
| Communications Lead | Updates internal/external stakeholders      |
| Scribe              | Documents timeline and actions in real-time |

---

## Simulation Drills

| Simulation Type     | Last Run         | Next Scheduled   | Notes                 |
|---------------------|------------------|------------------|-----------------------|
| SEV-1 Fire Drill    | <2025-06-27 Fri> | <2025-10-05 Sun> | API total outage test |
| Log Flood Injection | <2025-06-27 Fri> | <2025-10-06 Mon> | Alerting systems test |

---

## Tooling Reference

| Tool       | Purpose                 |
|------------|-------------------------|
| Prometheus | Metrics collection      |
| Grafana    | Alerting and dashboards |
| Sentry     | Exception tracking      |
| PagerDuty  | On-call escalation      |
| Loki       | Centralized logging     |

---

## Related Docs

- [logging-monitoring.md](logging-monitoring.md)
- [ci-cd.md](ci-cd.md)

<!-- END OF: incident-response.md -->
