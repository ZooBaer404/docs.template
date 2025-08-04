<!--
START OF: decisions-log.md
Purpose: Document major decisions and the reasoning behind them.
Update Frequency: Every time something is debated or a direction is chosen.
Location: docs/project-management/decisions-log.md
-->

# Decisions Log

Where bad ideas go to become *documented* bad ideas.

---

## <2025-06-17 Tue> — Switched to Async Upload Processing

> Team: Backend developer + Frontend developer

- Why:
  - Uploads were blocking the main thread.
  - Easier scaling with RabbitMQ.
- Alternatives Considered:
  - Threads? Too risky with Python GIL.
  - Crons? Not fast enough.

---

## <2025-02-24 Mon> — Chose Redis for Caching

- Why:
  - Fast reads, built-in TTLs.
  - Great local dev experience.
- Alternatives Considered:
  - Memcached: No persistence.
  - Custom in-memory store: Too fragile.

---

## <2025-05-05 Mon> — Stopped Using `.env` in Production

- Why:
  - Secret rotation was a mess.
  - Switched to Vault instead.

---

> Let this log save others from repeating our glorious mistakes.

<!-- END OF: decisions-log.md -->
