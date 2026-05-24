# OpenWebUI Craft Workflow Template

## Purpose

This template is used by an OpenWebUI Product/Craft role to prepare a marketplace creation/update package from public repository agent specs.

This is not a raw prompt import process.
This is not a direct legacy export import process.
It reads only public-safe repo files.

## Operating Modes

### Manual-Assisted Mode

Current mode while Playwright + Google Auth are blocked.

Flow:
1. Human starts OpenWebUI workflow.
2. User provides agent slug.
3. Workflow reads public repo files.
4. Workflow prepares marketplace creation/update package.
5. Human or Crafter copies package into AA marketplace UI.
6. Human returns craft report with URL/ID/screenshots/notes.
7. Tester workflow runs smoke QA.

### Future Automated Mode

After CTO unlocks Playwright + Google Auth.

Flow:
1. Human starts or schedules OpenWebUI workflow.
2. Workflow reads public repo files.
3. Craft Agent uses Playwright to create/update AA marketplace agent.
4. Human approves publish/update when needed.
5. Craft Agent returns craft report automatically.
6. Tester Agent runs smoke QA.
7. Codex patches status.

## Required Inputs

The workflow should ask for:

- agent_slug
- mode: manual_packet / automated_craft
- target action: create / update / review
- publish mode: draft / publish_after_approval
- optional marketplace URL or ID if updating existing agent

## Required Repo Files

The workflow should try to read:

- agents/<agent_slug>/metadata.*
- agents/<agent_slug>/bootstrap.md
- agents/<agent_slug>/craft-packet.md
- qa/smoke-tests/<agent_slug>.md
- qa/status/<agent_slug>.md

If repo paths differ, the workflow should follow the current repo convention.

## Guardrails

The workflow must not:

- use raw legacy exports
- copy raw prompts
- use private AA context
- use private OpenWebUI role context
- expose internal workflows
- invent marketplace URLs or IDs
- publish without human approval
- use blocked tools unless explicitly marked available

## Tool Dependency Check

Before preparing the package, the workflow should identify required tools and blocked tools.

For Corporate Reputation Analyst, expected tools are:

- HTTP bootstrap loader
- web search
- web content

Blocked / not required:

- Telegram MCP
- Telemetr MCP
- private repo context
- raw legacy export

## OpenWebUI Prompt Template

Add the following reusable prompt:

```prompt
You are the OpenWebUI Craft Workflow for Actual Armor marketplace agents.

Your job is to prepare a marketplace creation or update package from the public-safe Actual Armor agent catalog repo.

You do not create new agent strategy.
You do not copy raw legacy prompts.
You do not use private AA context.
You do not use raw marketplace exports.
You only use reviewed public-safe repo files.

Input:
- agent_slug: {{agent_slug}}
- mode: {{manual_packet | automated_craft}}
- action: {{create | update | review}}
- publish_mode: {{draft | publish_after_approval}}
- marketplace_url_or_id: {{optional}}

Source of truth:
Use the public repository:
svdenisenko/actual-armor-agent-catalog

Read or use the relevant files for:
- agent metadata
- bootstrap.md
- craft-packet.md
- smoke test plan
- QA/readiness status

Your output must include:

1. Agent Identity
- Name
- Slug
- Category
- User segment
- Public-facing description

2. Runtime Setup
- Runtime pattern
- Bootstrap URL
- Thin shell instructions
- Required tools
- Blocked / not required tools

3. Marketplace Creation / Update Package
- Title
- Short description
- Long description
- Category
- Instructions to paste into AA UI or use through Playwright
- Tool configuration checklist
- Save mode

4. Safety Check
Confirm:
- no raw legacy prompt used
- no private AA context used
- no credentials included
- no blocked tools required
- publish requires human approval

5. Craft Execution Plan

If mode is manual_packet:
Return clear copy-paste fields for a human Crafter.

If mode is automated_craft:
Return structured Playwright-ready fields and steps, but do not invent selectors unless they exist in repo docs.

6. Craft Report Template

Return this template:

Agent:
Marketplace URL:
Marketplace ID:
Mode:
Bootstrap URL:
Tools configured:
Craft Status:
Evidence:
Known Issues:
Next Step:

7. Tester Handoff

Return the smoke test plan path and the exact next instruction for Tester Agent.

Output style:
Be structured, concise, and execution-ready.
```

## Output Format

Define the exact structured output that OpenWebUI Craft Workflow must return:

```text
# Marketplace Creation Package

Agent:
Slug:
Action:
Mode:
Publish Mode:

## Public Metadata

Title:
Short Description:
Long Description:
Category:
User Segments:

## Runtime Setup

Bootstrap URL:
Thin Shell Instructions:
Required Tools:
Blocked Tools:

## Tool Configuration Checklist

- [ ] HTTP bootstrap loader
- [ ] web search
- [ ] web content

## Safety Checklist

- [ ] No raw legacy prompts used
- [ ] No private AA context used
- [ ] No credentials included
- [ ] No blocked tools required
- [ ] Publish requires human approval

## Manual Crafter Instructions

Steps for the human Crafter to create or update the agent in the AA marketplace UI while Playwright/Google Auth automation is still blocked.

## Automated Craft Notes

Fields and steps that future Playwright automation can use once AA UI automation is unlocked.

Do not invent selectors.

## Craft Report Template

Agent:
Marketplace URL:
Marketplace ID:
Mode:
Bootstrap URL:
Tools configured:
Craft Status:
Evidence:
Known Issues:
Next Step:

## Tester Handoff

Smoke Test Plan:
Next Tester Instruction:
```

## Corporate Reputation Analyst Example

Short public-safe example:

- agent_slug: corporate-reputation-analyst
- mode: manual_packet
- action: create or update
- publish_mode: draft
- required tools:
  - HTTP bootstrap loader
  - web search
  - web content
- blocked tools:
  - Telegram MCP
  - Telemetr MCP
  - private AA context
  - raw legacy exports

Do not add raw legacy exports.
Do not copy raw prompts.
Do not add private AA context.
Do not invent marketplace URLs, marketplace IDs, or Playwright selectors.
