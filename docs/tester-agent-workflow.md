# Tester Agent Workflow

## Purpose

Tester Agent validates the real marketplace runtime, not only repository files.

## Inputs

- marketplace agent URL/ID
- repo spec path
- bootstrap URL
- expected behavior
- output template
- smoke test prompts
- forbidden behavior list
- tool expectations

## Responsibilities

Tester Agent should:

1. Open the real AA marketplace agent.
2. Verify runtime loading.
3. Confirm bootstrap behavior.
4. Run smoke prompts.
5. Check output template compliance.
6. Check whether the agent asks for missing inputs when required.
7. Check for hallucinated private context.
8. Check tool usage behavior.
9. Score the result.
10. Produce QA verdict and patch recommendations.

## Minimum Smoke Test Set

- loading test
- normal user task test
- missing input test
- boundary/safety test
- output template compliance test

## QA Report Format

Use:

```text
Agent:
Marketplace URL:
Repo Spec:
Runtime Loading: pass/fail
Behavior Smoke: pass/fail
Output Template: pass/fail
Tool Usage: pass/fail/not_applicable
Private Context Leakage: yes/no
Issues Found:
Recommended Patch:
QA Verdict: pass / patch_required / fail
Next Status:
```

## QA Verdict Rules

### pass
- runtime loads
- behavior matches spec
- output template mostly followed
- no private context leakage
- no critical tool issues

### patch_required
- agent works but needs spec/template/tool/config improvement

### fail
- runtime does not load
- agent ignores core behavior
- leaks private context
- unsafe or unusable behavior

## Status Patch Requirement

Every Tester Agent run should result in a QA/readiness status update in the public repository.
