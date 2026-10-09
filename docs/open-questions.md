# Open questions

We work through these in order, one at a time:

1. **Part 1: The facts.** Questions about people and the school, with no technical answers yet.
2. **Part 2: Technical decisions.** Each one follows from Part 1.
3. **Part 3: Features and details.**

When a question is settled, write it up in [`decisions/`](decisions/) and check it off here with a link.

The screen references (1a–1j) point to [`design/Share Shelf.dc.html`](../design/Share%20Shelf.dc.html).

---

# Part 1: The facts

## A. The long term
- [x] What happens when the founder leaves? → [0001: The school runs it](decisions/0001-school-runs-it.md)
- [ ] How does the school run its website today? Partly answered from the outside → [research/school-tech-today.md](research/school-tech-today.md). Still unknown: *who* edits it.
- [x] One school or many? → CECC only ([principle 4](principles.md))

## B. Running it day to day
- [x] Who approves new people? → [0002: A starting list, then one admin approves](decisions/0002-who-gets-in.md)
- [x] Who removes posts and fixes problems? → the admin ([0005](decisions/0005-roles-by-action.md))
- [x] ~~Use the school's family roster?~~ No. Procare matching was ruled out in [0002](decisions/0002-who-gets-in.md).
- [x] Money → [0003: Aim for free; school pays at cost later](decisions/0003-cost.md)

## C. The community
- [x] Roughly how many families and staff? → [research/cecc-size.md](research/cecc-size.md)
- [x] One adult per family, or two? → [0004: One email = one account](decisions/0004-one-email-one-account.md)
- [x] Roles → [0005: Roles are defined by what people can do](decisions/0005-roles-by-action.md)
- [x] Which classroom(s) can a teacher act for? → [0006: Any room, usual room as default](decisions/0006-teachers-any-room.md)
- [ ] Does an admin need a "whole school" option? (Probably not until asked.)

## D. Trust and privacy
- [x] What do people see about each other? → [0007: Full names](decisions/0007-full-names.md)
- [x] What can unapproved people see? → [0008: Browse with names hidden](decisions/0008-browse-before-approval.md)
- [x] How sure do we need to be that someone belongs? → Covered by [0002](decisions/0002-who-gets-in.md) and [0008](decisions/0008-browse-before-approval.md)

## E. Everyday use
- [x] What devices? → [0009: A mobile-first web app that can be installed](decisions/0009-mobile-first-web-app.md)
- [x] Shared classroom iPads → fine if posts show whoever is signed in ([0009 addendum](decisions/0009-mobile-first-web-app.md))
- [ ] How often would people open it?
- [x] How do people hear about things? → [0010: Only when something happens to your post](decisions/0010-notifications.md)

---

# Part 2: Technical decisions

Each of these waits on the Part 1 answers listed next to it.

- [x] **Who owns the code and infrastructure** → the founder. The school is a customer ([0012](decisions/0012-account-owner.md)).
- [x] **Hosting** → [0013: Vercel free plan for the trial, revisit after](decisions/0013-hosting.md)
- [x] **Database** → [0014: Supabase (database, sign-in, photos) + daily keep-alive](decisions/0014-database-supabase.md)
- [x] **Sign-in** → [0011: 6-digit email code](decisions/0011-sign-in-with-email-code.md)
- [x] **User identity** → [0004: One email = one account](decisions/0004-one-email-one-account.md), [0005: Roles](decisions/0005-roles-by-action.md)
- [x] **Web app or App Store app** → [0009](decisions/0009-mobile-first-web-app.md)
- [x] **App address (domain)** → [0015: A domain the founder owns](decisions/0015-own-domain.md). Exact name still to pick.
- [x] **Email-sending service** → [0016: Resend](decisions/0016-email-resend.md)
- [x] **App framework and language** → [0017: Next.js + React + TypeScript + Tailwind](decisions/0017-stack.md)

---

# Part 3: Features and details

## What the product is

- [x] **Who can claim giveaways?** → Teachers and admins only, for a classroom ([0005](decisions/0005-roles-by-action.md))
- [x] **What's in v1?** → [0018: Both](decisions/0018-v1-both-flows.md)

## People and roles

- [x] Someone who is both a parent and on staff → teacher role ([0005](decisions/0005-roles-by-action.md))
- [ ] Co-teachers sharing one room's wishlist. (Floaters are covered by [0006](decisions/0006-teachers-any-room.md).)
- [ ] The start of each school year: families leaving, new families joining, kids changing rooms.

## Core flows

- [x] **Browsing** → [0019: Gallery](decisions/0019-gallery-browsing.md)
- [x] **Posting a giveaway: camera** → use the phone's standard camera and photo picker ([0009](decisions/0009-mobile-first-web-app.md)), not a custom camera screen
- [x] **Claims that go stale** → [0020: Claims don't expire; either side can release](decisions/0020-claims-dont-expire.md)
- [ ] **Things that arrive without a claim:** can a teacher close or reduce a need by hand?
- [ ] **"I ordered it online"** from the buy link: is that a claim?
- [ ] **Ongoing needs** ("30 paper towel tubes, no rush") versus dated needs ("rain boots by Thursday"): is that one kind of post or two?
- [ ] **Big items** (a play kitchen) that can't come in at drop-off: how does the handoff work?
- [ ] **The "Mine" screen:** what I've posted, what I've claimed, and what's coming to my classroom.

## Notifications and coming back

Mostly settled by [0010](decisions/0010-notifications.md): email only, sent only when your own post is claimed. A weekly digest and due-date reminders wait until real use shows a need ([principle 3](principles.md)).

## Details

- [ ] Expiration presets: "this weekend" posted on a Sunday, dates that fall on school breaks, what happens to claimed items that expire.
- [ ] Two people claiming the last few at the same moment. The server has to reduce the count safely.
- [ ] Scope creep: selling things, furniture. (Admins can remove posts, per [0005](decisions/0005-roles-by-action.md).)
- [ ] **Launch plan:** pilot with a couple of classrooms or launch to everyone? Note Resend's 100-emails-a-day free limit ([0016](decisions/0016-email-resend.md)). Also the QR poster and newsletter copy.
- [ ] Spam folders: the first sign-in email may land in spam.
