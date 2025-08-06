<!--
START OF: migrations.md
Purpose: Document database schema migration approach.
Update Frequency: When new migrations are introduced or policies change.
Location: docs/database/migrations.md
-->

# Database Migrations

Because changing a live database is always a good idea... if you're doing it **with structure**.

---

## Tools Used

We use **[Your Tool Here]** (e.g., Flyway, Alembic, Django ORM, custom SQL scripts).

---

## Migration Structure

- `migrations/001_init.sql` — Base schema creation.
- `migrations/002_add_plagiarism_log.sql` — Add plagiarism logging table.
- `migrations/003_add_index_assignments.sql` — Optimization migration.

---

## Workflow

1. All schema changes **must be applied via migration files**.
2. Migration files should be named using `NNN_description.sql`.
3. Each migration should:
   - Be **reversible** if possible.
   - Include `UP` and `DOWN` statements if tool supports.
   - Be tested on staging before prod.

---

## Testing Migrations

```bash
# Apply on test DB
$ migrate up

# Roll back last change
$ migrate down
```

> Remember: ALTER TABLE is forever. Choose wisely.

<!-- END OF: migrations.md -->
