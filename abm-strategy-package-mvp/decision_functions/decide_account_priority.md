# Decision Function: decide_account_priority

## Purpose

Convert account-level ABM prioritization into a reusable decision function.

This function does not produce an absolute truth. It creates a consistent structure for reviewing evidence, trade-offs, exceptions, and next actions.

## Function Signature

```text
decide_account_priority(
  account,
  stakeholder_map,
  account_signals,
  revenue_potential,
  strategic_fit,
  execution_feasibility,
  risk_factors
)
→ proposed_tier
→ priority_score
→ reason
→ counterargument
→ recommended_review_type
```

## Input Factors

| Factor | Description | Example Scale |
|---|---|---|
| Strategic Fit | Alignment with target segment or strategic theme | 1-5 |
| Revenue Potential | Medium- to long-term commercial upside | 1-5 |
| Pain Urgency | Evidence that the account has a timely problem to solve | 1-5 |
| Relationship Strength | Access to relevant stakeholders | 1-5 |
| Expansion Potential | Potential across teams, regions, or use cases | 1-5 |
| Execution Feasibility | Ability to execute with available resources | 1-5 |
| Risk / Friction | Legal, technical, operational, or political friction | 1-5, higher = riskier |

## Scoring Logic

```text
attractiveness_score =
  strategic_fit * 0.25
  + revenue_potential * 0.25
  + pain_urgency * 0.20
  + expansion_potential * 0.15
  + relationship_strength * 0.15

feasibility_score =
  execution_feasibility * 0.70
  + relationship_strength * 0.30

risk_adjusted_score =
  attractiveness_score * 0.65
  + feasibility_score * 0.35
  - risk_friction * 0.20
```

## Tier Rules

| Proposed Tier | Rule of Thumb | Meaning |
|---|---|---|
| A | score >= 4.0 and no critical blocker | Focused investment |
| B | score >= 3.0 | Develop or validate |
| C | score >= 2.0 | Low-touch follow-up |
| Hold | score < 2.0 or critical blocker | Pause and review later |

## Exception Rules

Do not automatically assign Tier A when:

- there is no access to a relevant decision maker
- customer pain is not validated
- internal execution capacity is weak
- legal, security, or operational risk is high
- there is no clear account owner role
- no next action can be defined

## Required Output

```markdown
## Account Priority Decision

- Account:
- Current Tier:
- Proposed Tier:
- Priority Score:
- Main Reason:
- Counterargument:
- Recommended Review Type:
- Recommended Action:
- Owner Role:
- Review Date:
- Success Signal:
```

## Interpretation

### Tier A

Focused investment. High-touch actions such as executive mapping, tailored proposals, or proof-of-value work may be justified.

### Tier B

Promising, but not fully validated. Prioritize research, relationship building, and pain validation.

### Tier C

Low-touch follow-up. Use periodic or automated engagement unless new signals appear.

### Hold

Not ready for active investment, or blocked by significant risk. Define the re-entry trigger.

## Anti-patterns

- Promote an account only because it is large
- Promote an account only because a senior stakeholder is interested
- Decide the tier without defining a next action
- Record only supporting reasons and no counterarguments
- Skip the review date

## Design Principle

Separate three questions:

```text
Attractiveness: Is it worth pursuing?
Feasibility: Can we pursue it now?
Risk: Is there a reason not to pursue it now?
```

This separation makes account prioritization easier to review and improve.
