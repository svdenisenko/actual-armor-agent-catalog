# Agent Prioritization Framework

Use this framework to score draft marketplace agent candidates using repository-grounded criteria.

## Scoring Criteria (1–5 each)

Score each criterion from **1 (low/weak)** to **5 (high/strong)**.

1. **User Value**
2. **Launch Speed**
3. **Differentiation**
4. **Strategic Fit**
5. **Evidence Availability**
6. **QA Readiness**
7. **Engineering Dependency**
8. **Risk / Compliance Sensitivity**

## Directional Guidance

- higher **User Value** is better
- higher **Launch Speed** is better
- higher **Differentiation** is better
- higher **Strategic Fit** is better
- higher **Evidence Availability** is better
- higher **QA Readiness** is better
- lower **Engineering Dependency** is better
- lower **Risk / Compliance Sensitivity** is better

## Priority Model

Calculate:

**Priority Score =**

- User Value
- + Launch Speed
- + Differentiation
- + Strategic Fit
- + Evidence Availability
- + QA Readiness
- - Engineering Dependency
- - Risk / Compliance Sensitivity

## Classification

- **20+** = strong candidate for draft creation
- **14–19** = needs review or better evidence
- **below 14** = do not create yet

## Notes

- Keep scoring conservative and evidence-aware.
- If evidence is weak, score down and document assumptions.
- This framework supports prioritization, not publication decisions.
