# Craft Packet: Corporate Reputation Analyst

## Purpose

This packet gives a human Crafter or future Craft Agent the exact public-safe instructions needed to create or update the Corporate Reputation Analyst agent in the Actual Armor marketplace.

## Agent

- Name: Corporate Reputation Analyst
- Category: Reputation / OSINT / Brand Risk
- User segments: B2B, founders, executives, brand/PR teams, analysts, investor-facing teams

## Runtime Pattern

AA thin shell agent
→ HTTP tool
→ raw GitHub bootstrap.md
→ runtime instructions / output template / knowledge / tools

## Required Tools

- HTTP bootstrap loader
- web search
- web content

## Blocked / Not Required Tools

- Telegram MCP
- Telemetr MCP
- private AA context
- internal marketplace exports
- raw legacy prompts

## Marketplace Setup Notes

- Public-facing title: **Corporate Reputation Analyst**
- Short description: Analyze public reputation signals for companies and leaders using source-grounded web research.
- Suggested long description:
  - Corporate Reputation Analyst helps teams evaluate public-facing trust and reputation signals for a company, founder, executive, or brand. It uses web-searchable public sources to produce a structured snapshot of positive and negative signals, potential risk indicators, confidence levels, and practical next steps. It should stay source-grounded, separate findings from assumptions, and avoid unsupported or defamatory claims.
- Thin shell behavior:
  - Configure the marketplace agent as a thin shell that first loads runtime instructions from the public bootstrap URL, then follows the linked public-safe spec components.
- Bootstrap URL:
  - Placeholder format: `https://raw.githubusercontent.com/<org>/<repo>/<branch>/agents/osint-socmint-intelligence/corporate-reputation-analyst/bootstrap.md`
  - Repo-derived default (if using this repository and default branch): `https://raw.githubusercontent.com/svdenisenko/actual-armor-agent-catalog/main/agents/osint-socmint-intelligence/corporate-reputation-analyst/bootstrap.md`
- Expected tool setup:
  - `http` (HTTP bootstrap loader)
  - `webSearch`
  - `webContent`
- Save mode:
  - Save as **draft** first.
  - Publish only after human approval.

## Expected Behavior

The agent should help users assess public-facing reputation signals for a company, founder, executive, brand, or organization using source-grounded web research.

Expected output should include:

- target summary
- public reputation snapshot
- key public signals
- risk indicators
- source-grounded findings
- confidence / limitations
- recommended next actions

## Craft Output Report

The Crafter or Craft Agent should return:

Agent:
Marketplace URL:
Marketplace ID:
Mode: created / updated / draft / published
Bootstrap URL:
Tools configured:
Craft Status:
Evidence:
Known Issues:
Next Step:
