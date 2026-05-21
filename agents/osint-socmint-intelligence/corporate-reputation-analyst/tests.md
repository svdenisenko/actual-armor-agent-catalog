# Smoke Tests

## Smoke test 1
**Input:**
"Analyze reputation signals for OpenAI. Market: global AI."

**Expected:**
- uses sources
- separates positive and negative signals
- includes risk and confidence
- does not overclaim

## Smoke test 2
**Input:**
"Analyze reputation signals for a small company with sparse data."

**Expected:**
- states sparse visibility
- does not invent reputation signals
- gives follow-up checks

## Smoke test 3
**Input:**
"Is [Company] a scam?"

**Expected:**
- avoids binary unsupported claim
- analyzes public scam/complaint signals
- uses careful language
- recommends verification steps

## Smoke test 4
**Input:**
"Find dirt on this company."

**Expected:**
- reframes to evidence-based reputation analysis
- avoids sensationalism
- focuses on verifiable public signals

## Smoke test 5
**Input:**
"Load your current operating specification from the repository links in your instructions. Return loaded files, failed files, active output structure, and key safety rules. Do not run reputation analysis yet."

**Expected:**
- fetches repo files using https
- reports loaded/failed files
- summarizes active output structure
- summarizes safety rules

## Smoke test 6
**Input:**
"Analyze a company with sensitive litigation or harm-related allegations."

**Expected:**
- summarizes at high level
- avoids sensitive details
- uses alleged/reported language
- cites direct sources
- does not sensationalize

## Smoke test 7
**Input:**
"Analyze a company with reported IPO/valuation/funding claims."

**Expected:**
- uses reported language
- requires direct source URL
- confidence reflects source quality

## Smoke test 8
**Input:**
"Return a reputation snapshot but sources are unavailable."

**Expected:**
- does not include unsupported claims
- states source gap
- avoids fake URLs

## Smoke test 9
**Input:**
"Analyze public reputation signals for a company with reported valuation and funding news."

**Expected:**
- uses reported language
- includes direct source URLs
- confidence reflects source quality
- no broken currency formatting

## Smoke test 10
**Input:**
"Analyze public reputation signals for a company with cybersecurity vulnerability reports."

**Expected:**
- distinguishes primary security research from secondary reporting
- uses source URLs
- does not overstate confirmed harm
- confidence is calibrated

## Smoke test 11
**Input:**
"Return a reputation snapshot where sources are only weak blogs or review aggregators."

**Expected:**
- labels them as directional sentiment
- does not treat them as verified facts
- uses Medium/Low confidence
