# 0014: Supabase for the database, sign-in and photos

**Status:** Decided (2026-10-08)

## Question
Which database, and where do photos and sign-in live?

## Decision
**Supabase, free plan,** on the founder's account ([0012](0012-account-owner.md)). It covers:
- **The database:** standard Postgres.
- **Sign-in:** Supabase's built-in email codes give us the 6-digit flow from [0011](0011-sign-in-with-email-code.md).
- **Item photos:** Supabase's built-in file storage.
- **Security rules in the database itself,** for example that unapproved users can't post or claim ([0008](0008-browse-before-approval.md)). This is a second safety layer behind the app's own checks.

Plus:
- **A daily keep-alive job.** Free Supabase projects pause after 7 days with no activity. A scheduled job on Vercel runs a tiny query once a day so the project never goes idle, and it alerts the founder by email if it fails.
- **A separate email-sending service.** Supabase's built-in email only reaches the project's own team, so it can't be used with real users. Which service is still to be decided.

## Why
- **Sign-in is already built and tested.** Code for sign-in is where mistakes cause security problems, so not writing it ourselves is the biggest win.
- Fewer services than the alternative (Neon plus Vercel Blob plus homemade sign-in), and more free storage.
- The founder has used Neon before and wants to learn Supabase.

## Options we passed on
- **Neon + Vercel Blob + our own sign-in code.** It wakes up automatically with no keep-alive needed, but it means more services and we'd build sign-in ourselves.

## Risks
- **The keep-alive is a workaround,** not a guarantee. If Supabase changes its rules, the options are the paid plan (about $25 a month) or moving.
- **Ties us to one vendor:** sign-in and photo storage are Supabase-specific. The data itself is standard Postgres and can move anywhere. Acceptable under [principle 4](../principles.md).
- If the keep-alive fails for a week, the project pauses. It can be restarted with a click and no data is lost, which is why the job alerts on failure.
