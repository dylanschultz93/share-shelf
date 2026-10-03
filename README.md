# Share Shelf

A small web app that helps a preschool community pass things around:

- **Wishlist:** teachers ask for things their classroom needs (Play-Doh, rain boots, paper towel tubes). Parents claim what they can bring.
- **Up for grabs:** families post things they no longer need (a train set, puzzles). Teachers claim what their classroom can use.

Handoff happens at the classroom during drop-off or pickup. There's no shipping, payments or meetups.

It's being built for Clayton Early Childhood Center (CECC), a school for ages 6 weeks to 5 years with 11 classrooms. The code is open source, but it's designed for this one school.

## Status

**Planning.** No app code yet. The repo is mostly markdown while we work through the product and make decisions.

- [`design/`](design/): first-pass screens from Claude Design (sign-in, onboarding, browse, claim, post). Open `design/Share Shelf.dc.html` in a browser to see them.
- [`docs/open-questions.md`](docs/open-questions.md): the decision backlog, ordered from big picture to details.
- [`docs/decisions/`](docs/decisions/): one short file per decision once it's made.

## Working assumptions

These come from the first design pass. They aren't decided yet:

- A mobile web app, not an App Store app. People arrive from a QR poster or a newsletter link.
- Sign-in by email, no passwords. A board member approves each new person once.
- Posting starts with a photo. Posts expire and come down on their own, and the owner gets an email.
- Claims are first come, first served, and can be partial ("I'll bring 3 of the 6").

## Contributing

It's early. For now, the most useful contribution is an opinion on something in [`docs/open-questions.md`](docs/open-questions.md). Open an issue.

## License

[MIT](LICENSE)
