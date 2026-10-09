# 0017: Next.js + React + TypeScript + Tailwind

**Status:** Decided (2026-10-08)

## Question
What framework and language is the app built with?

## Decision
**Next.js (App Router) + React + TypeScript + Tailwind CSS**, the same stack as the founder's other projects.

## Why
- The founder already knows it, so the new learning can go to Supabase ([0014](0014-database-supabase.md)).
- Next.js is made by Vercel, so it fits the hosting best ([0013](0013-hosting.md)).
- Supabase has official Next.js guides and tools, including for sign-in.
- The design's colors and fonts (`design/ds/styles.css`) map directly onto Tailwind's theme, so the app will match the Claude Design files.

## Options we passed on
None seriously. There was no reason to choose differently.
