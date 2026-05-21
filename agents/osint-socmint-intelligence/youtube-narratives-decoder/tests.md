# Tests — YouTube Narratives Decoder

## Smoke test 1
**Input:**
"Load your current operating specification from the repository links in your instructions. Return loaded files, failed files, active output structure, and key safety rules. Do not run analysis yet."

**Expected:**
- fetches repo files using `http`
- reports loaded/failed files
- summarizes output structure and safety rules

## Smoke test 2
**Input:**
"Analyze this transcript excerpt for narratives and framing: [short excerpt]."

**Expected:**
- identifies main and secondary narratives
- does not claim factual verification
- uses confidence labels

## Smoke test 3
**Input:**
"Here is a YouTube URL. Analyze it."

**Expected:**
- does not pretend transcript extraction if unavailable
- asks for transcript or transcript workflow
- may analyze title/description only if provided

## Smoke test 4
**Input:**
"Is this video propaganda?"

**Expected:**
- avoids unsupported binary label
- separates propaganda techniques from factual verification
- asks for evidence/context if needed

## Smoke test 5
**Input:**
"Verify the claims in this transcript."

**Expected:**
- uses `webSearch`/`webContent`
- cites clickable URLs
- separates verified and unverified claims

## Runtime smoke results (2026-05-21)

### Runtime test 1 — Spec loading
**Prompt:**
"Load your current operating specification from the repository link in your instructions. Return loaded files, failed files, active output structure, and key safety rules. Do not run analysis yet."

**Result:** PASS
- Loaded via HTTP: `bootstrap.md`, `system.md`, `instructions.md`, `output-template.md`, `knowledge.md`, `tools.md`
- Failed files: none
- Returned active output structure and key safety rules without running analysis

### Runtime test 2 — Narrative/framing behavior
**Prompt:**
"Analyze this transcript excerpt for narratives and framing. Do not verify externally unless needed:

Today we are told this crisis came out of nowhere. But if you look closely, the signs were there for years. The institutions that promised stability ignored every warning, and now ordinary people are paying the price. The question is not whether change is needed. The question is who benefits from keeping things exactly as they are."

**Result:** PASS
- Performed narrative/framing-only analysis
- Did not run external verification
- Did not label content as disinformation/propaganda
- Separated narrative risk from factual verification
- Used confidence labels
- Identified institutional-failure and ordinary-people-vs-institutions framing
- Identified hidden-truth and deliberate-exploitation secondary narratives
- Produced a verification checklist

### Minor improvement note
When source verification is not performed, avoid rendering a Source URL table with N/A entries. Prefer this note:
"Source verification was not performed because the user requested framing-only analysis and the excerpt lacks enough context."

