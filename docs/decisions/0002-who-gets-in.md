# 0002: Who gets in: a starting list, then one admin approves

**Status:** Decided (2026-10-02)

## Question
How do we keep Share Shelf limited to the school community, and who lets new people in?

## Decision
- **At launch:** load the app with a list of email addresses we already have for current families and staff. Those people can sign in right away, with no approval wait.
- **After launch:** anyone not on the list can request access. **One person approves them,** ideally an admin at the school.
- **No integration with Procare** or any other school system.

## Why
- **Starting from a list** makes launch easy. Most people get in on day one, and later the approval queue is only new families, which is a small, steady trickle.
- **One approver** keeps it simple and matches [decision 0001](0001-school-runs-it.md) (the school runs it).
- **We passed on matching against Procare automatically.** It would be elegant, but it's technically hard, ties us to one vendor and doesn't fit other schools. See [principle 3](../principles.md).
- **We passed on "anyone with the link."** It's simpler, but it felt too open for a school community.

## What this affects
- The admin needs **a way to add a list of emails** (pasting a list is enough) and **a simple approval queue.**
- Sign-in is by email, so **the email address is how we identify a person.** A parent who uses a different email than the one on the list goes to the approval queue, which is fine.
- **Still open:** removing people who leave the school, and whether someone can be on the list as staff vs. family.
