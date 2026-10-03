# 0009: A mobile-first web app that can be installed

**Status:** Decided (2026-10-02)

## Question
Where will people use it: phones, computers, or both? And is it an app-store app?

## Decision
- **A web app, not an app-store app.** People open it from a link.
- **Designed for phones first.** Every screen is designed for a phone, then given a simple layout that also works well on a computer or iPad.
- **Installable.** It can be saved to a phone's home screen and opened like an app (a "progressive web app," or PWA) for people who like that. Nobody has to.

## Why
- People are mostly on their phones, especially when photographing items to post.
- Teachers will probably use their classroom iPads, so tablets need to work well too.
- No app store means no download step, no store review and no developer accounts, and the QR poster and email links go straight in. It also fits "don't add another required app" (see [research](../research/school-tech-today.md)).

## What this affects
- **Sign-in has to survive the "opened from an email" case.** On iPhone, a sign-in link can open in a different browser than the installed app. Sending a link *and* a short code in the same email avoids that. This gets decided under sign-in.
- **Push notifications are limited.** On iPhone, web apps can only send push notifications if they're installed to the home screen. Email will be the main way to reach people.
- **Taking photos uses the phone's standard camera and photo picker**, which web apps can open directly.

## Addendum: shared classroom iPads (2026-10-02)
- **Teachers sharing one signed-in account on a classroom iPad is fine.** Posts may show whichever teacher is signed in. The classroom is what matters. No sign-out or PIN switching.
- **Teachers will also use their own phones or computers at home,** for example to add wishlist items after work. So one account has to stay signed in on several devices at once.
