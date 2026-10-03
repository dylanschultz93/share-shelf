# 0010: Notify people only when something happens to *their* post

**Status:** Decided (2026-10-02)

## Question
How should people find out something new is posted?

## Decision
No notifications about new posts. Email goes out only when something happens to something you posted:

1. **Your donated item was claimed.** The email says who claimed it and which classroom, so you know where to bring it.
2. **Your classroom need was claimed or filled.** The email says who is bringing it and how many.

A weekly digest of new posts is a nice-to-have, so it waits ([principle 3](../principles.md)).

## Why
- Sending an email for every new post would be noisy, and people would tune it out.
- The two emails above are the only times someone *has* to act or know something.

## What this affects
- Email is the only notification channel (see [0009](0009-mobile-first-web-app.md)).
- **Pending:** a few necessary system emails (sign-in, approval), proposed separately.
