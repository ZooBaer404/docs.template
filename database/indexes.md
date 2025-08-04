<!--
START OF: indexes.md
Purpose: Document indexing strategies to support performance and query optimization.
Update Frequency: When indexes are added, changed, or removed.
Location: docs/database/indexes.md
-->

# Indexing Strategy

## Purpose
Indexes improve query performance, especially on large tables. This document records all current indexing decisions and their justifications.

---

## Types of Indexes Used

| Type              | Usage Example              | Rationale                                 |
|-------------------|----------------------------|-------------------------------------------|
| Primary Index     | `id` (all tables)          | Ensures uniqueness and speeds up lookups. |
| Foreign Key Index | `user_id`, `assignment_id` | Supports JOIN performance.                |
| Full-Text Index   | `assignment.content`       | Enables fuzzy/semantic search.            |
| Composite Index   | `(user_id, submitted_at)`  | Optimizes combined lookups for analytics. |
| Unique Index      | `email` in `users`         | Prevents duplicate accounts.              |

---

## Example

```sql
CREATE INDEX idx_user_submission ON assignments (user_id, submitted_at);
```

Used in queries like:

```sql
SELECT * FROM assignments WHERE user_id = ? AND submitted_at > ?;
```

## Indexing Gotchas

- Indexes slow down INSERT/UPDATE.
- Too many indexes = degraded write performance.
- Composite indexes should reflect query access patterns.

## Indexing To-Do List

- Evaluate full-text index performance under load.
- Add GIN/BTREE index where applicable (PostgreSQL-specific).
- Periodically review unused indexes (via pg_stat_user_indexes).

<!-- END OF: indexes.md -->
