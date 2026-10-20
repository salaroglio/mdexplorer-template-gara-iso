---
mde_type: workflow
title: The internal audit
workflow: audit.workflow.json
---

# The internal audit

## TL;DR

The internal audit (ISO 9001, 9.2) of the plan in `quality/audit/README.md`: the agent prepares the report with one piece
of evidence for every finding, the internal auditor checks and approves it, management decides the actions (10.2).

- The internal auditor launches the agent when the audit «to do» of the plan comes.
- Whoever approves the report must not answer for the processes audited: the person guarantees independence, not the agent.
- Report and actions stay in `quality/audit/`, the decisions in the round log.

## The round

```plantuml(@workflow, ./audit.workflow.json)
```

## Who does what

| Step | Who works | What they deliver | Who approves |
|---|---|---|---|
| Prepare the report | internal auditor's assistant agent | `quality/audit/audit-<date>.md` | the internal auditor |
| Decide the actions | management | `quality/audit/actions-<date>.md` and the decision | — |
