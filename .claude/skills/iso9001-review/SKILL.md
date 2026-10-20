---
name: iso9001-review
description: "How to write the requirements review before committing to a customer (ISO 9001, 8.2.3): explicit, implicit and statutory requirements, capability to meet them, risks, recommendation. Use it when you write or check tenders/sheets/review.md or when you are asked whether an offer was reviewed."
---

# The requirements review (ISO 9001, 8.2.3)

Before committing to supply a product or a service — for a tender, **before submitting the offer** — the company reviews
the requirements and asks itself whether it can meet them. The outcome is **recorded** (8.2.3.2). In this method the record
is made of two things: the document `tenders/sheets/review.md` in git, and the person's decision in MdExplorer's round log,
with who, when and the approved commit.

## What it must contain

`tenders/sheets/review.md` has these sections, in this order:

- `## TL;DR`: three lines and three bullet points, written last.
- `## The call for tenders`: code, title, contracting authority, deadline for the offer and days left from the working date;
  the paths of the tender document, of the search and of the three approved sheets.
- `## Recommendation`: *bid*, *bid with conditions* or *do not bid*, with the reason in two lines. It is a proposal: the
  person decides.
- `## The five criteria`: a table with criteria 1 and 5 as the search judged them and criteria 2, 3 and 4 as the sheets
  closed them (result and the sheet it comes from).
- `## Requirements` (8.2.2), in three tables with section of the tender document and status (covered, partial, not covered,
  to be clarified):
  - **explicit**: what the call asks in writing;
  - **implicit**: what the customer expects even if they do not write it (for example the continuity of an existing service);
  - **statutory**: mandatory laws, standards and certifications, taken from the «Statutory requirements» sections of the sheets.
- `## Capability to meet them` (8.2.3.1): by area (technical, contract, delivery) what is missing and whether it can be
  filled before the deadline or the delivery.
- `## Risks` (6.1): the open risks by area, the most serious of each, and the opportunities if there are any.
- `## Points to clarify with the contracting authority` (8.2.1): a numbered list, with area and section of the tender document.
- `## Where the sheets contradict each other`: when two sheets say different things about the same point, write it here.
- `## For you to check`: three points where the review is least sure.

## Rules

- Every piece of data cites the **sheet** or the **section** of the tender document it comes from: the auditor must be able
  to find it again.
- Do not make things up: what the sheets and the tender document do not say is «to be clarified».
- The review does not decide: the decision is the person's, in the step «Decide whether to bid» of the workflow.
- If after the review the call changes (clarifications, corrections that touch the requirements — 8.2.4), the round is
  redone: the sheets and the review are rewritten, and the git history keeps the earlier versions.
