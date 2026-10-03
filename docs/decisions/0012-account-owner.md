# 0012: communications@claytonecc.org owns every account

**Status:** Decided (2026-10-02)

## Question
Which email address owns the app's service accounts (hosting, database, email sending, domain)?

## Decision
**`communications@claytonecc.org`**, a shared school address in the school's Google Workspace, is the owner of every service account from day one.

## Why
- It belongs to the school, not a person, so the school already owns everything ([0001](0001-school-runs-it.md)).
- The founder already has access, so setup isn't blocked on anyone.
- **Handoff is just stepping away.** Nothing has to be transferred. The school keeps access through the shared inbox.

## What this affects
- Every new service gets signed up under this address. Billing (during the trial and after) attaches to these accounts ([0003](0003-cost.md)).
- Prefer services that allow **one owner account plus extra team members,** so the founder or a future helper can be added and removed without sharing the inbox's password.
- **Still open:** the code lives in the founder's personal GitHub account ([dylanschultz93/share-shelf](https://github.com/dylanschultz93/share-shelf)). Before the handoff, it may need to move to a GitHub organization owned by the school.
