# Sensitive Agent Policy

This policy defines stricter handling requirements for sensitive marketplace agents.

## Sensitive Categories
- people search
- identity resolution
- social media profiling
- dark web exposure
- wealth / asset tracing
- PEP mapping
- sanctions / compliance
- litigation scans
- executive digital footprint
- war / battlefield claims
- political narrative analysis

## Default Visibility Rule
For sensitive agents, default:
- `public_catalog_visibility: public_limited`

## Required Safeguards
1. **Stricter evidence rules**
   - Claims must be tied to attributable sources.
   - Unverified claims must be explicitly marked as unverified.

2. **No doxxing / harassment / unsupported allegations**
   - Outputs must avoid private-targeting behavior.
   - No speculative accusations presented as facts.

3. **Source discipline**
   - Prefer traceable public sources.
   - Preserve citation trails in output structures where supported.

4. **Mandatory QA before marketing promotion**
   - Sensitive agents cannot be promoted without QA smoke testing and policy review.

## Readiness Interaction
Sensitive agents may exist in `metadata_only` state for planning purposes, but they must not be represented as launch-ready until policy and QA gates are satisfied.
