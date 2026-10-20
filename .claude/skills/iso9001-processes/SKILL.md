---
name: iso9001-processes
description: "The processes of the ISO 9001 quality system in MdExplorer: what quality/processes.md looks like, what the workflow proposal of a process looks like (quality/proposals/) and the audit plan (quality/audit/README.md). Use it when you describe a process, propose or review its workflow, or prepare an internal audit."
---

# The processes of the quality system

The method's idea: an ISO 9001 system is largely a set of **well-made processes**, and a process that changes hands is
an MdExplorer **workflow**. Who prepares (an agent) and who approves (a person of a role) are written down; every round
stays in the round log and in git, and it is the evidence the audit asks for (7.5).

## `quality/processes.md`

A table, one row per process:

| Column | What it holds |
|---|---|
| Process | the name, short: «Complaint handling» |
| Purpose and boundaries | what it is for, where it starts and where it ends |
| Input / output | what comes in, what comes out |
| Owner | the role that answers for it, as in `responsibilities.md` |
| Evidence | the documents the process leaves |
| Workflow | the path of its workflow document; «to design»; or «none», with the reason |

## The proposal `quality/proposals/proposal-<process>.md`

- `## TL;DR`: three lines and three points, written last.
- `## The process`: the row of `processes.md`, repeated.
- `## The steps`: a table with **step**, **who prepares** (agent, new or existing), **what it delivers** (the path of the
  file), **who approves** (the role), **if rejected** (redone, how many times).
- `## The evidence`: what stays and where, for every step: the document, the decision in the round log.
- `## The clauses`: the ISO 9001 clauses the process covers, with the number and one line of why.
- `## Open questions`: what the person must decide.
- `## To build it`: the new agents to write (`mde-agent` skill) and the workflow (`mde-workflow` skill, then the
  `check_workflow` tool).

## The audit plan `quality/audit/README.md`

A table: **audit** (the planned date), **scope** (the processes), **period** (from when to when), **status** («to do»,
«done: audit-<date>.md»). The internal auditor's assistant prepares the first one «to do». Whoever approves the report
does not answer for the processes audited.
