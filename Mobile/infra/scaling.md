<!--
START OF: scaling.md
Purpose: Define strategies to scale infrastructure components (horizontally/vertically).
Update Frequency: When scaling strategies or policies evolve.
Location: docs/infra/scaling.md
-->

# Infrastructure Scaling Guide

## Purpose
To keep the system performant and cost-efficient by scaling components based on usage and projected growth.

---

## Components & Scaling Strategies

| Component      | Type      | Scaling Method            | Notes                          |
|----------------|-----------|---------------------------|--------------------------------|
| API Servers    | Stateless | Horizontal (Auto-scaling) | Based on CPU > 65% for 10 mins |
| Database       | Stateful  | Vertical (Manual)         | Scheduled downtime if needed   |
| Message Queues | Stateful  | Partitioning              | Kafka topic rebalancing        |
| Load Balancers | Stateless | Auto-scaling              | Based on request throughput    |
| Redis / Cache  | Stateful  | Shard + Vertical          | Memory limit triggers alerts   |

---

## Scaling Triggers

-  **CPU > 70%**: Auto-scale application layer
-  **Memory > 80%**: Scale Redis or DB
-  **Queue backlog > 5000**: Add consumers
- ️**Error rate spike**: Investigate before scaling

---

## Scaling Limits

- Max replicas: 10 (per API service)
- DB max RAM: 32 GB
- Redis max cache: 8 GB

Manual approval needed to exceed these.

---

## Capacity Planning

- Reviewed quarterly based on traffic trends.
- Benchmarks run before release of new features.
- Stress testing using [Locust](https://locust.io) or [k6](https://k6.io).

---

##  Related Docs

- [message-queues.md](message-queues.md)
- [logging-monitoring.md](logging-monitoring.md)

<!-- END OF: scaling.md -->
