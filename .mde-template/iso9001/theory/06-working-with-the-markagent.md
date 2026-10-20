---
title: Working with the MarkAgent
---

# Working with the MarkAgent

## TL;DR

The MarkAgent is the assistant you talk to in MdExplorer: it reads this theory, the project's documents and the
workflows, and helps you understand and build. The method adds two agents: `iso9001-designer`, which proposes a workflow
starting from a process, and `iso9001-auditor`, which prepares the internal audit. All three propose; the people approve.

- You ask the MarkAgent to explain, to compare, to make the first draft: not to decide.
- The designer writes workflow proposals; the workflow itself is written with the `mde-workflow` skill and checked with `check_workflow`; the auditor writes reports.
- Everything that enters the project goes through a person's approval, and is recorded.

## What to ask the MarkAgent

To understand:

- «Explain 8.5.6 to me with an example from our work.»
- «What is the difference between a correction and a corrective action?»
- «Read the tender workflow and tell me which step covers 8.2.3.2.»

To look at the project with an auditor's eyes:

- «Which roles of the workflows have no person in the responsibilities document?»
- «Which processes of `quality/processes.md` have no workflow yet?»
- «Ask me the questions an auditor would ask about our complaints process.»

To build:

- «Help me turn our complaint handling process into a workflow.»
- «Propose the steps for change control, who prepares and who approves.»

If this theory is not in the project yet, the MarkAgent can offer to download it: the copy lands in `theory/iso9001/`
with a commit, from the version of the method the project uses.

## The `iso9001-designer` agent

It works for the quality manager. You launch it with the workflow «A process becomes a workflow»: it reads in
`quality/processes.md` the processes marked «to design», the responsibilities document and this theory, and for each one
it delivers a **proposal** in `quality/proposals/`: the steps, who prepares and who approves, the documents that stay as
evidence, the clauses the process covers, and what is needed to build it (new agents, the workflow).

The decisions that are not its own (who approves, how many times a step is redone) it leaves as open questions. The real
workflow is then written by the person with the MarkAgent (`mde-workflow` and `mde-agent` skills), and checked with the
`check_workflow` tool before adding it to the project.

The person reads the proposal, corrects it if they want, and approves it. Then they add the workflow to the project:
from that moment the workflow works.

## The `iso9001-auditor` agent

It works for whoever has the internal auditor role. It takes the first audit «to do» of the plan in
`quality/audit/README.md`, reads processes, responsibilities, workflows, round logs and git history, and delivers a report
in `quality/audit/` with the evidence of every finding. Document
[05 — Getting ready for the audit](05-getting-ready-for-the-audit.md) says what it looks for. It does not audit the work
of the person it works for: whoever approves the report must be independent of the process audited.

## What they do not do

- They approve nothing: an approval is always a person's, from their computer.
- They do not decide who comes next: the workflow does the hand-overs.
- They do not make up the standard: when a point is doubtful they say so, and refer to the official text.
- They do not change a workflow in use without saying so: a change is valid from the next round, and it is approved like
  the first version.

## A way of working that works

1. A person and the MarkAgent describe the processes together in `quality/processes.md`.
2. You pick the process that scares you most in an audit, not the easiest one.
3. The designer proposes the workflow; the person reads it again with the MarkAgent, question by question.
4. You do a real, small trial round, and adjust.
5. After a few rounds, the auditor does an internal audit on that process.
6. You move on to the next process.

See also: [03 — From process to workflow](03-from-process-to-workflow.md), [README](README.md).
