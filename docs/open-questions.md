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
- [ ] Who removes posts and fixes problems? (Probably the same admin.)
- [x] ~~Use the school's family roster?~~ No. Procare matching was ruled out in [0002](decisions/0002-who-gets-in.md).
- [x] Money → [0003: Aim for free; school pays at cost later](decisions/0003-cost.md)

## C. The community
- [x] Roughly how many families and staff? → [research/cecc-size.md](research/cecc-size.md)
- [ ] One adult per family using it, or two?
- [ ] How people relate to each other: families, staff, board, and anyone who is more than one of those.

## D. Trust and privacy
- [ ] Who should see what? What's sensitive?
- [ ] How sure do we need to be that someone really belongs to the school?

## E. Everyday use
- [ ] What devices do people use? How often would they open it?
- [ ] How do people find it, and how do they hear about new things?

---

# Part 2: Technical decisions

Each of these waits on the Part 1 answers listed next to it.

- [ ] **Hosting** (A, B)
- [ ] **Database** (B, C, D). At this school's size, volume isn't a concern. Who runs it and how matters more.
- [ ] **Sign-in** (D, E). Note: on iPhone, an email link alone can open in the wrong browser. An email with both a link and a code avoids that.
- [ ] **User identity:** individual accounts or households, and roles (C, D)
- [ ] **Web app or App Store app** (E). The working assumption is a mobile web app.
- [ ] **Email and notifications** (E)

---

# Part 3: Features and details

## What the product is

- [ ] **Who can claim giveaways?** Teachers only, or parents from other parents too? The design says everyone sees both tabs, but 1h says "if a *teacher* claims it." Teachers only keeps every handoff at a classroom. Parent to parent adds pickups, contact between families and moderation.
- [ ] **What's in v1?** Wishlist only, Up for grabs only, or both? The wishlist (teacher asks, parent brings it to the classroom) has the clearest value and the fewest edge cases.

## People and roles

- [ ] Someone who is both a parent and on staff. 1b makes them pick one.
- [ ] Households with more than one adult: two parents, split households, grandparents or nannies who do drop-off.
- [ ] Staff with no classroom (director, floaters), co-teachers sharing one wishlist.
- [ ] The start of each school year: families leaving, new families joining, kids changing rooms.

## Core flows

- [ ] **Browsing:** gallery (1c) or swipe (1d)? The leaning is gallery for everyone, filtered to your child's rooms and sorted by urgency.
- [ ] **Posting a giveaway:** keep the custom camera screen (1g), or use the phone's standard camera and photo picker?
- [ ] **Claims that go stale:** someone claims and never brings it. Does the claim expire? Can the teacher reopen it?
- [ ] **Things that arrive without a claim:** can a teacher close or reduce a need by hand?
- [ ] **"I ordered it online"** from the buy link: is that a claim?
- [ ] **Ongoing needs** ("30 paper towel tubes, no rush") versus dated needs ("rain boots by Thursday"): is that one kind of post or two?
- [ ] **Big items** (a play kitchen) that can't come in at drop-off: how does the handoff work?
- [ ] **The "Mine" screen:** what I've posted, what I've claimed, and what's coming to my classroom.

## Notifications and coming back

- [ ] Email only, or also push notifications for people who add it to their home screen?
- [ ] A weekly digest email ("3 new asks in Owl room"): opt in or opt out? Which day?
- [ ] Reminder the day before a claimed item is due.
- [ ] Thanking people and closing the loop without photos of children.
- [ ] Keeping it from feeling like pressure: no leaderboards, and not showing who gave what.

## Details

- [ ] Expiration presets: "this weekend" posted on a Sunday, dates that fall on school breaks, what happens to claimed items that expire.
- [ ] Two people claiming the last few at the same moment. The server has to reduce the count safely.
- [ ] Moderation: who can take a post down, and scope creep (selling things, furniture).
- [ ] The QR poster and newsletter copy for launch.
- [ ] Spam folders: the first sign-in email may land in spam.
