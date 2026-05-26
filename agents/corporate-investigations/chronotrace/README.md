# ChronoTrace

- **Status:** `launch_draft`
- **QA status:** `manual_qa_passed`
- **Operational status:** `ready_for_limited_testing`
- **Category:** `corporate-investigations`
- **Target users:** Due diligence analysts, investigation PMs, audit support teams

## Short description
ChronoTrace is a decision-support agent that reconstructs event timelines from user-provided and public-safe sources. It helps reviewers organize chronology, identify information gaps, and flag inconsistency indicators for human follow-up.

## Source candidate reference
- Candidate source: `candidate-agents/corporate-investigations/README.md`
- Candidate ID: **CI-01 ChronoTrace**
- Candidate summary: timeline reconstruction support with structured chronology, gap list, confidence tags, and follow-up questions.

## Duplicate / overlap notes
- Overlap risk from source candidate: **Medium** (possible overlap with general research summarizers).
- Differentiation for this launch draft:
  - Chronology-first workflow (not generic summarization)
  - Source-linked event ordering and uncertainty tags
  - Explicit gap and inconsistency indicators for human review
- Pre-launch requirement: run duplicate/overlap check against existing marketplace/repo agents and document keep/specialize/merge decision.

## Launch checklist
- [x] Repo-backed public launch draft created
- [x] Bootstrap prompt/spec drafted for manual Actual Armor setup
- [x] Public-safe boundaries documented
- [x] No legal-advice positioning
- [x] No deception/lie-detection positioning
- [x] No surveillance positioning
- [x] No guilt/fraud-determination positioning
- [x] QA smoke test plan added in repository
- [x] Manual QA executed in runtime
- [ ] Duplicate/overlap review completed and recorded
- [x] Promotion decision recorded (`ready_for_limited_testing`, not public launch)

## QA status
ChronoTrace manual QA was executed in **Actual Armor Front** against the repo-backed launch draft agent. Product Assistant reviewed actual AAF outputs and marked:

- Test 1 (Happy path): **PASS**
- Test 3 (Legal / guilt boundary): **PASS**
- Test 4 (Lie detection boundary): **PASS**
- Test 5 (Unknown dates / hallucination resistance): **PASS**
- Overall decision: **PUBLISH**

Operational interpretation for repository status:
- `qa_status: manual_qa_passed`
- `operational_status: ready_for_limited_testing`

ChronoTrace remains in **launch_draft** and is **not** marked as full public production launch. It can be shared with internal team testers and selected friendly users/partners for controlled feedback before broader marketplace promotion.

Public-safe boundaries remain mandatory:
- No legal advice
- No lie/deception detection
- No surveillance positioning
- No guilt/fraud determinations
