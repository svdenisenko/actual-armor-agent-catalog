# Actual Armor Public Agent Catalog

This repository contains **public-safe agent specifications** for Actual Armor marketplace agents.

## Purpose
- Provide customer-facing agent specs that can be used by compatible agent runtimes.
- Support Actual Armor running these agents as one platform/runtime.
- Keep specifications version-controlled for transparency, iterative improvement, and testing.
- Clarify that runtime-specific tool binding may still be configured manually by runtime operators.

## Scope
This repository is intentionally public-safe and does **not** contain internal Actual Armor operating context.

## Importing Legacy Agents

Legacy marketplace exports are handled in the private `actual-armor-context` repository only.
This public catalog accepts only reviewed, rewritten, public-safe metadata and runtime specs.

See:
- `docs/legacy-to-public-safe-import-policy.md`
- `docs/product-v2-next-refactor-candidates-workflow.md`

## Agent Factory Documentation

- `docs/end-to-end-agent-factory-loop.md`
- `docs/craft-agent-workflow.md`
- `docs/tester-agent-workflow.md`
- `docs/openwebui-craft-workflow-template.md`

## Agent Capabilities

- `docs/agents/CAPABILITIES.md`

## Agent Scoring

- `scoring/README.md`
- `scoring/agent-prioritization-framework.md`
- `scoring/agent-scorecard-template.md`
- `scoring/deduplication-checklist.md`
