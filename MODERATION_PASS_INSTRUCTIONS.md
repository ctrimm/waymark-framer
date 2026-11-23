# Waymark — Moderation Pass Instructions (2026-11-23)

**Context:** Framer abolished pre-publish template review in Framer 3.0 (Jun 2026). Publishing is instant; moderation is post-publish (user reports + automated systems + human moderators) judged against the official **Template Best Practices** checklist (framer.com/help/articles/template-best-practices). Wagesmith was removed hours after publishing on Nov 22 under this system. Waymark is free and not yet submitted — this pass hardens it **before** Cory submits, so there is nothing for a reporter or moderator to point at. **Do not submit or publish anything** — Cory submits.

Framer project: **Waymark** (`ilbNe2m8lZoHDjilIuyB`). Repo: `ctrimm/waymark-framer` (**public** — author all commits as Cory Trimm, no co-author trailers).

## The pass, in order

1. **Replace the demo video.** `marketplace/demo.mp4` on main is defective — its crossfades double every on-screen text label mid-transition (frame-verified 2026-11-22). Replace it with the verified hard-cut rebuild at `~/workspace/previews-framer/waymark/waymark-demo-v2-hardcut.mp4` (18.8s, frame-checked clean). Commit the swap on the same branch as the rest of this pass.
2. **Make every sample link resolve.** A link-in-bio template lives or dies on its links. Every entry in the Links CMS and every button on all 10 style pages must point to a real, loading destination (platform homepages or other stable generic URLs) — no dead, empty, or `example.com`-style placeholder URLs. The "Say hello" row and Email button must carry a correct working `mailto:`.
3. **Forms, if any exist.** Waymark is not expected to have a form; if you find one anywhere, connect it via Framer's built-in handling to **cory@ignitebright.com** with labelled fields and a visible success state, per the catalog pattern.
4. **Custom 404.** Verify a custom 404 page exists, is styled on-brand, and has a working link back. Create it if missing. (Explicitly on Framer's official checklist.)
5. **Full best-practices sweep, all 10 style pages.** Click every link and button on every style page — fix or remove anything dead; hover/active states present. Remove empty and unused CMS entries (Profile, Links), unused components, styles, and pages. Confirm every page has a title and description in site settings. Meaningful alt text on images (including the profile photo). Check every breakpoint including ~320px wide — no horizontal scroll, overflow, or broken layout on any of the 10 styles.
6. **Gallery accuracy.** Confirm the marketplace gallery images and the (new) demo video represent the current build of all 10 styles.
7. **Run the GoReview audit** (free plugin, built against Framer's checklist). Fix every error-level finding. Note any warnings you leave, and why.
8. **Republish the preview site**, then test as a stranger: click through at least three style pages at phone width and follow every link; test the remix link in a clean/second Framer account if you have one — if you can't, report it as unchecked, don't claim it.
9. **Update the repo** on a branch + PR (do not merge): `MARKETPLACE_LISTING.md` and `SUBMISSION_CHECKLIST.md` (tick what's now true), and a dated `DECISION_LOG.md` entry recording this pass, the demo swap, and each fix.

## Report back

Fixes mapped point-by-point to the Template Best Practices checklist · the updated preview URL · GoReview results (errors fixed, warnings left + why) · link-sweep result (how many links checked, any dead ones found) · repo PR link · checked vs unchecked stated plainly.
