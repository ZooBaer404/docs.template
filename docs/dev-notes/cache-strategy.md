<!--
START OF: cache-strategy.md
Purpose: Define what gets cached, where, and for how long.
Update Frequency: When performance or cache policies are changed.
Location: docs/dev-notes/cache-strategy.md
-->

# Cache Strategy

Faster than the DB. Not smarter.

---

## What’s Cached

| Data                  | Location  | TTL         | Notes                    |
|-----------------------|-----------|-------------|--------------------------|
| User profile (JWT)    | Redis     | 15 minutes  | From token decode        |
| Report previews       | Redis     | 5 minutes   | Full report isn't cached |
| System config (flags) | In-memory | App runtime | Rarely changes           |

---

## What *Not* to Cache

- ML detection results (prone to bugs)
- Live upload processing
- User roles (too sensitive)

---

## Invalidation Strategy

- Manual purge via admin panel
- Cache bust on DB update (where applicable)

---

> Cache responsibly. That 404 you saw may be last month’s ghost.

<!-- END OF: cache-strategy.md -->
