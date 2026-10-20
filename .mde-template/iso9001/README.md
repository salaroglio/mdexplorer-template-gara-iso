---
title: ISO 9001
---

# ISO 9001

## TL;DR

A way of working for MdExplorer: the quality management system as a set of well-made workflows. The processes are
described in `quality/processes.md`, one agent proposes how to turn them into workflows, another prepares the internal
audit with the evidence the rounds leave in git; the people approve and decide.

- It is chosen in «Create new project», on top of the common layer, or added to an existing project.
- With the example, the project also starts with the tender workflow (requirements review, 8.2.3) and a filled-in tender.
- The theory, if you ask for it, lands in `theory/iso9001/`: an ISO 9001 system seen as workflows, clause by clause.

## What it brings

| What | Where |
|---|---|
| The two workflows: a process becomes a workflow, the internal audit | `workflows/` |
| The cards of the two agents: designer, internal auditor's assistant | `agents/` |
| The roles: Quality manager, Internal auditor, Management | the project's responsibilities document, as open roles |
| The instructions for the project's agents | a block in `CLAUDE.md`, `AGENTS.md`, `copilot-instructions.md` |
| The group's starting files | `quality/`, copied once from `seeds/` |
| The processes skill | `.claude/skills/iso9001-processes/` |
| The theory | `theory/`, copied into `theory/iso9001/` if you ask for it |

## How to start

1. Whoever answers for the roles takes them in the responsibilities document (or says «It's mine» in the agent city).
2. With the MarkAgent, describe the processes in `quality/processes.md`; mark «to design» the ones to turn into workflows.
3. The quality manager launches the designer, reads the proposals, puts the approved workflows to work.
4. Write the audit plan in `quality/audit/README.md`; the internal auditor launches the audit when its date comes.

## From «Tender with ISO 9001»

Up to 1.2.0 this method was «Tender with ISO 9001» (id `gara-iso`, Italian only) and brought only the tender. From 2.0.0
the tender is the method's example, in the `example` branch. A project created with `gara-iso` stays as it is: it does
not update to `iso9001`, which is another template.
