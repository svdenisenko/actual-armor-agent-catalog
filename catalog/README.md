# Canonical Marketplace Agent Catalog

This directory is the public-safe, repo-backed catalog layer for Actual Armor marketplace agents and workflows. It is designed to give Product, Craft, QA, and CMO one normalized source for marketplace inventory, creation readiness, lifecycle-email references, and testing status.

## Catalog files

| File | Purpose |
|---|---|
| `marketplace-agents.yaml` | Canonical machine-readable catalog for Product/Craft automation, QA, and CMO planning. |
| `marketplace-agents.md` | Human-readable catalog summary for review and planning. |
| `schemas/agent.schema.json` | JSON schema for one normalized catalog record. |
| `aaf-live-agent-import-template.csv` | Template Product/humans should use to paste or export current live AAF marketplace inventory. |
| `creation-queue/aaf-creation-queue.md` | AAF creation selection rules and tracking table. |

## Current completeness warning

The broader live AAF marketplace inventory is **not present in this public repo** as of `2026-05-28`. The catalog therefore includes a control record with status `NEEDS_AAF_EXPORT` instead of inventing live agents.

Product or a human owner must import or paste the current AAF live marketplace list into this repo before anyone treats this catalog as complete. Use `aaf-live-agent-import-template.csv`, then convert each verified live item into a normal `marketplace-agents.yaml` record with status, source files, AAF link, QA state, and lifecycle-email constraints.

## Status values

Catalog records use one of these statuses:

- `LIVE_IN_AAF`: verified live marketplace item with repo-backed evidence and AAF link.
- `READY_FOR_LIMITED_TESTING`: created/tested enough for controlled limited testing, but not broad public launch.
- `AAF_CREATE_READY`: repo-backed creation packet exists; Product/Craft may create in AAF after confirming required fields.
- `DRAFT`: candidate or concept exists, but creation packet/readiness is incomplete.
- `NEEDS_PRODUCT_REVIEW`: needs product decision, specialization, duplicate review, or merge decision before creation.
- `NEEDS_QA`: created or drafted but QA is not complete.
- `HOLD`: blocked from creation.
- `REPOSITION_REQUIRED`: blocked until renamed/reframed into a public-safe concept.
- `NEEDS_AAF_EXPORT`: live marketplace inventory is missing from the repo and must be imported/exported.

## CMO / SendPulse usage rules

CMO should use only `catalog/marketplace-agents.yaml` or `catalog/marketplace-agents.md` as the source for marketplace agent/workflow references in lifecycle emails.

CMO must not invent:

- agent availability;
- CTA links;
- categories;
- workflow status;
- launch, QA, or testing claims.

If an agent has no `aaf_link`, or if its status is not `LIVE_IN_AAF` or `READY_FOR_LIMITED_TESTING`, CMO should avoid user-facing "try this agent now" language. For `AAF_CREATE_READY`, `DRAFT`, `NEEDS_PRODUCT_REVIEW`, `HOLD`, `REPOSITION_REQUIRED`, or `NEEDS_AAF_EXPORT` records, use internal planning language only.

For `READY_FOR_LIMITED_TESTING`, use controlled language such as selected/friendly tester feedback, not broad public launch claims.

## Product / Craft automation rules

Product/Craft automation should use `marketplace-agents.yaml` plus `creation-queue/aaf-creation-queue.md` when selecting AAB-to-AAF creation work.

Minimum rules:

1. Pick only `AAF_CREATE_READY` agents for new AAF creation.
2. Do not create `HOLD` or `REPOSITION_REQUIRED` agents.
3. Do not create agents missing required public-facing fields: name, slug, category, short/long descriptions, opening message, required inputs, expected output format, safety rules, source-discipline rules, and do-not-claim rules.
4. After AAF creation, update `creation_status`, `aaf_link`, and `qa_status` before any CMO or QA workflow treats the record as available.
5. Never convert a record to `LIVE_IN_AAF` without repo-backed evidence and an AAF link.

## Initial population

This catalog initially represents:

- `CI-01` ChronoTrace as `READY_FOR_LIMITED_TESTING`, based on the existing repo-backed launch draft and manual QA status.
- `CI-02` InvestIQ as `AAF_CREATE_READY`, based on its existing repo-backed packet and status tracker.
- `CI-03` through `CI-13` as candidate records with conservative readiness derived from the corporate investigations roster and status tracker.
- A marketplace inventory control record marked `NEEDS_AAF_EXPORT` because the current full live AAF marketplace list is not present in this repo.

No corporate investigations candidate is marked `LIVE_IN_AAF` in this initial catalog.
