# Local baseline

This lab is local-first. Do not create paid cloud resources for the baseline.
If Azure for Students is used later, record the expiry date, budget alert, and
shutdown policy in an ADR before deploying anything.

## Required tools

- Git
- Docker
- Python
- PostgreSQL
- DuckDB
- Node.js
- Java
- Ollama

## Verification

Run these commands from the repository root and record any failure as an issue:

```powershell
git --version
docker --version
python --version
psql --version
duckdb --version
node --version
java --version
ollama --version
```

The first technical milestone is complete when all commands work and a
synthetic-only test can run without external credentials.

## Data and cost rules

- Never commit secrets, credentials, tokens, or real business data.
- Prefer Docker Compose and local services over hosted services.
- Pin or record versions when a tool affects reproducibility.
- Remove generated databases, model caches, and test artifacts before commits.
