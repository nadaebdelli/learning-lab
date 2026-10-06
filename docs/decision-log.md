# Architecture decision log

## ADR-001: Local-first and synthetic-only development

- **Status:** accepted
- **Date:** 2026-10-05
- **Decision:** Build and test the learning lab locally with synthetic data.
  Use hosted services only for short, documented demonstrations after the
  local behavior is reproducible.
- **Reason:** The project has a €0 budget rule and must remain safe for public
  portfolio use. Local execution also makes failures and measurements
  repeatable.
- **Consequences:** Docker and local databases are part of the development
  workflow. Cloud-specific behavior must be isolated and documented rather
  than becoming a hidden dependency.
