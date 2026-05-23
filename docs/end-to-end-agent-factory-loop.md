# End-to-End Agent Factory Loop

## Purpose

This repository supports a controlled, public-safe workflow for turning selected agent ideas into runtime-loadable Actual Armor marketplace agents.

The public repository is the source of truth for public-safe metadata, clean runtime specs, bootstrap files, QA/readiness status, and process documentation. Private legacy data remains outside this repository.

## Target Loop

1. **Private legacy/context source**
2. **Product v2 candidate selection**
3. **Codex public-safe spec generation**
4. **Public repo PR / merge**
5. **Craft Agent marketplace creation/update**
6. **Tester Agent runtime QA**
7. **QA/readiness status patch**
8. **Human Product approval**
9. **Public-ready catalog status**

## Role Responsibilities

### Product v2
- Reviews private summaries and current public catalog status.
- Selects next candidates.
- Checks overlap, risk, value, and public-safety.
- Generates Codex-ready tasks.

### Codex
- Creates or updates public-safe repository files.
- Never copies raw prompts.
- Maintains metadata, bootstrap, specs, QA/readiness files, and docs.
- Patches readiness/status after QA.

### Craft Agent
- Creates or updates the marketplace agent from the repository source of truth.
- Uses the thin shell + HTTP bootstrap loading pattern.
- Returns marketplace URL/ID and craft evidence.

### Tester Agent
- Tests the real marketplace runtime.
- Checks loading, behavior, output format, private-context leakage, and tool usage.
- Produces QA verdict and patch recommendations.

### Human Product
- Approves candidate selection.
- Approves marketplace publish/update.
- Approves public-ready status.

## Status Model

- `candidate_identified`
- `metadata_skeleton_created`
- `clean_spec_drafted`
- `runtime_bootstrap_ready`
- `marketplace_created`
- `marketplace_updated`
- `runtime_loading_passed`
- `behavior_smoke_passed`
- `runtime_smoke_passed`
- `qa_patch_required`
- `qa_patch_applied`
- `public_ready`
- `blocked_by_craft`
- `blocked_by_runtime`
- `blocked_by_tools`
- `blocked_by_private_context_risk`

## Required Flow

Every candidate should follow this minimum progression:

**clean spec → runtime smoke → QA status patch**

A merged clean spec is required before marketplace creation/update. Runtime smoke results then drive a required QA/readiness status patch in this public repository.

## Guardrails

- No raw prompts.
- No raw legacy exports.
- No private Actual Armor context.
- No credentials.
- No direct dump-to-marketplace process.
- Repository source of truth comes before marketplace creation.
