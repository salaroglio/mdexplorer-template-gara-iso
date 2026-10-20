---
title: The tender example
---

# The tender example

## TL;DR

The tender workflow takes a call for tenders up to the decision to bid, through the requirements review ISO 9001 asks
for before committing to a customer (8.2.3). Here we read it as a model: for each step, what it proves to an auditor.
The workflow lives in the method's example branch: it is there in projects created «with the example».

- Every lead prepares and approves their own sheet; the review starts by itself when the three sheets are approved.
- The decision is a step of a person with two buttons: who took it, when and on which review stays recorded.
- It is a model to copy in its form, not in its content: the same pattern works for an offer, a contract, an order.

## Where to find it

In a project created with the example the workflow and its documents are in the method's folder and in `tenders/`, with
a tender already filled in (an invented call for tenders). In a project created with the structure only it is not there:
you can create a trial project with the example and look at it there.

## The round, step by step

| Step | Who works | What it delivers | What it proves |
|---|---|---|---|
| Search the calls | account manager's agent | a search, with one question per criterion | that the calls were assessed with written criteria, not by feeling |
| Technical sheet | technical lead's agent | the technical sheet | that technical capability was checked by whoever answers for it (8.2.3) |
| Contract sheet | legal lead's agent | the contract sheet | that the contractual and statutory requirements were read (8.2.2) |
| Delivery sheet | delivery lead's agent | the delivery sheet | that times and resources are sustainable |
| Requirements review | account manager's agent | the review: requirements, capability, risks, recommendation | the review before committing (8.2.3.1) and the risks considered (6.1) |
| Decide whether to bid | the account manager | the outcome «We bid» or «We do not bid» | the record of the review and of the decision (8.2.3.2) |

## Why it is built this way

**Three sheets, three leads.** Every sheet is approved by the person who answers for that point of view. Nobody signs
for someone else: it is 5.3 applied to a single call for tenders.

**The sheets start on request.** Every lead starts their own when the request arrives, from their computer. Whoever
launched the round does not decide for them when to work.

**The review waits for all three.** It starts by itself only when the three sheets are approved. A review done with a
missing sheet cannot exist: the workflow does not start it.

**Risks are a mandatory section of the review.** 6.1 is covered without a separate register: whoever approves the review
sees the risks written next to the recommendation.

**The decision is a button, not an email.** Whoever decides presses «We bid» or «We do not bid»: MdExplorer records who,
when and on which version of the review. There is no free text to interpret later.

**A rejected sheet is redone.** The loop «until approved» leaves in the history both the rejected version, with the
reason, and the approved one. An auditor sees that the control worked.

## What an auditor looks at on a round

1. The round log: the call for tenders, the dates of every step, who approved.
2. The approved review and the commit given in the decision: the document the person read is exactly that one.
3. The sheets: signed by different roles, each with its commit.
4. The rejections, if there were any: the reason and the redone version.
5. The consistency between the review's recommendation and the decision taken, or the written reason if they differ.

## How to reuse it

The same pattern (sheets by several leads, a review that puts them together, a decision with outcomes) works for many
processes: the review of an order, the acceptance of a contract change, the choice of a supplier (8.4). To build one
follow [03 — From process to workflow](03-from-process-to-workflow.md), and ask the MarkAgent to start from the form of
this one.

See also: [02 — The clauses that matter](02-the-clauses-that-matter.md),
[05 — Getting ready for the audit](05-getting-ready-for-the-audit.md).
