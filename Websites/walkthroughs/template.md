<!--
START OF: template.md
Purpose: to be filled.
Update Frequency: Each time the feature is updated.
Location: docs/walkthroughs/template.md
-->

# Feature Walkthrough: Feature Name

## Components Involved

- `backend/api/notify.py`
- `redis-pubsub`
- `frontend/NotificationPanel.jsx`

---

## Data Flow

1. User sends a message.
2. API triggers event → pushed to Redis.
3. Frontend subscribes to Redis via WebSocket.
4. Message shows in NotificationPanel.

---

## Gotchas

- Redis must be live before starting frontend.
- WS fails silently if token expired.

---

> Update this doc whenever the feature code changes.

<!-- END OF: walkthroughs/feature.md -->
