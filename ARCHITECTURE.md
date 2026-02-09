# Architecture

## Boundary

`provenact-agent-kit` adapts execution primitives from `provenact-sdk`.
It does not decide what to do next.

## Design

- `ProvenactExecutionAdapter` provides one call:
  - verify bundle
  - execute verified bundle
  - parse receipt
- The adapter delegates all trust-critical checks to `provenact-sdk`/`provenact-cli`.

## Explicit Non-Goals

- no planning loop
- no memory store
- no scheduler
- no workflow state machine
