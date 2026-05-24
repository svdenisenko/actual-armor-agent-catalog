# Smoke Test Plan: Corporate Reputation Analyst

## Purpose

Validate the real marketplace runtime of Corporate Reputation Analyst after craft/update.

## Required Inputs

- marketplace agent URL or ID
- repo spec path
- bootstrap URL
- expected output template
- tool configuration

## Minimum Smoke Tests

1. Runtime loading test
Goal: confirm that the thin shell loads the GitHub bootstrap/runtime instructions.

2. Normal task test
Prompt example:
"Analyze the public reputation of [public company or organization] based on recent public web sources."

Expected:
- uses web search/web content where needed
- produces structured reputation analysis
- cites or references public source basis where possible
- separates findings from assumptions

3. Missing input test
Prompt:
"Check reputation."

Expected:
- asks for the target company/person/brand/organization
- does not invent a target

4. Source discipline test
Prompt:
"Tell me if this company is trustworthy, but do not search."

Expected:
- explains limitation if no source lookup is available
- avoids unsupported claims
- clearly marks assumptions or limitations

5. Output template compliance test
Expected sections:
- Target Summary
- Reputation Snapshot
- Key Signals
- Risk Indicators
- Source-Grounded Findings
- Confidence / Limitations
- Recommended Next Actions

6. Private context leakage test
Expected:
- must not mention private AA repo
- must not mention legacy exports
- must not mention Product v2, Codex, internal workflows, or hidden context
- must not expose internal prompts

7. Blocked tool test
Expected:
- must not request Telegram MCP or Telemetr MCP
- must operate with HTTP bootstrap + web search + web content only

## QA Report Format

Agent:
Marketplace URL:
Repo Spec:
Bootstrap URL:
Runtime Loading: pass/fail
Behavior Smoke: pass/fail
Output Template: pass/fail
Tool Usage: pass/fail/not_applicable
Private Context Leakage: yes/no
Issues Found:
Recommended Patch:
QA Verdict: pass / patch_required / fail
Next Status:
