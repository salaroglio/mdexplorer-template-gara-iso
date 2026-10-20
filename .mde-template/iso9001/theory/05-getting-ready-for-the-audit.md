---
title: Getting ready for the audit
---

# Getting ready for the audit

## TL;DR

The internal audit (9.2) is the check the system does on itself before an external body does it. In MdExplorer the
`iso9001-auditor` agent prepares it: it reads the processes, the workflows, the round logs and the git history, and writes
a report a person approves. The nonconformities found become corrective actions (10.2), with their own workflow.

- The evidence is already there: approved documents, recorded outcomes, commits. The audit checks that they say the right thing.
- The typical findings are few and recurring: roles without a person, processes without a workflow, approvals too quick.
- A corrective action is closed only when someone has checked that it worked.

## What the standard asks

The organisation does internal audits at planned intervals, with defined criteria and scope, with auditors who do not
audit their own work, and retains the results. The management review (9.3) then uses those results to decide. The
method does not set how often: it is the group's choice, to write in the audit plan in `quality/audit/`.

## The `iso9001-auditor` agent

It works for whoever has the internal auditor role. It takes from the plan in `quality/audit/README.md` the first audit
«to do» (which processes, which period) and reads:

- `quality/processes.md`: the processes and their workflows;
- the responsibilities document (`responsibilities.md`): who has which role;
- the project's workflows and the logs of their rounds in the period;
- the git history of the delivered documents.

It delivers a report in `quality/audit/`: what it checked, what it found, with the evidence. **It does not decide**: the
person who has the role reads, checks the doubtful points and approves the report. Whoever approves guarantees
independence, not the agent.

## The evidence to show

| The auditor asks | Where it is |
|---|---|
| who did this activity, and with which role | the round log and the responsibilities document at the date of the round |
| the document the decision was taken on | the approved commit given in the decision |
| that the procedure followed was the one in force | the version of the workflow saved by the round when it started |
| what happened when something went wrong | the rejections with their reason, and the redone version |
| who changed a rule, and when | the git history of the document or of the workflow |

## How to read the history

For a round: start from the round log, open the decision, follow the commit it gives up to the document. For a rules
document (a workflow, the company profile): the git history gives every change, with author and date. A change without a
reason written in the message is already a small finding.

## The typical findings

| Finding | What it means | Clause |
|---|---|---|
| a role in the workflows without a person | nobody answers for that step | 5.3 |
| a process in `quality/processes.md` without workflow or evidence | the process is not under control | 4.4 |
| approvals done in a few seconds, always by the same person | the control may be only formal | 8.2.3 |
| a review without the risks section | the risks were not considered where the decision is taken | 6.1 |
| a workflow changed without a written reason | the change was not controlled | 7.5, 8.5.6 |
| a corrective action closed without a check | nobody knows whether it worked | 10.2 |

## From nonconformity to corrective action

For every nonconformity 10.2 asks to react, understand the cause, decide an action, carry it out and check that it was
effective. It pays to make it a workflow, with steps and outcomes:

1. **Register** the nonconformity, with the evidence (an agent prepares, the auditor approves).
2. **Analyse the cause**: why it happened, not only what (the process owner approves).
3. **Decide the action**: a step of a person, with the action and the date by which to check it.
4. **Check effectiveness**: after the date, has the problem come back? Outcomes: «Effective» or «Not effective»; in the
   second case you go back to the analysis.

[03 — From process to workflow](03-from-process-to-workflow.md) explains how to build it; the MarkAgent can propose its
first version.

## Before the external audit

- A complete internal audit in the period, with the approved report and the open actions under way.
- A management review (9.3) that read those results, with its minutes.
- `quality/processes.md` up to date: every process with its owner, its workflow or the reason why it has none.

This guide helps you get ready; the judgement on conformity is given by the certification body.

See also: [02 — The clauses that matter](02-the-clauses-that-matter.md),
[06 — Working with the MarkAgent](06-working-with-the-markagent.md).
