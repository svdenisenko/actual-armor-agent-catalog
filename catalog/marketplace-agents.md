# Marketplace Agent Catalog

- **Catalog version:** `0.1.0`
- **Last verified:** `2026-05-28`
- **Inventory completeness:** `NEEDS_AAF_EXPORT`

## Critical completeness note

The broader live AAF marketplace inventory is not present in this repo. The catalog includes a `NEEDS_AAF_EXPORT` control record so Product/CMO/QA do not invent live marketplace agents or workflow availability.

Product or a human owner must import the current AAF live marketplace list before treating this catalog as complete.

## Human-readable inventory

| ID | Name | Status | Category | QA status | Creation status | AAF link | CMO CTA guidance | Source files |
|---|---|---|---|---|---|---|---|---|
| AAF-LIVE-INVENTORY-EXPORT | Current AAF Live Marketplace Inventory Export Required | `NEEDS_AAF_EXPORT` | marketplace-inventory | `not_applicable` | `needs_aaf_export` | missing | No external CTA. Internal action only: import AAF live inventory. | `agents/index.md`<br>`catalog/aaf-live-agent-import-template.csv` |
| CI-01 | ChronoTrace | `READY_FOR_LIMITED_TESTING` | Timeline reconstruction | `manual_qa_passed` | `created_in_aaf_ready_for_limited_testing` | missing | Use controlled limited-testing language only; CTA should invite selected testers to provide feedback, not broad public launch claims. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md`<br>`agents/corporate-investigations/chronotrace/README.md`<br>`agents/corporate-investigations/chronotrace/bootstrap.md` |
| CI-02 | InvestIQ | `AAF_CREATE_READY` | Planning & scoping support | `not_started` | `launch_packet_complete_ready_for_aaf_creation` | missing | Internal/product CTA only: create in AAF and run QA. Do not tell end users to try it yet. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md`<br>`agents/corporate-investigations/investiq/README.md`<br>`agents/corporate-investigations/investiq/bootstrap.md`<br>`agents/corporate-investigations/investiq/qa-smoke-tests.md` |
| CI-03 | PolicySentry | `NEEDS_PRODUCT_REVIEW` | Policy mapping support | `not_started` | `not_started` | missing | No user-facing CTA until product review and creation readiness are recorded. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-04 | EvidenceLedger | `DRAFT` | Evidence organization | `not_started` | `not_started` | missing | No user-facing CTA until packet creation and QA status are recorded. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-05 | SourceReliability Mapper | `NEEDS_PRODUCT_REVIEW` | Source review & reliability | `not_started` | `blocked_pending_merge_review` | missing | No CTA; product merge decision required first. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-06 | EntityLink Mapper | `NEEDS_PRODUCT_REVIEW` | Entity relationship mapping | `not_started` | `not_started` | missing | No user-facing CTA until product review is complete. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-07 | RiskSignal Triage | `NEEDS_PRODUCT_REVIEW` | Early risk indicator triage | `not_started` | `not_started` | missing | No user-facing CTA until product review is complete. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-08 | NarrativeConsistency Review | `DRAFT` | Consistency analysis | `not_started` | `not_started` | missing | No user-facing CTA until packet creation and QA status are recorded. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-09 | AdverseMedia Digestor | `NEEDS_PRODUCT_REVIEW` | Media signal aggregation | `not_started` | `blocked_pending_merge_review` | missing | No CTA; product merge decision required first. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-10 | CounterpartyDD Brief | `DRAFT` | Due diligence support briefs | `not_started` | `not_started` | missing | No user-facing CTA until packet creation and QA status are recorded. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-11 | VeracityJudge | `REPOSITION_REQUIRED` | Truth/deception adjudication legacy concept | `blocked` | `hold_reposition_required` | missing | No CTA; do not promote or create. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-12 | WorkforceWatch | `REPOSITION_REQUIRED` | Employee monitoring legacy concept | `blocked` | `hold_reposition_required` | missing | No CTA; do not promote or create. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |
| CI-13 | FraudVerdict Engine | `REPOSITION_REQUIRED` | Deterministic fraud/guilt legacy concept | `blocked` | `hold_reposition_required` | missing | No CTA; do not promote or create. | `candidate-agents/corporate-investigations/README.md`<br>`candidate-agents/corporate-investigations/status-tracker.md` |

## CMO / SendPulse reminders

- Use this file or `marketplace-agents.yaml` for lifecycle email references.
- Do not invent availability, links, categories, workflow status, or launch claims.
- Avoid user-facing "try this agent now" language unless status is `LIVE_IN_AAF` or carefully scoped `READY_FOR_LIMITED_TESTING`.
- If `aaf_link` is missing, do not include a user-facing launch CTA.

## Initial catalog count

- Repo-backed corporate investigations agents/candidates represented: **13**.
- Full live AAF marketplace inventory: **missing; needs AAF export**.
