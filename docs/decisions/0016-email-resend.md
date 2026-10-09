# 0016: Resend sends the emails

**Status:** Decided (2026-10-08)

## Question
Which service sends sign-in codes and notifications?

## Decision
**Resend, free plan,** on the founder's account, sending from the app's own domain ([0015](0015-own-domain.md)). Supabase sends its sign-in codes through Resend too ([0014](0014-database-supabase.md)).

## Why
- It's the email service built into Vercel's marketplace, it works well with Supabase, and it's simple.
- **Free plan: 3,000 emails a month, at most 100 a day.** Normal use (a few sign-in codes and claim notices a day) is far below that.

## What this affects
- **Launch day could exceed 100 sign-ins.** That's a good problem to have. Options: launch with a couple of pilot classrooms first, launch in waves, or pay for one month around launch. Decide when we plan the launch.
