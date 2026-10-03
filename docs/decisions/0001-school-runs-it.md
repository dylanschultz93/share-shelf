# 0001: The school runs it, not the founder

**Status:** Decided (2026-10-02)

## Question
When the founding parent leaves CECC (or before), what happens to Share Shelf?

## Decision
School administration runs the app *from inside the app* (approving people, removing posts, managing classrooms), the same way they already update the school's website. The founder should spend no ongoing time on those day-to-day tasks, ideally even before leaving.

This is about in-app admin, not infrastructure. The founder operates the hosting and services ([0012](0012-account-owner.md)).

The app should be easy enough for the school office to manage without help.

## Why
- The founder's time and sanity: this shouldn't become a second job.
- An app that depends on one volunteer dies when that volunteer leaves.

## What this affects
- **Admin experience is a core feature, not an afterthought.** Approving people, removing posts, managing classrooms and starting a new school year all have to work without a developer.
- **No developer tasks in normal operation.** No touching a database, no terminal, no hand-edited config for routine changes.
- **Things that change from year to year are editable by the admin,** for example classroom names and teachers. Things that never change (the school name, the look) can just be built in.
- **The founder needs a clean handoff point** for the in-app admin role, something to plan for before leaving.

*Revised 2026-10-02: dropped multi-school and white-label goals. See [principle 4](../principles.md).*
