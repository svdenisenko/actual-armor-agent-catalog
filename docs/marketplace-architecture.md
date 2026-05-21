# Marketplace Architecture

## Purpose
This repository is the **source of truth** for customer-facing Actual Armor marketplace agent metadata and specifications.

## Source-of-Truth Boundary
- The public catalog in this repo governs marketplace-facing naming, descriptions, visibility, and readiness.
- Internal role assistants and backoffice assistants are out of scope.
- Public metadata here should be treated as authoritative for Product, CMO, QA, and automation workflows.

## Runtime Model
- Actual Armor runtime agents can be executed via a thin runtime shell that loads agent artifacts over HTTP(S) from this repository (or mirrored artifacts).
- Runtime-specific tool binding can still be configured by runtime operators.

## Specification Completeness Model
- `metadata_only` agents are intentional placeholders until prompt/tool export exists.
- Placeholder metadata may be listed in catalog/index files, but must not be treated as production ready.
- Full specs (system/instructions/output/tests/etc.) can be upgraded incrementally agent-by-agent.

## Upgrade Strategy
- Incremental rollout is expected:
  1. metadata skeleton
  2. draft imported materials
  3. full spec drafting
  4. runtime load tests
  5. QA smoke testing
  6. soft launch and promotion review

## Sensitive Agent Handling
- Sensitive agents require stricter evidence discipline, policy checks, and QA gating before marketing promotion.
- Sensitive coverage is defined in `docs/sensitive-agent-policy.md`.
