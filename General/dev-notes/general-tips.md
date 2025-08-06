<!--
START OF: general-tips.md
Purpose: Collects best practices, coding conventions, and general advice for developers on this project.
Update Frequency: Update whenever a new tip or best practice is discovered.
Location: docs/dev-notes/general-tips.md
-->

# General Tips

---

## Tip [#1] - [Descriptive function comment]

**Date:** <2025-06-27 Fri>
**Author:** Zubair

Description:
Write a descriptive comment above each function stating its parameters, their types, what bound the values of the parameters should be, what they should return.


Example:
```python
def fetch_users(limit: int, offset: int, active_only: bool = True) -> list[dict]:
    """
    Fetch a paginated list of users from the database.

    Parameters:
    - limit (int): The maximum number of users to return.
      Must be a positive integer (1–1000). Recommended: 10–100.
    - offset (int): The number of users to skip before starting to collect the result set.
      Must be >= 0.
    - active_only (bool): Whether to fetch only active users. Defaults to True.

    Returns:
    - list[dict]: A list of user records, each represented as a dictionary with keys like
      'id', 'name', 'email', 'is_active'.

    Raises:
    - ValueError: If the `limit` or `offset` is out of acceptable bounds.
    - DatabaseError: If there is an issue connecting to or querying the database.

    Example:
    >>> fetch_users(limit=50, offset=0)
    [{'id': 1, 'name': 'Alice', ...}, ...]
    """
    if not (1 <= limit <= 1000):
        raise ValueError("Limit must be between 1 and 1000.")
    if offset < 0:
        raise ValueError("Offset cannot be negative.")

    query = "SELECT id, name, email, is_active FROM users"
    if active_only:
        query += " WHERE is_active = TRUE"
    query += " LIMIT %s OFFSET %s"

    # Example DB call (pseudocode)
    return db.execute(query, (limit, offset))
```

---

## Tip [#2] -

---

## Notes

- Keep tips short and actionable.
- Link related tips or docs where relevant.

<!-- END OF general-tips.md -->
