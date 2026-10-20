---
mde_type: workflow
title: The tender, from the call to the decision
workflow: tender.workflow.json
---

# The tender, from the call to the decision

## TL;DR

This document says how the people of the tender and their agents pass the work to each other, from when a call for
tenders appears to when the account manager decides whether to bid. It is the requirements review ISO 9001 asks for
**before committing** to a customer (8.2.3): the decision, with who took it and when, stays recorded.

- The account manager launches the search on the calls and presses «Start the round» on the call that deserves it; each
  lead starts their own sheet (technical, contract, delivery) and approves it.
- The requirements review starts by itself when the three sheets are approved; then the account manager decides with a button.
- A rejected sheet is redone when the person presses «Restart», with no limit on the number of times.

## The round

```plantuml(@workflow, ./tender.workflow.json)
```

## What the standard asks, and where it is

| ISO 9001 | Where it is in the round |
|---|---|
| 8.2.1 customer communication | the «Questions for the client» of every sheet |
| 8.2.2 requirements, statutory ones included | the sheets and the «Requirements» section of the review |
| 8.2.3.1 review before committing | the «Requirements review» step and the person's decision |
| 8.2.3.2 record of the review | the review document in git and the decision in the round log, with who, when and the approved commit |
| 6.1 risks and opportunities | the «Risks» section of the review |

## Who does what

| Step | Who works | Who starts it | Who approves |
|---|---|---|---|
| Search the calls | account manager's agent | the account manager, when they want | the account manager, with «Start the round» on a call |
| Technical, contract, delivery sheet | each lead's agent | the lead, when the request arrives | the same lead |
| Requirements review | account manager's agent | it starts by itself | the account manager |
| Decide whether to bid | the account manager | it arrives in the mailbox | it is the decision |

The real people are in the project's responsibilities document: whoever answers for a role declares it there.
