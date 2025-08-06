<!--
START OF: ci-cd.md
Purpose: Document automated integration and deployment pipeline.
Update Frequency: When GitHub Actions or build process changes.
Location: docs/infra/ci-cd.md
-->

# CI/CD Pipeline

Where your commits go to be judged.

---

## Tools Used

- GitHub Actions
- Docker
- Terraform (infra)
- Python / Bash for scripts

---

## Workflow Overview

```bash
name: CI/CD Pipeline

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - run: npm test

  deploy-staging:
    if: github.ref == 'refs/heads/main'
    steps:
      - run: ./scripts/deploy-staging.sh
```

## Deployment Strategy

| Env     | Trigger                 | Auto Deploy | Notes                |
|---------|-------------------------|-------------|----------------------|
| Local   | Manual                  | no          | Dev use only         |
| Staging | Push to `main`          | yes         | Testing & QA         |
| Prod    | Git tag push (`v*.*.*`) | yes         | Requires code freeze |

## Secrets

- Stored in GitHub Secrets
- Names follow: PROD_DB_URL, STAGING_API_KEY, etc.

> See .github/workflows/*.yml for complete configs.

<!-- END OF: ci-cd.md -->
