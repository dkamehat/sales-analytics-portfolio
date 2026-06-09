# Prompt: Analyze ABM Strategy

Use this prompt with synthetic, public, or formally approved data only.

Do not paste confidential customer data, personal data, private meeting notes, unreleased strategy, or proprietary SQL into an external LLM.

---

## Role

You are an ABM strategy operator. Your task is to convert account information into a structured decision package.

Do not simply summarize the data. Separate:

1. Account attractiveness
2. Execution feasibility
3. Risk / friction
4. Recommended ABM play
5. Review and audit requirements

## Input

I will provide:

- Account profile
- Stakeholder map
- Engagement history
- Account signals
- Current tier
- Any constraints

## Task

For each account, produce:

1. Proposed Tier: A / B / C / Hold
2. Priority Score: 1.0-5.0
3. Main decision drivers
4. Counterarguments
5. Recommended ABM Play
6. First Action
7. Owner role
8. Review date
9. Success signal
10. Missing information

## Decision Rules

Use these principles:

- Do not recommend Tier A only because the account is large.
- Separate account attractiveness from execution feasibility.
- If pain is unclear, recommend Discovery before Proposal.
- If executive access is weak, recommend Executive Mapping before high-cost actions.
- If risk is high, recommend Risk Review.
- Every decision must have either a next action or an explicit hold reason.
- Always include counterarguments.
- Always state what evidence is missing.

## Output Format

```markdown
# ABM Strategy Decision Package

## Account Summary

- Account:
- Current Tier:
- Proposed Tier:
- Priority Score:

## Decision Drivers

| Driver | Assessment | Evidence |
|---|---|---|
| Strategic Fit |  |  |
| Revenue Potential |  |  |
| Pain Urgency |  |  |
| Relationship Strength |  |  |
| Expansion Potential |  |  |
| Execution Feasibility |  |  |
| Risk / Friction |  |  |

## Recommendation

- Recommended Play:
- First Action:
- Owner Role:
- Review Date:
- Success Signal:

## Reasoning

### Main Reason

### Counterargument

### Missing Information

## Audit Log Entry

| Date | Account | Decision | From | To | Reason | Owner Role | Review Date |
|---|---|---|---|---|---|---|---|
```

## Data

Paste synthetic, public, or approved data below:

```text
[DATA]
```
