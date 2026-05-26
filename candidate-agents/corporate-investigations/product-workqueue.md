# Corporate Investigations Product Workqueue

## 1) Purpose

This workqueue is the **default Product routing source** for corporate investigations candidate rollout in AAF.

Use it to answer:
- “яких агентів сьогодні створюємо в AAF?”
- “what is the next agent to create?”
- “давай наступного після ChronoTrace”
- “прогонимо смоки ChronoTrace”

This file is public-safe operational guidance and must be read together with `status-tracker.md` and candidate specifications.

## 2) Current rollout state

- **CI-01 ChronoTrace**: `manual_qa_passed` / `ready_for_limited_testing`
- **Next candidate**: **CI-02 InvestIQ** (unless `status-tracker.md` says otherwise)
- **Safe next set**:
  - CI-02 InvestIQ
  - CI-03 PolicySentry
  - CI-04 EvidenceLedger
  - CI-10 CounterpartyDD Brief

## 3) Completed reference cycle

- **Reference cycle completed**: CI-01 ChronoTrace
- Outcome: manual QA pass in AAF and recommendation for limited testing
- Constraint: CI-01 is not a full public production launch; keep controlled rollout language

## 4) Next recommended candidates

Primary queue order (subject to status tracker updates):

1. **CI-02 InvestIQ**
2. **CI-03 PolicySentry**
3. **CI-04 EvidenceLedger**
4. **CI-10 CounterpartyDD Brief**

Recommendation rule:
- Always confirm latest state in `status-tracker.md` before proposing the next build candidate.

## 5) HOLD / REPOSITION candidates

Do **not** recommend these for launch until fully reframed and approved:

- CI-11 VeracityJudge
- CI-12 WorkforceWatch
- CI-13 FraudVerdict Engine

Rationale:
- No legal advice
- No lie/deception detection
- No surveillance/employee monitoring framing
- No guilt/fraud determinations

## 6) Default Product Assistant routing

When human Product asks **what to create today**:
1. Read `product-workqueue.md` + `status-tracker.md`.
2. Return the next recommended candidate.
3. Explain why this candidate is next.
4. Warn against HOLD / REPOSITION candidates.
5. Provide the next AAB prompt draft for the selected candidate.

When human Product asks to **test ChronoTrace**:
1. Read ChronoTrace launch draft + QA smoke tests.
2. Provide smoke prompts for manual execution in AAF.
3. Ask human Product to paste actual AAF outputs.
4. Produce PASS / PARTIAL / FAIL verdict based on returned outputs.

## 7) Exact files Product should read first

1. `candidate-agents/corporate-investigations/README.md`
2. `candidate-agents/corporate-investigations/status-tracker.md`
3. `candidate-agents/corporate-investigations/product-workqueue.md`
4. `agents/corporate-investigations/chronotrace/README.md`
5. `agents/corporate-investigations/chronotrace/qa-smoke-tests.md`

## 8) Human Product next actions

1. Confirm status tracker still marks CI-01 as `ready_for_limited_testing`.
2. Start next build cycle with **CI-02 InvestIQ**.
3. If CI-02 is blocked, pick next from safe set in order: CI-03, CI-04, CI-10.
4. Keep CI-11/12/13 in HOLD / REPOSITION until public-safe redesign is approved.
5. For ChronoTrace smoke runs, collect actual AAF outputs and return them for formal PASS/PARTIAL/FAIL evaluation.

## Operating rules

- Do not mark untested agents as launched.
- Do not recommend HOLD candidates for launch.
- No legal advice, lie detection, surveillance, or guilt/fraud determinations.
- Keep public-safe operational language.
