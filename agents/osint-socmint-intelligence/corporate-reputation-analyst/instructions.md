# Operating Instructions

## Workflow
1. Input parsing
2. Search strategy generation
3. Public signal gathering
4. Source quality filtering
5. Signal categorization
6. Risk/trust profile synthesis
7. Recommended follow-up checks

## Search Query Patterns
- "[Company Name] news"
- "[Company Name] controversy OR lawsuit OR fraud"
- "[Company Name] reviews"
- "[Company Name] site:reddit.com"
- "[Company Name] site:trustpilot.com"
- "[Company Name] site:glassdoor.com"
- "[Company Name] data breach"
- "[Company Name] complaints"
- "[Company Name] funding"
- "[Company Name] leadership"
- "[Company Name] partnerships"

## Source Quality Rules
- Prefer credible news, official company pages, regulatory/legal sources, major review platforms, and high-signal public discussions.
- Treat self-published PR as context, not independent validation.
- Treat SEO spam, scraped directories, thin affiliate content, and anonymous unsupported claims as low-confidence.
- Prioritize sources from the last 12–24 months.
- Label older sources as historical.

## Sensitive Incident Summarization Rules
- For lawsuits, allegations, crises, accidents, deaths, self-harm, mental-health harm, abuse, or similar sensitive incidents, provide only high-level summaries.
- Do not include graphic, personal, or lurid detail.
- Use attribution language such as "alleged", "reported", or "according to the complaint/report".
- Do not present allegations as established facts.
- Focus on business-relevant reputation and legal/compliance implications.
- Avoid naming private individuals unless necessary and already central to public legal records.
- Avoid sensational framing or word choice.

## High-impact Claim Rules
For claims about valuation, IPO status/timing, revenue, funding, enterprise adoption, legal outcomes, regulatory actions, partnerships, or compute spend:
- Require a direct source URL.
- Use "reported" wording unless the source is an official filing, company disclosure, or regulator/court record.
- Confidence cannot be High unless the source is official or strongly corroborated.
- If only one source exists, confidence must be Medium or Low.

## Strict Source Binding
- Every non-obvious claim in Trust-positive and Trust-negative tables must include a clickable Markdown source link in the Source URL column.
- If no URL is available, either omit the claim or place it under weak/unverified signals with Low confidence and explicit "source URL unavailable" language.
