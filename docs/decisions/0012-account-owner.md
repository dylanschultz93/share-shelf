# 0012: The founder runs the infrastructure. The school is a customer

**Status:** Decided (2026-10-02). Replaces an earlier version that had the school owning the service accounts.

## Question
Who owns the code, the hosting and the service accounts (database, email sending, domain)?

## Decision
Share Shelf works like any other app:

- **The founder owns the code and runs the infrastructure.** The repo ([dylanschultz93/share-shelf](https://github.com/dylanschultz93/share-shelf), MIT license), hosting, database and email-sending accounts are all the founder's.
- **The school is a customer.** It uses the app. Its admin runs things *inside* the app: approving people, removing posts, editing classrooms ([0001](0001-school-runs-it.md)).
- **The school never touches hosting, servers or service accounts.**

## Why
- That's how apps work. Customers don't own their vendor's code or infrastructure.
- Infrastructure at this size mostly runs itself. The founder's time-consuming jobs (approving people, managing content) go to the school's admin inside the app.

## What this affects
- Costs land on the founder's accounts. After the trial, the school reimburses at cost ([0003](0003-cost.md)).
- `communications@claytonecc.org` (a shared school inbox the founder can access) is a good candidate for the **first admin account inside the app.**
- **Still open:** what happens to the running app if the founder ever stops operating it entirely.
