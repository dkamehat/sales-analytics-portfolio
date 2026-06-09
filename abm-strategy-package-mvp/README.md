# ABM Strategy Package MVP

A lightweight portfolio project for converting account prioritization discussions into a reusable ABM strategy decision package.

This project is designed for Sales Ops, BizOps, RevOps, and strategy operators who often see the same pattern:

- account prioritization depends on recurring meetings
- criteria shift from meeting to meeting
- analysis outputs do not become reusable decision logic
- decisions are made, but actions and review dates are unclear
- junior or mid-level operators can see the structure, but do not have formal authority to redesign the process

The goal is not to replace human judgment. The goal is to make judgment reusable, reviewable, and easier to improve.

## Concept

```text
Business Objects
  ↓
Decision Functions
  ↓
Recommended Actions
  ↓
Review / Audit
```

This is a small example of turning strategy work into an operating package.

| Before | After |
|---|---|
| Account priority is discussed from scratch | Priority logic is reused and reviewed |
| Spreadsheet analysis stays as meeting material | Analysis becomes input to a decision function |
| Criteria are implicit | Criteria, exceptions, and counterarguments are written down |
| Tiering ends the discussion | Tiering creates a next action and review date |
| Decisions disappear after the meeting | Decisions are auditable and improvable |

## What this project contains

```text
abm-strategy-package-mvp/
├ README.md
├ docs/
│ ├ problem_statement.md
│ └ public_safety_notes.md
├ ontology/
│ └ abm_objects.yml
├ decision_functions/
│ ├ decide_account_priority.md
│ └ select_abm_play.md
├ actions/
│ └ action_catalog.yml
├ prompts/
│ └ analyze_abm_strategy.md
├ templates/
│ ├ account_strategy_canvas.md
│ ├ decision_memo.md
│ └ audit_log.csv
└ samples/
  ├ accounts_dummy.csv
  ├ stakeholders_dummy.csv
  ├ engagements_dummy.csv
  └ example_decision_memo.md
```

## Minimal usage

1. Review `samples/accounts_dummy.csv`.
2. Check object definitions in `ontology/abm_objects.yml`.
3. Apply `decision_functions/decide_account_priority.md`.
4. Select a play from `decision_functions/select_abm_play.md`.
5. Record the result in `templates/decision_memo.md`.
6. Append the decision to `templates/audit_log.csv`.

## Intended audience

- Sales Ops / BizOps / RevOps operators
- Sales strategy analysts
- Junior or mid-level operators in coordination-heavy organizations
- People who want to move from “reporting numbers” to “designing decision workflows”

## Public-data policy

This repository uses only fictional sample data and generic business objects.

Do not add:

- real customer names
- real revenue, margin, or KPI values
- proprietary SQL
- CRM/SFA exports
- private meeting notes
- internal organization names
- personal data
- company-identifiable anecdotes

## One-line summary

ABM strategy should not live only in meetings. It can be packaged as objects, decision functions, actions, and review logs.
