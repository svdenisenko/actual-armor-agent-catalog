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
