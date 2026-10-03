# 0005: Roles are defined by what people can do

**Status:** Decided (2026-10-02)

## Question
Does the app need to know who's a teacher and who's a parent?

## Decision
Yes, but roles are defined by **actions**, not by job title. Each role includes everything the one before it can do:

| Action | Parent | Teacher | Admin |
|---|:-:|:-:|:-:|
| 1. Post an item to donate | ✓ | ✓ | ✓ |
| 2. Claim a classroom need (bring it or buy it) | ✓ | ✓ | ✓ |
| 3. Claim a donated item for a classroom | | ✓ | ✓ |
| 4. Post a classroom need | | ✓ | ✓ |
| 5. Administer the site | | | ✓ |

## Why
- Parents claiming an item "for a classroom" makes no sense, so they can't do #3.
- Teachers should be able to donate things too (#1). For example, a teacher might pass something along to another room.
- Each role building on the one before keeps it simple. Someone who is both a parent and on staff just gets the teacher role and loses nothing.

## What this affects
- **Donated items only go to classrooms.** Families never claim from each other, so every handoff happens at a classroom. This settles the "who can claim giveaways" question.
- Each account has **one role.** The admin sets it when approving someone, and the starting email list ([0002](0002-who-gets-in.md)) can mark who's on staff.
- **Still open:** which classroom(s) a teacher can act for, and what an admin with no classroom posts or claims for.
