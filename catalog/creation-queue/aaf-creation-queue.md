# AAF Creation Queue

This queue defines how Product/Craft should choose repo-backed agents for AAF creation and how QA/CMO should know whether a newly created agent can be referenced.

## Selection rules

1. Pick only records with status `AAF_CREATE_READY` in `catalog/marketplace-agents.yaml`.
2. Do not create records with status `HOLD` or `REPOSITION_REQUIRED`.
3. Do not create records missing required public-facing fields:
   - `name`
   - `slug`
   - `category`
   - `short_description`
   - `long_description`
   - `opening_message`
   - `required_inputs`
   - `expected_output_format`
   - `safety_rules`
   - `source_discipline_rules`
   - `do_not_claim`
4. Do not create records whose `duplicate_overlap_notes` require merge/specialization review before launch.
5. After AAF creation, update the catalog record with:
   - `creation_status`
   - `aaf_link`
   - `qa_status`
   - `last_verified_date`
6. Do not mark a record `LIVE_IN_AAF` unless repo evidence confirms live availability and the record has a working AAF link.
7. CMO should not use "try now" language until status is `LIVE_IN_AAF` or carefully scoped `READY_FOR_LIMITED_TESTING`.

## Current creation tracking table

| Priority | ID | Agent | Catalog status | Creation status | QA status | AAF link | Owner | Next action |
|---:|---|---|---|---|---|---|---|---|
| 1 | CI-02 | InvestIQ | `AAF_CREATE_READY` | `launch_packet_complete_ready_for_aaf_creation` | `not_started` | missing | Product/Craft | Create in AAF from repo-backed packet, then run smoke tests and update catalog. |
| - | CI-01 | ChronoTrace | `READY_FOR_LIMITED_TESTING` | `created_in_aaf_ready_for_limited_testing` | `manual_qa_passed` | missing in repo | Product/QA | Add AAF link if available; keep controlled limited-testing language. |
| - | CI-03 | PolicySentry | `NEEDS_PRODUCT_REVIEW` | `not_started` | `not_started` | missing | Product | Specialize scope and caveat requirements before packet prep. |
| - | CI-04 | EvidenceLedger | `DRAFT` | `not_started` | `not_started` | missing | Product | Prepare packet after higher-priority safe candidates. |
| - | CI-05 | SourceReliability Mapper | `NEEDS_PRODUCT_REVIEW` | `blocked_pending_merge_review` | `not_started` | missing | Product | Run duplicate/merge review. |
| - | CI-06 | EntityLink Mapper | `NEEDS_PRODUCT_REVIEW` | `not_started` | `not_started` | missing | Product | Define evidence-grounded scope and ambiguity handling. |
| - | CI-07 | RiskSignal Triage | `NEEDS_PRODUCT_REVIEW` | `not_started` | `not_started` | missing | Product | Define non-deterministic rubric and human-review checkpoints. |
| - | CI-08 | NarrativeConsistency Review | `DRAFT` | `not_started` | `not_started` | missing | Product | Draft packet with consistency-analysis framing. |
| - | CI-09 | AdverseMedia Digestor | `NEEDS_PRODUCT_REVIEW` | `blocked_pending_merge_review` | `not_started` | missing | Product | Run duplicate/merge review against reputation agents. |
| - | CI-10 | CounterpartyDD Brief | `DRAFT` | `not_started` | `not_started` | missing | Product | Prepare packet after initial low-risk candidates. |
| blocked | CI-11 | VeracityJudge | `REPOSITION_REQUIRED` | `hold_reposition_required` | `blocked` | missing | Product | Do not create; rename/reframe away from deception adjudication. |
| blocked | CI-12 | WorkforceWatch | `REPOSITION_REQUIRED` | `hold_reposition_required` | `blocked` | missing | Product | Do not create; remove surveillance/employee-monitoring framing. |
| blocked | CI-13 | FraudVerdict Engine | `REPOSITION_REQUIRED` | `hold_reposition_required` | `blocked` | missing | Product | Do not create; replace deterministic verdict framing with indicator-only support. |

## AAF live inventory import blocker

The broader live AAF marketplace inventory is still missing from this repo. Product/humans must complete `catalog/aaf-live-agent-import-template.csv` or paste equivalent exported data before this catalog can claim complete marketplace coverage.
