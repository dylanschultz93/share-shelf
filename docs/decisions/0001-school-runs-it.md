# 0001: The school runs it, not the founder

**Status:** Decided (2026-10-02)

## Question
When the founding parent leaves CECC (or before), what happens to Share Shelf?

## Decision
School administration runs the app, the same way they already run the school's website. The founder should spend no ongoing time on it, ideally even before leaving.

The app should be easy enough to manage that another school could pick it up and run it too. That's also the path to white-labeling or offering it to other schools.

## Why
- The founder's time and sanity: this shouldn't become a second job.
- An app that depends on one volunteer dies when that volunteer leaves.
- "Easy for a school office to run" and "easy to hand to another school" are the same requirement.

## What this affects
- **Admin experience is a core feature, not an afterthought.** Approving people, removing posts, managing classrooms and starting a new school year all have to work without a developer.
- **No developer tasks in normal operation.** No touching a database, no terminal, no hand-edited config for routine changes.
- **School-specific details are settings, not code:** the school name, classroom names, logo and colors.
- **Accounts and billing belong to the school,** not a personal account. This shapes hosting choices.
- **The founder needs a clean handoff point,** something to plan for before leaving.
- **Open question:** one shared install that hosts many schools, or a separate copy per school? This comes later, but this decision makes it a real question.
