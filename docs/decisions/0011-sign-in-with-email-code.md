# 0011: Sign in with a 6-digit email code

**Status:** Decided (2026-10-02)

## Question
How do people sign in?

## Decision
Like Substack: **enter your email, get a 6-digit code by email, type it in.** No passwords, and no sign-in link.

## Why
- It's simple, familiar and works well.
- **Code only, no link,** also avoids the iPhone problem from [0009](0009-mobile-first-web-app.md), where a sign-in link opens in a different browser than the installed app. You type the code into whichever app or browser you're already using.
- People stay signed in afterward, on as many devices as they like (see the [0009 addendum](0009-mobile-first-web-app.md)).

## What this affects
- The sign-in email is a required system email ([0010](0010-notifications.md)).
- Codes should expire after a short time, and attempts should be limited.
- **How it's built:** Supabase's built-in email codes ([0014](0014-database-supabase.md)), with the email template set to show the 6-digit code instead of a link.
