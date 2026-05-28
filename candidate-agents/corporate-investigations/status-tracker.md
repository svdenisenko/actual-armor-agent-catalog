# Corporate Investigations Launch Status Tracker (Operational)

This tracker records rollout status for corporate investigations **candidate agents** so Product can independently track progress across Actual Armor Backoffice (AAB) and Actual Armor Front (AAF).

Operational constraints:
- Candidate roster source of truth remains `README.md` in this folder.
- Do not mark candidates as launched unless they have completed required launch steps.
- High-risk legacy concepts remain **HOLD / REPOSITION** unless explicitly reframed.

## Launch tracker table

| ID | Candidate name | Risk level | Recommended action | Current status | AAB Product packet status | AAF created? | Manual QA status | Repo launch draft status | Limited testing status | Next action | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| CI-01 | **ChronoTrace** | Low | Create | **manual_qa_passed / ready_for_limited_testing** | Complete | Yes | Passed | Exists | Not started | Share with internal team and selected friendly testers | Completed reference cycle: candidate selected, repo-backed draft created, AAF agent created, manual QA passed, Product Assistant review completed. |
| CI-02 | **InvestIQ** | Low | Create | **launch_packet_complete / ready_for_aaf_creation** | Complete | No | Not started | Exists | Not started | Create InvestIQ in AAF from repo-backed launch packet, then run manual QA smoke tests | Product packet and launch draft prepared; not created in AAF, not QA-passed, not launched. |
| CI-03 | **PolicySentry** | Medium | Specialize | not_started | Not started | No | Not started | Not started | Not started | Draft public-safe scope language and uncertainty/caveat requirements before packet prep | Keep non-legal-advice framing and avoid enforcement conclusions. |
| CI-04 | **EvidenceLedger** | Low | Create | not_started | Not started | No | Not started | Not started | Not started | Queue for packet creation after CI-02 | Low-risk organizational utility; strong follow-on candidate. |
| CI-05 | **SourceReliability Mapper** | Medium | Merge | not_started | Not started | No | Not started | Not started | Not started | Run duplicate/overlap review and decide merge target | High overlap risk with existing verification/reputation capabilities. |
| CI-06 | **EntityLink Mapper** | Medium | Specialize | not_started | Not started | No | Not started | Not started | Not started | Define evidence-grounded scope and ambiguity handling before packet prep | Avoid insinuation language in relationship mapping outputs. |
| CI-07 | **RiskSignal Triage** | Medium | Specialize | not_started | Not started | No | Not started | Not started | Not started | Define non-deterministic triage rubric and human-review checkpoints | Do not position as automated pass/fail risk scoring. |
| CI-08 | **NarrativeConsistency Review** | Medium | Create | not_started | Not started | No | Not started | Not started | Not started | Draft packet with strict consistency-analysis framing | Keep positioning away from deception detection claims. |
| CI-09 | **AdverseMedia Digestor** | Medium | Merge | not_started | Not started | No | Not started | Not started | Not started | Run duplicate/overlap review against existing reputation agents | Prefer integration instead of net-new launch if overlap confirmed. |
| CI-10 | **CounterpartyDD Brief** | Low | Create | not_started | Not started | No | Not started | Not started | Not started | Queue after initial low-risk candidates; require uncertainty section | High-value due diligence briefing candidate. |
| CI-11 | **VeracityJudge** | High | **HOLD / REPOSITION** | **hold / reposition_required** | Blocked | No | Blocked | Blocked | Blocked | Keep on hold until fully renamed/reframed to public-safe use | Legacy deception-adjudication concept; not launch-ready. |
| CI-12 | **WorkforceWatch** | High | **HOLD / REPOSITION** | **hold / reposition_required** | Blocked | No | Blocked | Blocked | Blocked | Keep on hold until surveillance framing is removed and use case is rewritten | Legacy employee-monitoring concept; not launch-ready. |
| CI-13 | **FraudVerdict Engine** | High | **HOLD / REPOSITION** | **hold / reposition_required** | Blocked | No | Blocked | Blocked | Blocked | Keep on hold until deterministic verdict framing is replaced with indicator-only support | Legacy deterministic fraud/guilt concept; not launch-ready. |

## Status legend

- `not_started`: no launch execution started yet.
- `next_candidate`: prioritized next for the manual launch cycle.
- `manual_qa_passed / ready_for_limited_testing`: manual QA completed in AAF; controlled limited testing is next.
- `hold / reposition_required`: blocked from launch pending rename/reframe to public-safe scope.
- `launch_packet_complete / ready_for_aaf_creation`: Product packet and repo launch draft exist, but AAF creation, manual QA, limited testing, and launch are not complete.
