# Decision Function: select_abm_play

## Purpose

Select the appropriate ABM play after account priority has been reviewed.

A tier is not the end of the decision. A tier should trigger a specific next action, owner role, success signal, and review timing.

## Function Signature

```text
select_abm_play(
  proposed_tier,
  relationship_strength,
  pain_urgency,
  executive_access,
  execution_feasibility,
  risk_friction
)
→ recommended_play
→ next_action
→ owner_role
→ success_signal
→ review_timing
```

## Play Types

| Play | When to Use | Primary Goal |
|---|---|---|
| Executive Mapping | High-priority account but weak decision-maker access | Identify the buying path |
| Discovery Sprint | Pain or urgency is unclear | Validate the problem |
| Tailored Proposal | Fit and pain are validated | Advance a specific proposal |
| Proof of Value | Customer needs evidence before broader commitment | Validate impact in a controlled scope |
| Stakeholder Warming | Attractive account but relationship is weak | Build relationship first |
| Expansion Mapping | Existing access but expansion path is unclear | Identify additional opportunities |
| Risk Review | Attractive account but execution risk is high | Resolve blockers before investing more |
| Nurture | Not ready for active pursuit | Maintain low-cost engagement |
| Deprioritize | Low fit or low feasibility | Stop active investment for now |

## Selection Rules

### Rule A: Tier A + Strong Pain + Good Access

```text
if proposed_tier = A
and pain_urgency >= 4
and relationship_strength >= 4
then Tailored Proposal or Proof of Value
```

### Rule B: Tier A + Weak Executive Access

```text
if proposed_tier = A
and executive_access <= 2
then Executive Mapping
```

### Rule C: Tier B + Unclear Pain

```text
if proposed_tier = B
and pain_urgency <= 3
then Discovery Sprint
```

### Rule D: High Attractiveness + High Risk

```text
if attractiveness is high
and risk_friction >= 4
then Risk Review
```

### Rule E: Tier C or Hold

```text
if proposed_tier in [C, Hold]
then Nurture or Deprioritize
```

## Required Output

```markdown
## Recommended ABM Play

- Account:
- Proposed Tier:
- Recommended Play:
- Why this Play:
- First Action:
- Owner Role:
- Due Date:
- Success Signal:
- Review Timing:
```

## Anti-patterns

- Create a proposal before pain is validated
- Assign Tier A without a high-touch action
- Keep a Hold account without a re-entry trigger
- Ignore risk because an account looks attractive
- Treat all Tier A accounts with the same play

## Design Principle

Account priority and account state are different.

```text
Important but weak access → Executive Mapping
Important but unclear pain → Discovery Sprint
Important with validated pain → Tailored Proposal
Important but risky → Risk Review
Not ready → Nurture or Deprioritize
```
