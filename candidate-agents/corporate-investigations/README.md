# Corporate Investigations Candidate Agents (Public-Safe)

## 1) Purpose

This document is a **public-safe candidate roster** for corporate investigation, due diligence, and evidence-organization workflows. It is designed to be a **stable repository source** for Product Assistant evaluation and selection.

Important scope notes:
- These are **candidate agents only** (not launched marketplace agents).
- This file does **not** claim production readiness.
- This file avoids internal-sensitive investigative workflows and avoids private OpenWebUI attachment context.
- This file provides decision-support framing only and does not provide legal advice.

## 2) Public-safety guardrails

All candidates in this roster must follow these constraints before any launch consideration:

1. **Decision support only**: source review, timeline reconstruction, evidence organization, consistency analysis, risk indicators, policy mapping support, due diligence support.
2. **No legal advice**: outputs must include appropriate non-legal-advice framing.
3. **No deterministic truth/guilt claims**: do not claim deception detection, lie detection, guilt detection, or guaranteed fraud determinations.
4. **No surveillance positioning**: no employee monitoring, stalking, covert tracking, or private intelligence framing.
5. **Human oversight required**: risk flags are indicators for reviewer follow-up, not final judgments.
6. **Public-source and user-provided data boundaries**: candidates should be framed around lawful, consented, and policy-compliant inputs.
7. **High-risk candidates cannot proceed directly**: must be marked **HOLD / REPOSITION** until reframed to public-safe use.

## 3) Candidate roster table

> Source note: roster represents 13 internal candidate concepts from `CorpInvestigations.xlsx`, rewritten into public-safe specifications without importing the raw spreadsheet.

| ID | Candidate name | Investigation phase / category | Target users | Public-safe description | Likely inputs | Expected outputs | Risk level | Duplicate/overlap risk | Recommended action | Notes |
|---|---|---|---|---|---|---|---|---|---|---|
| CI-01 | **ChronoTrace** | Timeline reconstruction | Due diligence analysts, investigation PMs, audit support teams | Reconstructs event timelines from documents and public sources to support review and escalation sequencing. | Dated documents, emails, filings, media links, user notes | Structured chronology, gap list, confidence tags, follow-up questions | Low | Medium (overlap with general research summarizers) | **Create** | Strong first-launch candidate if scoped to chronology + evidence links only. |
| CI-02 | **InvestIQ** | Planning & scoping support | Investigations leads, risk analysts, compliance program teams | Helps define investigation scope, hypotheses, source plan, and review checkpoints for human-led workflows. | Case objective, constraints, known entities, source access assumptions | Investigation plan, scope matrix, source checklist, milestone plan | Low | Medium (overlap with project planning copilots) | **Create** | Strong first-launch candidate with strict non-accusatory language. |
| CI-03 | **PolicySentry** | Policy mapping support | Compliance, internal audit, risk operations | Maps observed facts to policy/control frameworks and highlights where human interpretation is required. | Policy text, controls library, incident facts, evidence excerpts | Policy-to-fact map, potential control gaps, review questions | Medium | Medium (overlap with compliance assistants) | **Specialize** | Candidate for early launch if wording avoids enforcement/legal conclusions. |
| CI-04 | **EvidenceLedger** | Evidence organization | Case managers, legal ops support, trust & safety review teams | Organizes documents, sources, and notes into traceable evidence bundles with provenance metadata. | Files, URLs, interview notes, source annotations | Evidence index, provenance map, citation pack, missing-evidence list | Low | Low | **Create** | High utility and low policy risk when limited to organization tasks. |
| CI-05 | **SourceReliability Mapper** | Source review & reliability | Analysts, reputational risk teams | Assesses source quality signals and consistency across references; flags verification depth needed. | Source links, publication metadata, claim excerpts | Source reliability matrix, corroboration map, caveat summary | Medium | High (overlap with verification/reputation agents) | **Merge** | Merge/reuse with existing verification capabilities where possible. |
| CI-06 | **EntityLink Mapper** | Entity relationship mapping | Corporate intelligence teams, vendor risk teams | Builds relationship maps between organizations, people, and events from provided/public evidence. | Entity names, corporate records, disclosures, news items | Relationship graph summary, linkage rationale, ambiguity flags | Medium | Medium | **Specialize** | Keep strictly evidence-grounded; avoid insinuation language. |
| CI-07 | **RiskSignal Triage** | Early risk indicator triage | Vendor onboarding, partnership screening, procurement risk | Converts mixed evidence into transparent risk indicators and recommends reviewer follow-up depth. | Intake forms, screening notes, adverse media snippets | Risk indicator checklist, triage priority, escalation suggestions | Medium | High (overlap with existing risk-scoring tools) | **Specialize** | Must avoid deterministic pass/fail claims. |
| CI-08 | **NarrativeConsistency Review** | Consistency analysis | Analysts, comms risk teams, due diligence reviewers | Compares statements across time/sources for inconsistencies and unresolved questions. | Public statements, filings, interviews, website snapshots | Consistency matrix, contradiction candidates, clarification prompts | Medium | Medium | **Create** | Safe if framed as “consistency analysis,” not deception detection. |
| CI-09 | **AdverseMedia Digestor** | Media signal aggregation | Reputation analysts, due diligence teams | Summarizes adverse media themes, recurrence, and unresolved allegations with sourcing quality notes. | News links, watchlists, date ranges, entity aliases | Thematic digest, allegation status tracker, source caveats | Medium | High (overlap with corporate-reputation agents) | **Merge** | Prefer integration with existing corporate reputation analyst. |
| CI-10 | **CounterpartyDD Brief** | Due diligence support briefs | Deal teams, procurement, partnerships, investor ops | Produces structured due diligence briefs combining known facts, open questions, and risk indicators. | Entity profile, collected evidence, market context notes | DD brief, unresolved issues list, decision-support summary | Low | Medium | **Create** | High value; include mandatory uncertainty section. |
| CI-11 | **VeracityJudge** | Truth/deception adjudication (legacy concept) | N/A (not public-safe as defined) | Legacy concept attempting to classify truthfulness/deception; not suitable for public-safe release. | Statements, transcripts, behavioral claims | Would produce deception verdicts (disallowed) | High | Low | **Hold / Reject** | **HOLD / REPOSITION before launch**; conflicts with guardrails on lie/deception detection. |
| CI-12 | **WorkforceWatch** | Employee monitoring (legacy concept) | N/A (not public-safe as defined) | Legacy monitoring concept with surveillance-like framing; not suitable for public-safe release. | Internal communications/activity logs | Monitoring alerts (disallowed framing) | High | Low | **Hold / Reject** | **HOLD / REPOSITION before launch**; surveillance/employee monitoring not allowed. |
| CI-13 | **FraudVerdict Engine** | Deterministic fraud/guilt determination (legacy concept) | N/A (not public-safe as defined) | Legacy concept attempting guilt/fraud determinations; incompatible with public-safe policy. | Mixed case evidence | Deterministic verdict output (disallowed) | High | Low | **Hold / Reject** | **HOLD / REPOSITION before launch**; replace with non-deterministic risk-indicator support only. |

## 4) Risk notes

- **Low-risk candidates** are generally those focused on structure: timeline reconstruction, evidence organization, and scoped due diligence briefing.
- **Medium-risk candidates** require careful language controls to avoid legal conclusions or deterministic judgments.
- **High-risk candidates** in this roster (CI-11 to CI-13) are intentionally preserved as legacy concepts but are explicitly **not launch-ready** and must remain **HOLD / REPOSITION**.

## 5) Recommended first-launch candidates

Recommended initial set (public-safe, high-value, lower-risk):

1. **ChronoTrace (CI-01)** — timeline reconstruction support.
2. **InvestIQ (CI-02)** — investigation planning and scoping support.
3. **PolicySentry (CI-03)** — policy mapping support (carefully phrased, non-legal-advice).
4. **EvidenceLedger (CI-04)** — evidence organization and provenance packaging.
5. **CounterpartyDD Brief (CI-10)** — due diligence brief generation with uncertainty disclosures.

Not recommended for first launch:
- Any candidate framed around deception/lie detection, surveillance/employee monitoring, legal execution, or deterministic guilt/fraud determination (CI-11, CI-12, CI-13).

## 6) Product evaluation instructions

When Product Assistant evaluates candidates from this file:

1. Treat this file as the **stable source of candidate context**.
2. Confirm candidate status is “candidate only,” not production-ready.
3. Validate guardrail compliance in description, inputs, and outputs.
4. Ensure outputs are positioned as decision support with human review.
5. Require uncertainty/caveat sections for medium-risk candidates.
6. Block escalation of any **HOLD / REPOSITION** candidate until renamed and reframed to public-safe scope.

## 7) Duplicate/overlap review requirement

Before recommending any candidate for launch, Product Assistant must run a **duplicate/overlap review** against existing public marketplace agents and repository agent capabilities:

- Check for functional overlap with existing due diligence, reputation, verification, and policy-support agents.
- Prefer **specialize/merge** over net-new launch when overlap is high.
- Require a clear differentiation statement (unique inputs, outputs, or workflow value).
- Record the dedup decision in the candidate evaluation notes.

**Mandatory note:** Product Assistant must run duplicate/overlap checks against existing public marketplace agents before recommending any candidate for launch.
