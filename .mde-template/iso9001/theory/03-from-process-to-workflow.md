---
title: From process to workflow
---

# From process to workflow

## TL;DR

A workflow is built starting from the process as it is today, not from an ideal model: you describe it in a row of
`quality/processes.md`, split it into steps, decide who prepares and who approves each step, and only at the end you
write it. The example that follows is complaint handling.

- First the process row (purpose, input, output, owner, evidence), then the steps, then the file.
- An agent prepares, a role approves: every step delivers a file, and every decision is an outcome with buttons.
- The workflow is written with the `mde-workflow` skill and checked with the `check_workflow` tool before using it.

## 1. Describe the process in one row

In `quality/processes.md` every process of the group has a row:

| Field | What to write | Complaints, for example |
|---|---|---|
| Purpose | why the process exists, in one sentence | answering the customer and removing the cause of the problem |
| Input / output | what starts it, what it delivers | a complaint; the answer to the customer and, if needed, a corrective action |
| Owner | the role that answers for it | Quality manager |
| Evidence | what must stay written | the registered complaint, the analysis, the answer, the decision |

If a row cannot be filled in, the problem is not the workflow: it is that the process is not clear yet. It pays to stop
there and talk about it in the group.

## 2. Split it into steps

Write the process as a sequence of activities, each with **one** owner and **one** result. For complaints:

1. **Register the complaint**: whoever receives it describes it, with customer, date, product or service.
2. **Analyse**: what happened, which requirement was not met, whether it is an isolated case.
3. **Decide**: is a correction enough, or is a corrective action on the cause needed (10.2)?
4. **Answer the customer**: the answer, approved by whoever answers for it.
5. **Check effectiveness**, if there was a corrective action: after an agreed time, has the problem come back?

A useful rule: if a step has two approvers, it is two steps.

## 3. Decide who prepares and who approves

For every step, two questions:

- **Does an agent prepare it or does a person do it?** A document to write (the analysis, the draft answer) is prepared by
  an agent; a choice (correct, or act on the cause) is a step of a person, with the outcomes as buttons.
- **Who approves?** Usually whoever answers for the agent; when the standard wants another signature, the workflow says
  so with the approval of a role («the answer to the customer is approved by the Quality manager»).

| Step | Who works | What it delivers | Who approves or decides |
|---|---|---|---|
| Register | customer service agent | `quality/complaints/<code>.md` | Customer service |
| Analyse | customer service agent | `quality/complaints/<code>-analysis.md` | Quality manager |
| Decide | Quality manager | outcome: «Correction» or «Corrective action» | it is the decision |
| Answer | customer service agent | `quality/complaints/<code>-answer.md` | Quality manager |

The roles must exist in the responsibilities document, with a person behind them.

## 4. Define the outputs as files

Every delivery is a file with a fixed path, in a folder that exists and has its `README.md`. A path with `*`
(`complaints/complaint-*.md`) is fine when every round produces a new file. The files are the evidence: they must say what
was done, not summarise it.

## 5. Decide what happens when something is rejected

A rejected analysis is redone: it is a loop «until approved». Decide whether it repeats without limit (usually the right
choice) or at most a certain number of times, and who restarts it. The limit is a decision of the people, not of the
MarkAgent.

## 6. Write the workflow, and check it

Only now you write it. The `iso9001-designer` agent can prepare its proposal (steps, roles, evidence); the real workflow
you write with the MarkAgent and the `mde-workflow` skill: the document with `mde_type: workflow` and its
`.workflow.json` file, plus the cards of the agents it needs. Then:

1. MdExplorer's `check_workflow` tool must answer that it is valid; every warning must be read;
2. the document is added to the project's workflows (Project settings, «Workflow documents»);
3. whoever answers for the process reads it, with the drawing MdExplorer makes of it, and approves it;
4. a trial round is done on a small real case, and it is adjusted.

A round keeps the version of the workflow it started with: a change is valid from the next round.

## 7. Update the process row

Go back to `quality/processes.md` and write, next to the process, the path of its workflow. This way the list says which
processes are already workflows and which are not: it is the first thing an internal auditor will look at.

See also: [04 — The tender example](04-the-tender-example.md),
[06 — Working with the MarkAgent](06-working-with-the-markagent.md).
