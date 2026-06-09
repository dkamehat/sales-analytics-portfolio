# Example ABM Decision Memo

This example uses fictional data only.

## Decision Summary

| Item | Value |
|---|---|
| Decision Date | 2026-06-10 |
| Account | Northstar Manufacturing Co. |
| Current Tier | B |
| Proposed Tier | A |
| Decision Type | Tier Change |
| Decision Owner Role | Sales Lead |
| Review Date | 2026-07-10 |

## 1. Recommendation

Move Northstar Manufacturing Co. from Tier B to Tier A, but do not start with a full proposal.

Recommended Play: Executive Mapping.

## 2. Main Reason

The account has high strategic fit, high revenue potential, strong expansion potential, and validated operational pain. It is worth concentrated ABM effort.

## 3. Counterargument

Executive access is still weak. Without an economic buyer or executive sponsor, a high-effort proposal may become premature and waste resources.

## 4. Evidence

| Evidence Type | Summary | Strength |
|---|---|---|
| Strategic Fit | Matches priority segment and use case pattern | Strong |
| Revenue Potential | Strategic revenue band and multi-unit expansion potential | Strong |
| Pain Urgency | Champion confirmed operational pain | Medium |
| Stakeholder Access | Champion exists, but economic buyer access is weak | Weak |
| Expansion Potential | Multiple teams or regions may be relevant | Strong |
| Execution Feasibility | Feasible if scope is controlled | Medium |
| Risk / Friction | No critical blocker identified yet | Low |

## 5. Recommended ABM Play

| Item | Value |
|---|---|
| Play | Executive Mapping |
| First Action | Map economic buyer, blockers, and potential executive sponsor path |
| Owner Role | Account Owner |
| Due Date | 2026-06-24 |
| Success Signal | At least one executive sponsor or economic buyer path is identified |

## 6. Missing Information

- Who owns the budget?
- What is the executive-level priority?
- Is there an active transformation initiative?
- Which stakeholder can introduce the economic buyer?

## 7. Review Plan

At the review date, check:

- Was an executive sponsor path identified?
- Did the champion agree to introduce another stakeholder?
- Did pain become more urgent or remain vague?
- Should the account remain Tier A, move to Tier B, or shift to Discovery Sprint?

## 8. Audit Entry

```csv
date,account_id,account_name,decision_type,from_tier,to_tier,priority_score,reason,counterargument,recommended_play,owner_role,review_date,success_signal
2026-06-10,ACC-001,Northstar Manufacturing Co.,tier_change,B,A,4.2,High fit and validated pain,Executive access is weak,executive_mapping,account_owner,2026-07-10,Executive sponsor role identified
```
