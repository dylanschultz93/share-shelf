# 0004: One email = one account. No family grouping

**Status:** Decided (2026-10-02)

## Question
In a family, does one parent use the app or both? Is an account a person or a family?

## Decision
- **An account is just an email address.** Whoever signs in with that email uses that account.
- Parents with **separate emails** get separate accounts. Parents who **share an email** share an account. Both cases work without anything special.
- **No family grouping.** The app doesn't link spouses or households together.
- **Duplicates are fine.** If two parents in one family both claim the same thing, so be it. Nothing in the app prevents it.

## Why
- This handles the harder case (separate emails) and the easy case (shared email) with the same simple model.
- Linking families is a feature the app works without ([principle 3](../principles.md)), and preventing duplicates is policing behavior before it's a real problem ([principle 2](../principles.md)).

## What this affects
- The starting email list ([0002](0002-who-gets-in.md)) can include both parents' emails when we have them.
- Each account picks its own classroom(s). Two parents in one family each pick theirs.
- No "household" anywhere in the data model.
