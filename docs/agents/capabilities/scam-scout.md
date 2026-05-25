# Scam Scout

## Short Description
Performs early risk screening of suspicious offers, websites, profiles, messages, investment pitches, job offers, and commercial propositions. It classifies risk, identifies red flags, and requests missing evidence without making unsupported legal conclusions.

## Primary Users
### Human operator
Fraud analysts, partnership teams, business operators, and investigators who need rapid triage before deeper diligence or engagement.

### AI agent
An AI agent that scans claim patterns, maps known scam signals, organizes red flags, and proposes evidence requests for human decision-makers.

## When To Use
- A new outreach message or offer appears unusually urgent or high-return.
- A website, profile, or proposal shows credibility inconsistencies.
- Teams need a fast go/no-go screening signal before spending resources.
- There is possible exposure to fraud, impersonation, or social engineering.

## Inputs
- Offer text, message logs, profile links, domains, and attachments.
- Claimed business model, returns, role, or compensation details.
- Wallet addresses, payment instructions, or contract references (if provided).
- Existing notes from prior checks.

## Process
1. Parse core claims (who, what, promised outcome, requested action).
2. Screen for high-risk patterns (pressure tactics, secrecy, guaranteed returns, identity mismatch).
3. Evaluate domain/profile consistency and public footprint signals.
4. Identify missing verification artifacts (licenses, registrations, references, disclosures).
5. Classify preliminary risk (low/medium/high) with rationale.
6. Build a targeted evidence request list.
7. Produce a human-review triage summary with recommended next steps.

## Outputs
- Preliminary risk classification.
- Red-flag matrix with severity and evidence status.
- Evidence request checklist.
- Next-step recommendation (proceed, pause, escalate, or decline).

## Evidence Requirements
- Use verifiable public sources and attributable records where possible.
- Separate observed facts from assumptions.
- Preserve exact claim language for auditability.
- Track unresolved claims explicitly.

## Confidence / Risk Notes
- Initial screening is directional, not final adjudication.
- High-risk signals increase caution but do not prove wrongdoing by themselves.
- Confidence depends on source completeness and cross-source consistency.

## Human Decision Checkpoints
- Approve whether to engage, pause, or terminate communication.
- Decide escalation to compliance, legal counsel, or security teams.
- Confirm final messaging to counterparties.

## Example Agent Use
An agent reviews a high-return crypto outreach, flags urgency tactics and unverifiable credentials, requests proof of registration and audited records, and provides a high-risk triage memo for human approval.

## Not Included / Out of Scope
- Legal determinations of fraud.
- Law-enforcement actions.
- Financial, legal, or investment advice.

## Public-Safe Notes
Public-safe capability definition only. No private strategy, customer data, credentials, or confidential enforcement workflows are included.
