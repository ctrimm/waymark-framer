# Waymark — Submission Checklist

Framer mechanics verified against Framer's official help centre
(2026-11-16, see SOURCES.md): templates publish **immediately** on
submit — no manual review. Creators keep 100% of template sales;
Waymark is free, so the economics here are the **referral share
(50% of a referred Framer subscription's first year)** — which is
why the remix flow must be frictionless.

## Status — 2026-11-21 evening (verified)

- [x] Preview republished and curl-verified: https://lovely-pictogram-627853.framer.app (version d176a9a93) — / and /start return 200 with correct titles
- [x] CMS structure audit (read-only, via Framer MCP): exactly one Profile collection (1 item) and one Links collection (7 items), no drafts; all 10 style pages bind to those same collections; no unused entries. One unused field: Profile → Email is bound nowhere (buttons use a typed mailto:) — fix-or-delete is Cory's call, tracked in the Claude handoff
- [x] Demo video replaced with the style-cycling cut (8 styles, crossfades, 18.2s, 1080p) in marketplace/demo.mp4
- [ ] Gallery badge fix pending: live-site captures carry the "Made in Framer" badge + edit button (phone shots partly covered). Recapture with the badge element removed before screenshot — in the Claude handoff
- [ ] Manual, Cory only: Site Settings → Staging & Versions "Optimized" status; File → Copy Remix Link; the 3 live switch tests; Submit

## Build (from FRAMER_BUILD_SPEC.md)

- [x] CMS collections created; CSVs imported (Profile 1 item, Links 7)
- [x] Profile Card / Link Button / Socials Row components, all 10 Style variants
- [x] Color Styles created per style and applied (no raw hex on frames)
- [x] 10 style pages + Start here page + custom 404
- [x] Nocturne set as home page for the listing preview
- [x] All links are real (example.com demo targets, real mailto:)
- [x] Footer Badge present on all style pages, linked to the listing (placeholder: Marketplace home until the listing URL exists)
- [x] Favicon + site title set

## Quality pass

- [x] Preview each style page at phone width — column centred, no overflow
- [ ] Switch test: edit one link label in CMS → confirm it changes on all 10 pages
- [ ] Variant test: flip one Link Button's Style → renders correctly
- [ ] Method 1 test: re-set home to another style page → publishes correctly
- [ ] Start here page reads cleanly and its internal links work
- [ ] No lorem ipsum anywhere; demo content is the June Calloway set
- [ ] Avatar image has alt text (set it in the CMS image when a photo is added; demo uses initials); per-page title + description set on all pages (10 styles + Start here + 404) — titles/descriptions done
- [ ] Framer performance check reviewed on the published preview; avatar image compressed
- [ ] Unused CMS entries/fields deleted (best practice: no empty or unused entries ship)
- [ ] Cross-sell check: paid-template mentions live ONLY on the Start here page; the Footer Badge is template attribution and removable (no ads on buyer pages)

## Publish + list

- [x] Publish the preview site (done 2026-11-21, URL above); open the Preview URL in a private window — still Cory's check
- [ ] Remix link copied from the share dialog; test it in a private window
- [ ] Creator → New Template: name, byline, description (from MARKETPLACE_LISTING.md)
- [ ] Categories: Link in Bio / Personal / Portfolio
- [ ] Price: **Free** (no Stripe step for this one)
- [ ] Upload the 11 marketplace images from `marketplace/`
- [ ] Submit → template is live immediately
- [ ] Optional but Framer-recommended: publish the Community feed post with the personal message drafted in `MARKETPLACE_LISTING.md`
- [ ] After it's live: add the listing URL to the Footer Badge link in the project and republish the preview
- [ ] Live check: open the Marketplace page, remix it as a stranger would, confirm the Start here page is intact

## Aftercare

- [ ] Add the listing URL + launch date to this repo's README
- [ ] When Nocturne / Wagesmith listings go live, update the guide's style table links in the Framer project (one edit on the Start here page)
