---
mde_type: workflow
title: A process becomes a workflow
workflow: process.workflow.json
---

# A process becomes a workflow

## TL;DR

A process of the quality system described in `quality/processes.md` and marked «to design» becomes the proposal of a
workflow: the steps, who prepares and who approves, the evidence that stays, the clauses it covers. The quality manager
decides whether it is built, and puts it to work with the MarkAgent.

- The quality manager launches the designer when a process is ready to become a workflow.
- A proposal to redo is redone when the person presses «Restart».
- The method's theory, chapter «From process to workflow», explains how to do it by hand or with the MarkAgent.

## The round

```plantuml(@workflow, ./process.workflow.json)
```

## Who does what

| Step | Who works | What they deliver | Who approves |
|---|---|---|---|
| Propose the workflow | designer agent | `quality/proposals/proposal-<process>.md` | the quality manager |
| Decide on the proposal | the quality manager | the decision, in the round log | — |
