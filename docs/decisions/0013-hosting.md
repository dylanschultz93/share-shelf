# 0013: Host on Vercel's free plan for the trial. Revisit after

**Status:** Decided (2026-10-08)

## Question
Where is the app hosted?

## Decision
- **Vercel, on the founder's account, free (Hobby) plan,** for the trial.
- **Revisit after the trial,** and only if the school adopts it.

## Why
- The founder already uses Vercel. It deploys straight from GitHub and creates a preview link for every change.
- During the trial the app is free to the school, which fits the free plan's non-commercial terms.

## What this affects
- **If the school ever pays,** even just reimbursing costs, that's commercial use, and Vercel's paid plan is about $20 a month. That feels steep for this app, so at that point we'd consider a cheaper host. Any infrastructure costs would be passed through in whatever the school pays. We'll cross that bridge if and when we get there.
- To keep a future move cheap, avoid tying the app to Vercel-only features where a standard option works just as well.
