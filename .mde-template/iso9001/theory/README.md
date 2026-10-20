---
title: The theory of the ISO 9001 method
---

# The theory of the ISO 9001 method

## TL;DR

This folder explains how an ISO 9001 quality management system becomes, in MdExplorer, a set of well-made workflows:
who prepares, who approves, what stays written. You read it alone or with the MarkAgent, and with the MarkAgent you
build the group's real workflows.

- Six short documents, to read in order the first time; then you go back to the one you need.
- The starting point is a single idea: a well-described ISO 9001 process is already almost a workflow.
- It is a working guide: it does not replace the standard, nor the judgement of a certification body.

## What you find here

| Document | What it is about | When to read it |
|---|---|---|
| [01 — ISO 9001 as workflows](01-iso-9001-as-workflows.md) | the idea: processes, responsibilities and evidence become steps, roles and commits | first |
| [02 — The clauses that matter](02-the-clauses-that-matter.md) | the clauses of the standard next to the MdExplorer things that cover them | when you wonder «where is this, for the auditor?» |
| [03 — From process to workflow](03-from-process-to-workflow.md) | the procedure step by step, with the complaints example | when you build a new workflow |
| [04 — The tender example](04-the-tender-example.md) | the tender workflow read as a model: what each step proves | to see a finished workflow |
| [05 — Getting ready for the audit](05-getting-ready-for-the-audit.md) | the internal audit, the evidence to show, the corrective actions | before an audit, internal or external |
| [06 — Working with the MarkAgent](06-working-with-the-markagent.md) | what to ask, and the method's two agents | always, while you work |

## The reading order

1. Read document 01: it says why this method works, and where it stops.
2. Skim 02 without stopping on every row: you need to know the table exists.
3. Before building your first workflow read 03 and 04 together: 03 says how it is done, 04 shows the result.
4. 05 is for when the audit gets close, but it pays to read it early: it says what the auditor will look at, so what the
   workflows must leave written.
5. 06 is the user manual of the method's two agents and of the MarkAgent.

## How to use it with the MarkAgent

The MarkAgent reads these documents as you do. You can ask it to explain a point, to apply it to your case, or to take
the first step with you. Some example requests:

- «Explain in simple words what 8.2.3 asks and where it is in our project.»
- «Help me turn our complaint handling process into a workflow.»
- «Read `quality/processes.md` and tell me which processes have no owner or no evidence yet.»
- «Ask me the questions an auditor would ask about the tender workflow.»

The MarkAgent proposes; **the people decide**. A workflow enters the project only when whoever answers for the process
has read and approved it, and when MdExplorer's `check_workflow` tool says it is valid.

## The words

| Word | What it is | In MdExplorer |
|---|---|---|
| Process | a set of activities that turns inputs into outputs | a workflow |
| Process owner | whoever answers for how the process works | a role in the responsibilities document |
| Documented information | what must be kept written (7.5) | the project's documents and their history in git |
| Evidence | the proof that something was done | an approved document, a recorded outcome, a commit |
| Internal audit | the check the system does on itself (9.2) | a round with the `iso9001-auditor` agent |

## What you do not find here

- The text of the standard: read it in the official edition the company owns.
- A list of mandatory documents to fill in: the standard asks for results and evidence, not forms.
- The certification: an accredited body issues it, after its own audit.
