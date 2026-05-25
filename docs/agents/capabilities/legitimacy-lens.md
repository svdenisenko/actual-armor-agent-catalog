# Legitimacy Lens

## Short Description
Runs structured legitimacy checks on organizations, projects, founders, offers, and online presence using evidence-grounded due diligence and trust assessment methods.

## Primary Users
### Human operator
Investment analysts, partnership teams, procurement teams, and founders evaluating counterparties before commitments.

### AI agent
An AI agent that gathers corroborating records, maps claim-to-evidence links, highlights inconsistencies, and assembles a transparent trust assessment draft.

## When To Use
- Evaluating a new partner, vendor, founder, or project.
- Validating claims before signing agreements or allocating resources.
- Conducting pre-engagement due diligence for strategic collaborations.
- Re-checking legitimacy when risk signals emerge.

## Inputs
- Entity names, people names, domains, social profiles, and public documents.
- Claimed milestones, credentials, partnerships, and operating history.
- Jurisdiction and business context (if known).
- Prior screening outputs from other capabilities.

## Process
1. Extract explicit claims and categorize them (identity, operations, traction, governance).
2. Collect corroborating public evidence for each claim.
3. Score source reliability and relevance.
4. Identify gaps, contradictions, and unverifiable assertions.
5. Build a claim-evidence matrix with confidence notes.
6. Generate a trust/risk summary with unresolved questions.
7. Prepare escalation recommendations for human decision-makers.

## Outputs
- Legitimacy assessment brief.
- Claim-evidence matrix.
- Trust/risk indicators with confidence levels.
- Priority follow-up questions and evidence requests.

## Evidence Requirements
- Prioritize primary records and first-party statements with clear attribution.
- Use multiple independent sources for material claims.
- Timestamp evidence and preserve citation links.
- Mark unknowns and unverifiable items clearly.

## Confidence / Risk Notes
- Trust assessments are probabilistic and can change with new evidence.
- Missing evidence is a risk signal, not automatic proof of deception.
- Confidence should be tied to source depth, quality, and cross-validation.

## Human Decision Checkpoints
- Approve whether evidence suffices for partnership or investment progression.
- Decide whether unresolved gaps require additional diligence.
- Confirm final risk posture and communication language.

## Example Agent Use
An agent evaluates a proposed vendor, validates some operating claims, finds inconsistencies in team history, and submits a medium-confidence legitimacy brief with targeted follow-up requests.

## Not Included / Out of Scope
- Automatic approval or rejection decisions.
- Legal certification of legitimacy.
- Access to private or restricted systems without authorization.

## Public-Safe Notes
This public-safe capability excludes confidential customer information, internal-only risk models, and non-public investigative procedures.
