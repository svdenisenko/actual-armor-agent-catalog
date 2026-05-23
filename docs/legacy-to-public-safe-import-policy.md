# Legacy-to-Public-Safe Import Policy

## Purpose

This repository (`svdenisenko/actual-armor-agent-catalog`) contains only public-safe marketplace agent metadata and runtime-loadable specifications.

Its role is to publish reviewed, customer-facing agent materials that are safe to expose publicly and safe to run through the Actual Armor thin-shell runtime path.

## Repository Boundary

### Private repository (non-public)
- `actual-armor-context`
- Stores private and internal operating context, including OpenWebUI role assistants, private marketplace context, internal workflows, and legacy runtime exports.

### Public repository (this repo)
- `svdenisenko/actual-armor-agent-catalog`
- Stores only reviewed, rewritten, public-safe metadata and runtime specs for customer-facing marketplace agents.

## Legacy Export Handling

Raw legacy export files (for example `agent_export.json`, `agent_export.csv`, and `agent_export.md`) belong only in the private `actual-armor-context` repository.

These files must **never** be committed to this public repository, directly or indirectly.

## What Is Allowed in This Repo

Allowed public-safe import outputs include:
- reviewed metadata skeletons
- refactored public-safe specs
- `bootstrap.md` files
- runtime-loadable instructions
- output templates
- public-safe knowledge stubs
- public-safe tool declarations
- QA/readiness status files
- smoke test notes and status patches

## What Is Not Allowed

The following content is disallowed in this public repository:
- raw prompts
- private Actual Armor context
- live account exports
- credentials or sensitive account identifiers beyond already-public/general references
- internal business workflows
- private OpenWebUI role context
- internal marketplace reasoning
- unreviewed agent dumps
- sensitive operational context
- private customer/team/investor content

## Required Review Flow

Before any legacy-derived agent can be treated as public catalog material, follow this flow:

1. Raw legacy export lands in private repo only.
2. Product v2 reviews the legacy agent list.
3. Product v2 selects next refactor candidates.
4. Candidate receives public-safe metadata skeleton.
5. Candidate is rewritten into a clean spec.
6. Runtime bootstrap is created or updated.
7. AA thin shell loads raw GitHub `bootstrap.md` through HTTP tool.
8. Runtime smoke test verifies loading and behavior.
9. QA status patch updates readiness/status.
10. Only then can the candidate be treated as public catalog material.

## Required Runtime Path

Every legacy-derived public candidate must preserve this path:

`clean spec → runtime smoke → QA status patch`

## Naming and Status Conventions

Use clear, auditable progression states such as:
- `candidate_identified`
- `metadata_skeleton_created`
- `clean_spec_drafted`
- `runtime_bootstrap_ready`
- `runtime_loading_passed`
- `behavior_smoke_passed`
- `runtime_smoke_passed`
- `qa_patch_required`
- `qa_patch_applied`
- `public_ready`

## Minimum Acceptance Checklist

For any future legacy-derived public agent, all items below must be satisfied:

- [ ] No raw legacy prompt copied
- [ ] No private AA context included
- [ ] No credentials or live account dump included
- [ ] Agent has public-safe description
- [ ] Agent has clear user-facing value proposition
- [ ] Agent has clean runtime instructions
- [ ] Output template is safe and structured
- [ ] Tool usage is declared without private implementation details
- [ ] Runtime loading smoke test passed
- [ ] Behavior smoke test passed
- [ ] QA/readiness status updated
