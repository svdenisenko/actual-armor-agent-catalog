# CMO Lifecycle Agent Shortlist — Planning Only

**Date:** 2026-05-28  
**Source:** raw AAF inventory classification for `catalog/imports/aaf-agent-inventory-2026-05-28.csv`  
**Audience:** CMO, Product, QA, and lifecycle campaign planning  
**Decision state:** internal planning support only; not launch approval

## 1. Executive summary

This shortlist converts the raw AAF inventory classification into conservative lifecycle planning buckets for CMO SendPulse architecture work. It is **not** a public catalog, launch list, or approval to promote any individual agent.

The imported AAF inventory contains **88 agents** discovered from `chat@actualarmor.com`. The classification states that **0 agents are confirmed public/live**, **0 public AAF URLs are verified**, every `aaf_public_url` is `UNKNOWN`, and every record requires prompt review. Therefore every candidate below remains planning-only with the status bundle:

`DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET`

CMO may use these buckets to sketch lifecycle education arcs, audience segmentation, nurture sequences, and Product verification requests. CMO must not write “try this agent now,” “use this agent,” “available in AAF,” “live,” “launched,” “QA passed,” or any direct agent CTA until Product verifies public/live status, usable AAF link, QA state, prompt safety, and public-safe copy.

## 2. CMO usage rules

1. **Use this document for campaign architecture only.** Treat bucket names as themes for lifecycle planning, not as public claims about available tools.
2. **Do not promote raw inventory.** Raw imported agents are discovery-only and are not canonical `LIVE_IN_AAF` catalog records.
3. **Do not invent URLs.** Every raw imported agent has `aaf_public_url = UNKNOWN`; do not add links or link-like CTAs.
4. **Do not imply availability.** No candidate below may be described as live, public, launched, ready, verified, QA-approved, or user-accessible.
5. **Use workflow-level language.** Until verification, CMO may plan generic educational CTAs such as “learn the workflow,” “review the checklist,” “see how analysts structure this process,” or “join the waitlist/updates,” if Product approves that campaign frame.
6. **Ask Product for a verification batch.** Select 5–10 priority concepts from these buckets for Product, QA, and safety review before any agent-level lifecycle copy is drafted.
7. **No final SendPulse email copy yet.** This document supports lifecycle map creation and Product handoff only.

## 3. Lifecycle campaign buckets

### 3.1 OSINT / investigation activation

**Planning theme:** introduce structured investigation workflows, source mapping, timeline reconstruction, evidence organization, and analyst training without promising automated investigation outcomes.

| Candidate agent | Why it may be useful for lifecycle planning | Status | Safe internal planning CTA idea | User-facing CTA rule | Do-not-claim notes |
|---|---|---|---|---|---|
| InvestIQ | Maps to investigation scoping, hypotheses, source plans, and review checkpoints; useful for onboarding analysts to responsible investigation planning. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan an “investigation planning checklist” nurture step for Product review. | Do not invite users to try InvestIQ until public/live status and a usable AAF link are verified. | Do not claim end-to-end investigation, target profiling, hidden facts, or legal conclusions. |
| ChronoTrace | Lifecycle-friendly concept for reconstructing timelines from user-provided and public-safe sources; useful as a workflow education anchor. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Draft architecture for a “turn scattered events into a review chronology” education module. | Do not use a public “try now” CTA unless Product confirms the catalog status, AAF link, and CTA constraints. | Do not claim the raw imported record is live/public; avoid certainty beyond sourced chronology support. |
| OSINT Sensei | Educational OSINT micro-learning concept; lower-risk planning candidate if framed as methodology training. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan an onboarding sequence around OSINT terminology, source discipline, and reporting hygiene. | Use only generic learning CTAs until Product verifies public-safe availability. | Do not teach evasion, stalking, identity targeting, or covert surveillance. |
| Learning Report Generator | Could support media narrative lifecycle education and structured learning reports if prompt safety is confirmed. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan an internal “how to document narrative lifecycle findings” content block. | No agent-level CTA until verified. | Do not claim forensic certainty, debunking authority, or platform access beyond approved public-safe sources. |
| OSINT Grandmaster | Broad OSINT concept may help frame advanced workflow segmentation, but needs strong safety review due to scope. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Use as a Product review candidate for whether a broad OSINT training concept should be narrowed. | Do not mention publicly until renamed/reframed and approved. | Do not imply surveillance, target dossiers, private data access, or identity investigation capabilities. |

### 3.2 Telegram / narrative intelligence activation

**Planning theme:** help CMO map a lifecycle arc around channel strategy, content analysis, audience understanding, and narrative monitoring while avoiding surveillance, covert monitoring, or claims of detecting wrongdoing.

| Candidate agent | Why it may be useful for lifecycle planning | Status | Safe internal planning CTA idea | User-facing CTA rule | Do-not-claim notes |
|---|---|---|---|---|---|
| Telegram Narrative Monitor | Natural fit for a narrative intelligence education sequence about mentions, sentiment, and emerging themes. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “monitor narratives without overclaiming certainty” lifecycle module. | No user-facing Telegram monitoring CTA until Product verifies safe scope, status, and link. | Do not claim bot detection, covert monitoring, surveillance, or verified influence operations. |
| Competitor Insight Analyst | Could support a marketing operations sequence around ethical competitive benchmarking of public Telegram channels. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a Product review brief for public-channel benchmarking positioning. | Do not say users can analyze competitors until verified. | Do not imply private competitor access, scraping beyond approved tools, or hidden intelligence. |
| TeleBoost Strategist | Useful planning concept for Telegram channel growth education if kept to legitimate channel metrics and content improvements. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Draft lifecycle bucket for “turn channel metrics into content experiments.” | No direct CTA until verified. | Do not claim guaranteed growth, manipulation, spam tactics, or monetization outcomes. |
| Telegram Audience Insights & Content Tuner | Planning candidate for audience profile and content strategy lifecycle messaging. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan an internal “audience insight to editorial calendar” campaign step. | Do not invite users to paste channel data into an agent until link/status are verified. | Do not claim demographic certainty, personal identity inference, or private audience data access. |
| Telegram Engagement Strategist | Could support community management education if copy stays on public, ethical engagement practices. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “responsible engagement loop” nurture section. | No public agent CTA until approved. | Do not claim automated engagement, platform manipulation, or compliance clearance. |

### 3.3 YouTube / media analysis activation

**Planning theme:** educate users on summarizing, decoding, and analyzing video/media narratives without presenting outputs as truth adjudication or propaganda determinations.

| Candidate agent | Why it may be useful for lifecycle planning | Status | Safe internal planning CTA idea | User-facing CTA rule | Do-not-claim notes |
|---|---|---|---|---|---|
| The YouTube Summarizer | Practical lifecycle concept for turning long videos into structured notes; likely understandable for broad audiences after review. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan an educational CTA around “summarize before you analyze.” | Do not publish “summarize this video now” agent CTA until verified. | Do not claim transcript access works universally or that summaries are error-free. |
| YouTube Narratives Decoder | Useful for a media literacy sequence about identifying main narratives and framing in public videos. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “decode framing, then check sources” lifecycle step. | No direct agent CTA until public/live link is verified. | Do not claim hidden true meaning, psychological certainty, or definitive influence intent. |
| YouTube Narrative Intelligence Analyst | Candidate for advanced media analysis lifecycle planning; requires extra safety review due to propaganda/security framing. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Use internally to define an advanced “media discourse review” segment. | Do not use in emails until Product approves public-safe name, scope, and link. | Do not claim propaganda verdicts, military/security intelligence, or hidden actor attribution. |
| YouTube Defense Interview Analyst | May inform a specialized media-analysis lifecycle pathway, but defense/security positioning makes it high risk. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Put in Product review backlog rather than first CMO batch. | Do not use publicly yet. | Do not claim defense expertise, war-claim verification, or authoritative security assessment. |
| GeoNarrative Insight Analyst | May support multimodal narrative education, but geopolitical framing requires careful review before any lifecycle use. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Capture as a possible advanced media-analysis concept for safety review. | No public CTA. | Do not claim geopolitical truth, propaganda proof, geolocation certainty, or intelligence-grade conclusions. |

### 3.4 disinformation / claim-checking activation

**Planning theme:** build a lifecycle education arc around media literacy, claim decomposition, source checking, and uncertainty labeling. Avoid “truth machine,” guilt, deception, bot, or propaganda verdicts.

| Candidate agent | Why it may be useful for lifecycle planning | Status | Safe internal planning CTA idea | User-facing CTA rule | Do-not-claim notes |
|---|---|---|---|---|---|
| Student Claim Checker | Strong education/onboarding candidate for step-by-step claim verification and digital literacy. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “check one claim in five steps” education module. | Do not say students/users can use the agent until verified. | Do not claim definitive truth, plagiarism verdicts, or guaranteed detection. |
| Disinfo Sensei | Useful education concept for media literacy, source verification, and critical thinking. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “learn disinformation patterns safely” onboarding path. | Use only generic education CTAs until Product verifies. | Do not teach manipulation tactics as operational guidance; avoid political persuasion claims. |
| The Truth Scanner | Potentially compelling but risky name/framing; useful only as a Product review item for safer claim-checking positioning. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Ask Product whether to rename/reframe as “claim review assistant” or similar. | Do not use in user-facing emails yet. | Do not claim to determine truth, credibility scores, deception, or factual finality. |
| The Scalpel | Could support atomic claim analysis and source checking if renamed/reframed and safety-reviewed. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan as an internal candidate for claim decomposition workflow architecture. | No user-facing CTA until approved. | Do not claim influence operation detection, proof of falsehood, or authoritative debunking. |
| Digital Psychology Analyst | Useful for teaching language/framing analysis; must avoid mind-reading or manipulation certainty. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “identify emotional framing cues” lifecycle lesson. | No direct CTA. | Do not claim psychological diagnosis, intent detection, or manipulator identification. |

### 3.5 PR / reputation monitoring activation

**Planning theme:** develop lifecycle education around brand monitoring, pitch quality, crisis preparation, and reputation response planning without claiming continuous monitoring, crisis detection guarantees, or verified public availability.

| Candidate agent | Why it may be useful for lifecycle planning | Status | Safe internal planning CTA idea | User-facing CTA rule | Do-not-claim notes |
|---|---|---|---|---|---|
| PR Sensei | Clear onboarding concept for PR methodology, media pitching, crisis communication, and brand strategy education. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “PR basics for analysts/founders” nurture sequence. | Do not claim the PR Sensei agent is available until verified. | Do not imply guaranteed coverage, journalist response, or crisis prevention. |
| PR Architect | Practical concept for press releases, media pitches, and official statement drafting after copy review. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “draft a better public statement” workflow education block. | No “draft with this agent” CTA until link/status are verified. | Do not claim AP/legal/compliance approval or suitability for regulated disclosures. |
| Pitch Critic | Useful lifecycle candidate for pitch improvement education and subject-line critique. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “before you send the pitch” checklist. | No direct agent CTA until verified. | Do not claim journalist simulation accuracy or guaranteed press coverage. |
| Corporate Reputation Analyst | Strong conceptual fit for reputation monitoring lifecycle; requires safety review due to OSINT/public signal framing. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan an internal “public signal review” campaign bucket for Product verification. | Do not say it monitors brands for users until verified. | Do not claim real-time monitoring, comprehensive coverage, or wrongdoing findings. |
| Global Brand Sentiment Tracker | Useful PR lifecycle theme for media/social sentiment education, but “real-time” claims need verification. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “from sentiment signals to response options” campaign segment. | No public CTA or real-time availability claim until Product verifies. | Do not claim continuous tracking, exhaustive global coverage, or sentiment certainty. |
| Reputation Guardian | Candidate for reputation-risk response planning if framed as strategic support, not automated protection. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “reputation response checklist” lifecycle step. | No direct CTA until verified. | Do not claim it protects reputation, prevents crises, or resolves legal/PR risk. |

### 3.6 due diligence / corporate risk activation

**Planning theme:** map an executive/corporate risk education path for document review, red-flag triage, and diligence workflow design. This bucket needs the strictest copy review because many records touch legal, compliance, sanctions, PEP, identity, asset, litigation, or fraud-risk topics.

| Candidate agent | Why it may be useful for lifecycle planning | Status | Safe internal planning CTA idea | User-facing CTA rule | Do-not-claim notes |
|---|---|---|---|---|---|
| Strategic Red Flag Summarizer | Useful as a safe-ish workflow concept for compressing diligence materials into review questions if framed cautiously. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “summarize diligence red flags for human review” architecture note. | No user-facing CTA until verified. | Do not claim legal conclusions, fraud findings, guilt, or investment advice. |
| Deal Room Compliance Dossier Agent | Potential lifecycle theme for M&A diligence preparation, but compliance framing is high risk. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Ask Product whether a generic “diligence document checklist” version is public-safe. | Do not mention as available to users. | Do not claim KYC/AML clearance, legal compliance, risk scores, or regulatory advice. |
| Target Company Litigation Scan Agent | Useful Product review candidate for litigation-aware diligence workflows, but legal topic requires careful constraints. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan only a generic “public records review questions” lifecycle placeholder. | No public CTA. | Do not claim legal analysis, case outcome prediction, or complete litigation search. |
| Supply Chain & Partner Sanctions Check | Might support vendor-risk lifecycle education after compliance/legal review. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a Product handoff for whether sanctions-related content can be safely referenced at all. | Do not use in lifecycle emails yet. | Do not claim sanctions screening, compliance clearance, watchlist coverage, or legal advice. |
| Hidden Distress Indicator Agent | Could inform corporate risk education if reframed away from deterministic scoring. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a cautious “signals to questions, not conclusions” due diligence module. | No direct CTA until reviewed. | Do not claim prediction, financial distress determination, or exhaustive alternative-data coverage. |
| Pre-Viral Controversy Alert Agent | PR/corporate risk crossover; useful as a planning theme but high-risk due to monitoring and prediction language. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Use internally to map “early signal review” copy constraints. | No public CTA. | Do not claim real-time alerts, controversy prediction, surveillance, or crisis prevention. |

### 3.7 education / sensei onboarding

**Planning theme:** introduce lower-commitment educational sequences that teach methods, vocabulary, and checklists. Even education agents still need prompt and copy review before public mention.

| Candidate agent | Why it may be useful for lifecycle planning | Status | Safe internal planning CTA idea | User-facing CTA rule | Do-not-claim notes |
|---|---|---|---|---|---|
| OSINT Sensei | Strong fit for introductory OSINT methodology education and source-discipline onboarding. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan first-touch education around “what responsible OSINT is and is not.” | Do not invite users to start a session until verified. | Do not provide covert surveillance, doxxing, stalking, or identity-targeting guidance. |
| PR Sensei | Strong fit for PR lifecycle onboarding and founder/marketer education. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “PR fundamentals” welcome track. | No direct CTA until verified. | Do not promise media coverage or crisis outcomes. |
| Disinfo Sensei | Good education concept for media literacy and critical thinking if politically neutral and safety-reviewed. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “spot patterns, verify claims” learning path. | No direct CTA until verified. | Do not train persuasion, manipulation, harassment, or partisan targeting. |
| Propaganda Sensei | Possible advanced media literacy concept, but name and politics-adjacent framing require careful review. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Keep as a later-stage educational concept pending Product naming review. | Do not use in first campaign wave. | Do not claim definitive propaganda identification or political neutrality without review. |
| AI Detection Sensei | Useful educational sequence about AI-generated media/text limitations and responsible uncertainty language. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan an “AI detection is probabilistic” lesson. | No direct CTA until verified. | Do not claim reliable AI detection, deepfake certainty, or academic misconduct determination. |
| Plagiarism Sensei | Education concept for citation, paraphrasing ethics, and academic integrity; requires careful academic-integrity guardrails. | `DISCOVERY_ONLY` / `NEEDS_PUBLIC_LINK` / `NEEDS_COPY_REVIEW` / `NEEDS_PROMPT_REVIEW` / `DO_NOT_USE_IN_EMAILS_YET` | Plan a “cite, paraphrase, and disclose responsibly” onboarding module. | No direct CTA until verified. | Do not promise plagiarism avoidance, academic compliance, or bypassing detection. |

## 4. Do not use yet

The following raw inventory themes should **not** appear in lifecycle emails until Product, QA, legal/safety, and CMO complete a separate approval pass. They may be tracked internally for triage, rename/merge/retire decisions, or future public-safe repositioning.

### 4.1 High-risk agents and themes

| Agent or theme | Risk reason | Planning disposition |
|---|---|---|
| OSINT War Claim Verifier, Senior_GEOINT_Analyst, GeoNarrative Insight Analyst, YouTube Defense Interview Analyst | Military, war-claim, geolocation, defense/security, or geopolitical assertions can create safety and accuracy risks. | Keep out of lifecycle campaigns; Product/safety review only. |
| Real-Time Sanctions Monitor, Supply Chain & Partner Sanctions Check, Political Exposure & PEP Network Mapping Agent | Sanctions, PEP, watchlist, and compliance topics risk legal/regulatory overclaims. | Do not use in CMO emails without legal/compliance-approved copy constraints. |
| Wealth & Asset Tracing Agent, UBO Shell Company Unmasking Agent, Covert Corporate Alliance Tracker | Asset tracing, UBO, hidden relationship, and covert alliance framing can imply invasive investigation or legal conclusions. | Internal diligence review only; likely needs repositioning. |
| Deep Web & Dark Web Exposure Scan Agent, Telegram Scanner | Dark web and deep reconnaissance framing risks unsafe targeting, privacy, and source-access claims. | Do not use in lifecycle emails. |
| The Visual Profiler, SOCMINT Identity Analyst, Executive Digital Footprint Auditor, Social Identity Auditor, Founding Team OSINT Analyst | Identity/person investigation and digital footprint mapping can imply stalking, doxxing, or profiling. | Do not use until rewritten around consent, public-safe materials, and human review. |
| Network Influence Analyst, Disinformation Threat Detector, OSINT Disinformation Analyst, Twitter Narrative Analysis Agent | Botnet/CIB/disinformation detection can imply deterministic attribution or coordinated-behavior proof. | Use only as internal safety review candidates; no public claims. |
| Hidden Distress Indicator Agent, Third-Party Reputational Contagion Monitor, Strategic Scenario Synthesizer | Deterministic scoring, forecasting, contagion, or prediction language can overstate reliability. | Reframe as “signals and questions” before any CMO use. |
| Counter-Messaging Generator, Financial Counter-Narrative Analyst | Counter-messaging and counter-narrative tools risk persuasion, political manipulation, or market misinformation claims. | Do not use in lifecycle emails until scope is clearly neutral, educational, and non-manipulative. |
| AI Scanner, The Truth Scanner, Narrative Watchdog | Names/descriptions can imply definitive detection, truth adjudication, or hidden-agenda identification. | Rename/reframe before any public-facing mention. |

### 4.2 Internal/test-looking agents

The classification flags internal/test-looking records. These should not be used in CMO emails unless Product explicitly converts them into public-safe catalog entries with public-safe names, descriptions, QA status, and verified links.

Examples to keep out of campaigns for now include:

- InvestIQ, when sourced only from the raw private inventory record rather than the canonical repo-backed catalog record.
- Global OSINT.
- Social Media Scanner.
- Telegram Scanner.
- LinkedIn Profile Viewer.
- Any record with blank category, “personal digital detective,” “cyber-stalker,” anonymous profile viewing, private edit-only URLs, or target-centric reconnaissance framing.

### 4.3 Duplicate and overlap risks

The classification marks most records as duplicate/overlap risks. CMO should not build individual agent campaigns around clusters until Product decides whether to merge, rename, retire, or promote one canonical public-safe concept.

Priority overlap clusters for Product decision:

- Telegram analytics/growth/monetization agents.
- YouTube/media narrative analysis agents.
- PR/reputation/pitch agents.
- Disinformation/claim-checking/AI detection agents.
- Corporate diligence/risk/compliance agents.
- Twitter/LinkedIn lead generation and social selling agents.

## 5. Recommended CMO next step

1. Draft SendPulse campaign architecture using **buckets**, not individual “try this agent now” claims.
2. Use generic workflow CTAs until public/live links are verified, such as:
   - “Learn the workflow.”
   - “Review the checklist.”
   - “See the analyst process.”
   - “Get the next workflow update.”
3. Do not create final SendPulse email copy yet.
4. Send Product a proposed verification batch of 5–10 priority agents. Recommended first-pass candidates because they are lifecycle-friendly if safely verified:
   - OSINT Sensei
   - Student Claim Checker
   - The YouTube Summarizer
   - PR Sensei
   - PR Architect
   - Pitch Critic
   - Corporate Reputation Analyst
   - Global Brand Sentiment Tracker
   - ChronoTrace
   - Strategic Red Flag Summarizer
5. Keep high-risk compliance, person-investigation, sanctions, dark web, military/war-claim, identity, and deterministic scoring concepts out of user-facing emails until a separate review approves a safe public framing.

## 6. Recommended Product next step

1. Verify public/live status and usable AAF public links for the top CMO candidates.
2. Confirm whether each candidate is public-safe, limited-test only, internal-only, needs rename/reframe, duplicate/merge, or should be retired.
3. Review prompts and safety behavior before any CMO copy draft.
4. Mark which agents can be safely referenced in lifecycle emails and document allowed CTA language.
5. Promote only verified, repo-backed records into the canonical catalog. Do not mark any imported raw agent as `LIVE_IN_AAF` without evidence, QA status, and a public AAF link.

## 7. Guardrails

- Raw inventory is not the canonical public/live catalog.
- This shortlist is CMO planning support, not campaign launch approval.
- All raw imported candidates remain discovery-only and not email-ready.
- CMO can use this shortlist for lifecycle architecture and Product verification requests only.
- CMO must not claim availability, QA pass, launch status, public status, direct CTA availability, or user access without verified catalog status and a usable AAF public link.
- CMO must not say “try this agent now” for any candidate in this document.
- CMO must not invent URLs, public status, categories, agent capabilities, prompt quality, source coverage, or safety outcomes.
- Product, QA, and safety review must happen before agent-level public copy, campaign copy, or SendPulse CTAs are drafted.
