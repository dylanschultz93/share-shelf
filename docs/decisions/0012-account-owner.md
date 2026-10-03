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
- **The code is separate. It stays in the founder's GitHub** ([dylanschultz93/share-shelf](https://github.com/dylanschultz93/share-shelf)), under the MIT license in the founder's name. The founder owns the product. The school owns its running copy and its data. That's the normal vendor arrangement.
- **When the founder steps away,** the school's app keeps running as is. If the school ever needs changes, the code is open source, so anyone can copy (fork) it and work from there. Nothing has to be transferred.
- **Detail for the hosting decision:** the school's hosting account has to deploy code from the founder's repo. How that connection works depends on the host.
