# Learning Lab architecture

## Current state

The repository is at the bootstrap stage. No runtime services or external
providers are required yet.

## First vertical slice

```text
synthetic fixtures
        |
        v
source simulator (PostgreSQL, files, HTTP API)
        |
        v
ingestion library
  - contract validation
  - pagination and retries
  - checkpoints and idempotency
        |
        +--> quarantine records
        |
        v
local raw storage
```

The first implementation will use synthetic data and local services only.
Transformations, orchestration, retrieval, model calls, and observability are
later layers; they should not be introduced before ingestion behavior is
tested.

## Success criteria

- A fresh checkout can run the tests without credentials.
- A fixed input snapshot produces the same output on repeated runs.
- Duplicate and malformed records are handled explicitly.
- A failed page can be retried without duplicating stored records.
