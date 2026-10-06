# Learning Lab

Local-first learning laboratory for building a production-shaped AI data
platform with synthetic data only.

## Constraints

- **Budget:** €0. Use local open-source software by default.
- **Data safety:** never add EPOS, client, personal, or production data.
- **Reproducibility:** every project must have a one-command setup, tests, and
  a short runbook.
- **AI discipline:** record a baseline and measurable evaluation before adding
  an AI feature.

## Repository map

```text
docs/       architecture, decisions, and operating notes
src/        learning-lab application code
tests/      automated checks
```

## First milestone

Build a local source simulator and reliable ingestion library for PostgreSQL,
CSV/JSON, and a paginated HTTP API. The simulator will include duplicates,
deleted records, malformed records, and schema changes so retries,
checkpointing, idempotency, and quarantine behavior can be tested safely.

### Start here

1. Verify the local prerequisites listed in `docs/local-baseline.md`.
2. Create the first synthetic source fixture.
3. Implement the ingestion contract and a happy-path test.
4. Add failure cases one at a time and document the measured behavior.

Progress is tracked through GitHub issues and the evidence scoreboard in the
learning plan. Each completed milestone should include code, tests,
documentation, and reproducible measurements.
