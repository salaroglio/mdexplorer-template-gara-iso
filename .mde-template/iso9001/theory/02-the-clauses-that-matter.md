---
title: The clauses that matter
---

# The clauses that matter

## TL;DR

This is the map between the ISO 9001:2015 clauses that touch everyday work and the MdExplorer things that cover them:
roles, documents, workflows, git history. The clauses are described in our own words and with their number: for the
exact text, read the standard.

- Roles and responsibilities (5.3) are in the responsibilities document; the evidence (7.5) is in git.
- Requirements (8.2), changes (8.5.6), nonconformities (8.7, 10.2) and audit (9.2) become workflows with outcomes.
- Context, leadership and management review stay the people's work, but they too leave documents in the project.

## How to read the table

For every clause: what it asks, in short; where it is in an MdExplorer project; what to show an auditor. A clause not
listed is not less important: it is only less tied to the way the group passes work on.

## Organisation and responsibilities

| Clause | What it asks | Where it is in MdExplorer |
|---|---|---|
| 4.4 processes of the system | knowing the processes, their inputs and outputs, who answers for them, how they are controlled | `quality/processes.md`, one row per process; one workflow for every process that changes hands |
| 5.3 roles and responsibilities | assigning and communicating who has which responsibility | the project's responsibilities document: role, person, email, agents |
| 7.2 competence | competent people for the role, with evidence | the responsibilities document says who; the evidence of competence is kept separately |

The responsibilities document is a table: the **role** is the name the workflows use, the person is whoever answers for
it today. When someone changes job one row changes, and the git history says since when.

## Risks and documented information

| Clause | What it asks | Where it is in MdExplorer |
|---|---|---|
| 6.1 risks and opportunities | considering the risks that can prevent the results, and acting | a fixed item of the review documents: the «Risks» section, as in the tender review |
| 7.5 documented information | keeping written what is needed, identified, up to date, protected | the project's markdown documents; the git history says who changed what, and when |

6.1 does not ask for a risk register separate from everything else: it asks that risks are considered where decisions
are made. Putting them as a mandatory section of a document a role approves is the simplest way to show it.

7.5 distinguishes between what is **maintained** (the rules: procedures, workflows, company profile) and what is
**retained** (the records: reviews done, outcomes, minutes). In MdExplorer the former are documents that change with
approved versions; the latter are the documents delivered in the rounds, which are not rewritten.

## Operations

| Clause | What it asks | Where it is in MdExplorer |
|---|---|---|
| 8.2.2 and 8.2.3 requirements and their review | understanding what the customer asks and reviewing it before committing, recording the outcome | a workflow like the tender one: sheets, review, decision with an outcome |
| 8.5.6 control of changes | reviewing and controlling changes, recording who authorised them | a «change» workflow: request, impact analysis, approval by a role |
| 8.7 nonconforming outputs | identifying what is wrong and deciding what to do with it | a step of a person with outcomes: correct, redo, accept under concession, scrap |

The tender's requirements review is the complete example: document [04 — The tender example](04-the-tender-example.md)
reads it.

## Evaluation and improvement

| Clause | What it asks | Where it is in MdExplorer |
|---|---|---|
| 9.1 monitoring and measurement | deciding what to measure and analysing it | the round logs: how many, how long, how many rejections |
| 9.2 internal audit | checking at planned intervals that the system works | a round of the `iso9001-auditor` agent, with the report in `quality/audit/` |
| 9.3 management review | management reviews the system and decides | a step of a person of the Management role, with the minutes as a produced document |
| 10.2 nonconformity and corrective action | reacting, finding the cause, correcting, checking that it worked | a workflow with outcomes: cause analysis, action, check of effectiveness |

## What stays outside the workflows

- **Clause 4** (context and interested parties) and **5.2** (quality policy): they are documents management writes and
  approves. In the project they are in `quality/`, like any other document, with their history.
- **7.1** (resources, infrastructure, measuring instruments): it depends on the company's work; the method does not model it.
- **Applicability**: if a clause does not apply, it must be said and justified. It is a decision of the people.

See also: [01 — ISO 9001 as workflows](01-iso-9001-as-workflows.md),
[03 — From process to workflow](03-from-process-to-workflow.md),
[05 — Getting ready for the audit](05-getting-ready-for-the-audit.md).
