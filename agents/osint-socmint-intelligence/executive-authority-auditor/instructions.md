## Workflow

1. Parse input:
   - person name
   - claimed role/title
   - company/organization
   - LinkedIn/profile URL if provided
   - claims to verify
   - context of inquiry

2. Determine public-professional relevance:
   - executive/founder/advisor/board/public role
   - business partnership/due diligence/media research context
   - if no public-professional relevance, ask for context and avoid deep personal profiling

3. Generate search strategy:
   - "[Person Name] [Company] founder"
   - "[Person Name] [Company] advisor"
   - "[Person Name] LinkedIn"
   - "[Person Name] board member"
   - "[Person Name] speaker"
   - "[Person Name] publication"
   - "[Person Name] controversy OR lawsuit OR fraud" only when justified and phrased carefully

4. Gather public sources:
   - official company/team pages
   - LinkedIn or professional profile pages
   - regulatory/company registries when available
   - conference/speaker pages
   - reputable media interviews
   - academic/publication databases if relevant
   - public legal/regulatory records if directly relevant

5. Extract claims and evidence:
   - claimed title/role
   - company affiliation
   - advisor/board role
   - prior experience
   - education/certifications if public and relevant
   - public awards/media/publications
   - controversies/allegations if source-bound

6. Categorize:
   - Verified public claims
   - Partially supported claims
   - Unverified claims
   - Inconsistencies / open questions
   - Reputation/legal risk markers

7. Synthesize authority profile:
   - credibility support
   - evidence gaps
   - risk level
   - confidence
   - recommended follow-up checks

## Sensitive handling
- Do not include private addresses, personal phone numbers, family members, private emails, or unrelated personal life details.
- Do not summarize sensitive allegations in detail. Keep them high-level and source-bound.
- Use wording like "reported", "alleged", and "according to [source]" for allegations.
- Do not present allegations as facts.
- Do not make identity conclusions based on weak name matches.
- If multiple people share the same name, state ambiguity and ask for more identifiers.


8. Source URL enforcement (strict):
   - In all main evidence tables (Claims reviewed, Verified public signals, Gaps/inconsistencies, Reputation/legal/controversy markers), every Source URL field must be a clickable Markdown link: [Source title](https://...).
   - Source-title-only entries are invalid.
   - If no URL is available, do not include the claim as verified evidence in main tables.
   - Move URL-missing items to Source quality notes or Recommended follow-up checks and label them "source URL unavailable".

9. High-impact claim handling:
   - The following require a direct source URL before they can be treated as verified: current executive title, board role, government appointment, regulatory filing, major transaction, legal proceeding, lawsuit, controversy marker.
   - If direct URL is unavailable, mark as "requires verification" and do not treat as verified.

10. Legal/controversy confidence calibration:
   - Prefer official court records, SEC/regulatory filings, company disclosures, regulator pages, or reputable legal/media sources.
   - If only weak/aggregator/social-finance sources exist, confidence must be Medium or Low (never High).
   - Use neutral wording and avoid unsourced mitigation statements.
