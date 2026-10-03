# CECC's tech today

What we could learn from the outside about the tools the school already uses (checked 2026-10-02, from claytonecc.org and public DNS records).

## Website: Squarespace
- Runs on **Squarespace**, on an older template generation (7.0). The domain was registered in 2012, and the site has looked roughly the same for years.
- **It is still being edited.** Site content changed on 2026-09-30 (the enrollment banner at the top). So someone at the school can make basic changes in a no-code tool.
- Some signs of light upkeep: pages left with default names like `/new-page-1` and `/new-page-2`, the newest annual report is 2022–23, and the calendar page looks empty.
- The domain's DNS is managed through Squarespace.

**What this suggests:** whoever runs the site is comfortable with a point-and-click editor, but probably not much more, and has limited time. Share Shelf's admin side has to be at least that easy.

## Email: Google Workspace
- `@claytonecc.org` email runs on **Google Workspace**.
- There are shared role addresses: `contact@`, `director@`, `preschool@`, `infant@`, `board@`.
- **Open:** do teachers have their own `@claytonecc.org` addresses? If they do, "Sign in with Google" restricted to the school's domain could identify staff automatically.
- The domain has **no SPF record** (a DNS setting that tells other mail servers who may send email for the domain). If Share Shelf ever sends email *as* `@claytonecc.org`, that would need to be fixed or it would land in spam. Sending from a Share Shelf domain avoids the problem.

## Parent communication: Tadpoles
- The school uses **Tadpoles** for daily reports, photos and messages between teachers and families.
- That means a **family roster already exists** somewhere, and parents are already used to a school app.
- **Open:** can the school export a roster from Tadpoles (or its admin system) to approve families automatically?

## Other things worth knowing
- The school serves ages **6 weeks to 5 years**, not just preschool. Infant rooms are part of the picture, which matters for item safety rules.
- It's licensed by Missouri DESE and follows NAEYC guidelines.
- The board has up to 11 members and a shared `board@` address.
- Leadership: an Executive Director plus separate Preschool and Infant/Toddler program coordinators.
