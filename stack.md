<!--
START OF: stack.md
Purpose: Outlines the technology stack that will be used when building the project.
Update Frequency: Whenever a new technology is integrated into the project.
Location: docs/stack.md
-->

# Project Tech Stack

> This document outlines the technologies, frameworks, libraries, and platforms powering the project.

## Backend

| Tech       | Purpose               | Notes                       |
|------------|-----------------------|-----------------------------|
| Go         | Core backend API      | High-performance services   |
| gRPC       | Service communication | Efficient and type-safe     |
| PostgreSQL | Relational DB         | Used for transactional data |

## Frontend

| Tech       | Purpose      | Notes                       |
|------------|--------------|-----------------------------|
| TypeScript | Language     | Safer and scalable          |
| React      | UI framework | Dynamic frontend components |

## Infrastructure

| Tech       | Purpose                       | Notes                         |
|------------|-------------------------------|-------------------------------|
| Docker     | Containerization              | Unified dev/prod environments |
| Kubernetes | Orchestration                 | For scalability               |
| NGINX      | Reverse proxy / Load balancer | High availability             |

## Testing

| Tech    | Purpose                 | Notes                      |
|---------|-------------------------|----------------------------|
| Jest    | Unit testing (frontend) |                            |
| Go test | Backend testing         | Standard Go test framework |

## Monitoring & Analytics

| Tech       | Purpose            | Notes |
|------------|--------------------|-------|
| Prometheus | Metrics collection |       |
| Grafana    | Visualization      |       |

## Logging & Analysis

| Tech                                | Purpose                  | Notes |
|-------------------------------------|--------------------------|-------|
| ELK Stack (Elastic/Logstash/Kibana) | Centralized log analysis |       |


## Security & Auth

| Tech   | Purpose                    | Notes                     |
|--------|----------------------------|---------------------------|
| JWT    | Token-based authentication | Used for session handling |
| OAuth2 | Third-party logins         | e.g., Google/GitHub auth  |

## Miscellaneous

- Markdown for documentation
- GitHub Projects for task management
- VSCode recommended setup (see `dev-notes/tools-setup.md`)

<!-- END OF stack.md -->
