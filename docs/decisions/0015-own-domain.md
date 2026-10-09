# 0015: The app lives at a domain the founder owns

**Status:** Decided (2026-10-08). The exact name isn't picked yet.

## Question
What web address does the app live at, and where do its emails come from?

## Decision
- **A domain the founder buys and owns,** about $10–20 a year. The top pick is `shareshelf.app` or something similar.
- **The app and its emails both use it.** For example, the app at `shareshelf.app` and sign-in codes from `hello@shareshelf.app`.

## Why
- Sign-in codes and notifications have to come from a domain we control, or they land in spam. A free `vercel.app` address can't send email.
- It fits "the founder runs the infrastructure" ([0012](0012-account-owner.md)). It doesn't depend on access to the school's Squarespace domain settings.
- It's cheap and gives flexibility later.

## Options we passed on
- **A free `share-shelf.vercel.app` address:** no email, and it looks unofficial.
- **A subdomain of the school's domain** (`shelf.claytonecc.org`): it looks official, but it depends on whoever controls the school's domain settings.

## Notes
- **Availability (checked 2026-10-08):** `shareshelf.com` is taken. `shareshelf.org`, `shareshelf.io` and `getshareshelf.com` are available. `shareshelf.app`, `.co` and `.school` show no sign of use but weren't confirmed. Check at a registrar.
- **If other schools ever join,** each school's separate copy would get a subdomain (`claytonecc.shareshelf.app`) rather than a path (`shareshelf.app/claytonecc`), because a subdomain can point at a whole separate copy of the app. Nothing to do now ([principle 4](../principles.md)).
- **Account owner:** the founder ([0012](0012-account-owner.md)).
