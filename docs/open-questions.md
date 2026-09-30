# Open questions

The backlog of decisions still to make. **Tier 1** shapes everything else, so it comes first. Later tiers get more detailed and mostly depend on earlier answers.

When a question is settled, write it up in [`decisions/`](decisions/) and check it off here with a link.

The screen references (1a–1j) point to [`design/Share Shelf.dc.html`](../design/Share%20Shelf.dc.html).

---

## Tier 1: What the product is

These change the scope, the data model and who the app is for.

- [ ] **Who can claim giveaways?** Teachers only, or parents from other parents too? The design says everyone sees both tabs, but 1h says "if a *teacher* claims it." Teachers only keeps every handoff at a classroom. Parent to parent adds pickups, contact between families and moderation.
- [ ] **What's in v1?** Wishlist only, Up for grabs only, or both? The wishlist (teacher asks, parent brings it to the classroom) has the clearest value and the fewest edge cases.
- [ ] **Is this for CECC only, or built for any school?** This affects how much gets hardcoded (classroom names, branding, the approval flow) and whether multiple schools could ever share one install.
- [ ] **Who runs it long term?** Who owns the accounts, pays for the domain and handles problems once the founding parent's kid has aged out? The answer should push the stack toward low maintenance.
- [ ] **Does the center have rules about what can come into a classroom?** Licensed centers often ban recalled toys, choking hazards in toddler rooms, car seats and cribs, and food. Ask the director. This may shape what can be posted at all.

## Tier 2: Platform and access

- [ ] **Web app or App Store app?** The working assumption is a mobile web app that can be added to the home screen, because people arrive from a QR code or an email link.
- [ ] **How does sign-in work?** An email link alone breaks on iPhone when the link opens in the wrong browser (for example, inside the Gmail app). The proposal is an email with both a link and a 6-digit code.
- [ ] **How do people get approved?** A board member approves each new person (1b). Could we instead approve people automatically from a family roster or a staff email domain, and only send unknown people to the board?
- [ ] **Stack.** The proposal is Next.js on Vercel, Supabase (database, sign-in, photo storage) and Resend (email), all on free tiers. This depends on the "who runs it" answer.
- [ ] **What's the privacy stance?** For example: no children's faces in photos, whether giver names are shown, and what's visible to people who haven't been approved yet.

## Tier 3: People and roles

- [ ] Someone who is both a parent and on staff. 1b makes them pick one.
- [ ] Households with more than one adult: two parents, split households, grandparents or nannies who do drop-off.
- [ ] Staff with no classroom (director, floaters), co-teachers sharing one wishlist.
- [ ] The start of each school year: families leaving, new families joining, kids changing rooms.

## Tier 4: Core flows

- [ ] **Browsing:** gallery (1c) or swipe (1d)? The leaning is gallery for everyone, filtered to your child's rooms and sorted by urgency.
- [ ] **Posting a giveaway:** keep the custom camera screen (1g), or use the phone's standard camera and photo picker?
- [ ] **Claims that go stale:** someone claims and never brings it. Does the claim expire? Can the teacher reopen it?
- [ ] **Things that arrive without a claim:** can a teacher close or reduce a need by hand?
- [ ] **"I ordered it online"** from the buy link: is that a claim?
- [ ] **Ongoing needs** ("30 paper towel tubes, no rush") versus dated needs ("rain boots by Thursday"): is that one kind of post or two?
- [ ] **Big items** (a play kitchen) that can't come in at drop-off: how does the handoff work?
- [ ] **The "Mine" screen:** what I've posted, what I've claimed, and what's coming to my classroom.

## Tier 5: Notifications and coming back

- [ ] Email only, or also push notifications for people who add it to their home screen?
- [ ] A weekly digest email ("3 new asks in Owl room"): opt in or opt out? Which day?
- [ ] Reminder the day before a claimed item is due.
- [ ] Thanking people and closing the loop without photos of children.
- [ ] Keeping it from feeling like pressure: no leaderboards, and not showing who gave what.

## Tier 6: Details

- [ ] Expiration presets: "this weekend" posted on a Sunday, dates that fall on school breaks, what happens to claimed items that expire.
- [ ] Two people claiming the last few at the same moment. The server has to reduce the count safely.
- [ ] Moderation: who can take a post down, and scope creep (selling things, furniture).
- [ ] The QR poster and newsletter copy for launch.
- [ ] Spam folders: the first sign-in email may land in spam.
