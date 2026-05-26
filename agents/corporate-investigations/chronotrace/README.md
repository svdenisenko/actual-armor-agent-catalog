# ChronoTrace

- **Status:** `launch_draft`
- **QA status:** `manual_qa_pending`
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
- [ ] Manual QA executed in runtime
- [ ] Duplicate/overlap review completed and recorded
- [ ] Promotion decision recorded (`not_launched` until QA passes)

## QA status
ChronoTrace is in **launch draft** state and remains **manual_qa_pending**. This agent is **not launched** and must not be promoted until manual QA and overlap review are completed.
