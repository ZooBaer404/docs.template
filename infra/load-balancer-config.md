<!--
START OF: load-balancer-config.md
Purpose: Explain load balancer setup and routing rules.
Update Frequency: When routing or balancing behavior changes.
Location: docs/infra/load-balancer-config.md
-->

# Load Balancer Config

Let there be traffic... and let it be *balanced*.

---

## Load Balancer Details

- **Type**: Application Load Balancer (AWS ALB)
- **Protocol**: HTTPS (TLS v1.2)
- **Certs**: AWS ACM (auto-renewed)

---

## Health Checks

- Path: `/health`
- Interval: 30s
- Unhealthy threshold: 3
- Timeout: 5s

---

## Routing Rules

| Rule        | Target Group      | Behavior                  |
|-------------|-------------------|---------------------------|
| `/api/*`    | `backend-service` | Forward to app containers |
| `/static/*` | `s3-cloudfront`   | Serve via CDN             |
| `/admin/*`  | `admin-ui`        | Auth required via Cognito |

---

>  Changing this without warning = you get the “prod went down” badge.

<!-- END OF: load-balancer-config.md -->
