# 0006: Teachers can act for any room, with their usual room as the default

**Status:** Decided (2026-10-02)

## Question
Which classrooms can a teacher post needs for or claim items for?

## Decision
- **Any room.** Every time a teacher posts or claims, the classroom is one field they can change.
- **The app remembers each teacher's usual room** and fills it in automatically. Teachers pick it themselves when they sign up (the same way parents pick their child's rooms) and can change it in their own settings.
- **The admin doesn't assign or maintain teacher rooms.**

## Why
- Most of the time the teacher doesn't have to pick a room, because it's already filled in.
- Floaters, part-time staff and teachers who change rooms can still act for any room in one tap.
- There's no list for the office to keep up to date ([principle 1](../principles.md)).
- Nothing technically prevents posting for another room. We trust teachers ([principle 2](../principles.md)).

## What this affects
- Parents and teachers both pick "my rooms" during first-time setup (screen 1b). It's one mechanism for both.
- Admins can also act for any room. **Still open:** do admins need a "whole school" option (for example, for the kitchen or playground)? Per [principle 3](../principles.md), probably not until someone asks.
