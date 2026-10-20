---
title: ISO 9001 as workflows
---

# ISO 9001 as workflows

## TL;DR

ISO 9001 asks to manage work by processes: each one with its inputs and outputs, who answers for it, and the evidence
that it was done as planned. An MdExplorer workflow already holds these three things, and the git history keeps the
evidence with no extra work. What no workflow can say by itself stays out: whether the processes are the right ones.

- Process = workflow: the steps are the activities, the roles are the responsibilities, the outcomes are the decisions.
- The evidence the auditor asks for is the round log and the approved commits, not a form filled in on the side.
- Management, context and improvement stay the people's work: the workflow makes them visible, it does not do them.

## The idea

A quality management system, in the end, answers three questions for every activity that matters:

1. **What comes in and what goes out?** The call for tenders comes in, the decision to bid goes out. The complaint comes
   in, the answer to the customer and the corrective action, if any, go out.
2. **Who answers for it?** Not «the office», but a precise role, with a person behind it.
3. **How do you show it went that way?** With something written, dated, attributable to someone.

An MdExplorer workflow answers the same three questions, but in a format that runs:

| Question of the standard | In the workflow |
|---|---|
| What comes in and what goes out | the `inputs` and `outputs` of every step: project files, with their path |
| Who answers for it | the role of every step of a person (`person`) and of every approval (`approval.by`), bound to real people in the responsibilities document |
| How you show it | every approved delivery is a commit; every decision is an outcome recorded with who, when and on which commit |

This is why the method says: **managing a project with ISO 9001 is, in the end, a well-made workflow**.

## What a workflow looks like

A workflow is a markdown document (with `mde_type: workflow`) that explains it to people, plus a JSON file MdExplorer
runs. The JSON lists the steps:

- **a step of an agent**: an agent prepares a document; the person who answers for that agent, or another role,
  approves it;
- **a step of a person**: a role reads what it receives and closes the step with an outcome, that is a button («We bid»
  / «We do not bid», «Solved» / «A corrective action is needed»);
- **repeated rounds**: a rejected document is redone, until it is approved.

Agents **prepare**, people **approve and decide**. MdExplorer passes the work from one step to the next with fixed rules,
and does not let an agent decide by itself who comes next.

## Why the auditor finds what they look for

An auditor does not want to see well-written procedures: they want to see that the work **went** as the procedures say.
With an MdExplorer workflow the evidence is born while you work:

- the delivered document, in the approved version, with its commit;
- who approved it, from which computer, when;
- the outcome of the decision, with the person who pressed the button;
- the rejections and the reworks, with the reason written by whoever rejected;
- the version of the workflow the round started with: a round keeps the workflow it had at the start, even if it changes later.

This is the **retained documented information** clause 7.5 talks about: identified, dated, attributed, protected from
unauthorised changes because every change stays in the git history.

## What a workflow does not cover

A well-made workflow covers a lot, not everything. These stay with the people:

- **the context and the interested parties** (clause 4): which processes are really needed, for whom, with which boundaries;
- **leadership** (clause 5): the quality policy, the objectives, the commitment of management;
- **resources and competence** (7.1, 7.2): that people can do what the role asks;
- **judgement**: a review approved in a hurry is still a review done badly, even if it is recorded.

The workflow makes these points **visible**: a role without a person, a step approved in one minute, a process without a
workflow. It does not solve them.

## The starting point

The first step is not writing a workflow: it is describing the processes the group already has, one per row, in
`quality/processes.md`. Document [03 — From process to workflow](03-from-process-to-workflow.md) explains how, and
[04 — The tender example](04-the-tender-example.md) shows a process that has already become a workflow.

See also: [02 — The clauses that matter](02-the-clauses-that-matter.md).
