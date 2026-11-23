# Waymark — Submission Checklist

Framer mechanics verified against Framer's official help centre
(2026-11-16, see SOURCES.md): templates publish **immediately** on
submit — no manual review. Creators keep 100% of template sales;
Waymark is free, so the economics here are the **referral share
(50% of a referred Framer subscription's first year)** — which is
why the remix flow must be frictionless.

## Status — 2026-11-23 moderation pass (verified)

Against Framer's Template Best Practices; see DECISION_LOG D8.

- [x] Every sample link resolves: 6 Links CMS rows and the 3 social buttons on all 10 style pages moved off example.com to real platform homepages; "Say hello" row + Email button → mailto:cory@ignitebright.com. Zero example.com left anywhere in the project
- [x] Link sweep on the republished preview (version 91850c14d): 12 pages × 320/390/1440px = 453 link instances, 22 unique destinations, 0 dead; 56 real taps at iPhone width on Nocturne, Vermilion, Dev and Retro, 0 failures
- [x] Hover + pressed states on every link: pressed state added to Link Button (20 variants), Start here chips and 404 button; hover + pressed added to the social chips; hover added to the footer links
- [x] No horizontal scroll or broken layout at 320 / 390 / 1440px on all 10 styles, Start here and 404
- [x] No forms in the project (nothing to connect)
- [x] Custom 404 exists, on-brand, "Back to the links" button works; served with HTTP 404
- [x] Title + description set on all 12 pages; no lorem/placeholder text on any live page
- [x] No unused components (all 4 used), colour styles (77) or text/link styles (16); no empty CMS entries
- [ ] Demo video swap BLOCKED: waymark-demo-v2-hardcut.mp4 was not reachable from the build session; current marketplace/demo.mp4 (crossfade cut) is known-defective — swap before upload
- [ ] GoReview audit NOT RUN: it is a Framer editor plugin; needs Cory in the editor
- [ ] Remix link tested in a clean second Framer account — not done
- [ ] Manual, Cory only: Site Settings → "Optimized" status; File → Copy Remix Link; Submit

## Status — 2026-11-21 evening (verified)

- [x] Preview republished and curl-verified: https://lovely-pictogram-627853.framer.app (version d176a9a93) — / and /start return 200 with correct titles
- [x] CMS structure audit (read-only, via Framer MCP): exactly one Profile collection (1 item) and one Links collection (7 items), no drafts; all 10 style pages bind to those same collections; no unused entries. Unused field Profile → Email removed (binding was not possible for both links: "Say hello" is a Links row with its own URL field), republished as version d7a20d5f4 and curl-verified; cms/SCHEMA.md + cms/profile.csv updated to match
- [x] Demo video replaced with the style-cycling cut (8 styles, crossfades, 18.2s, 1080p) in marketplace/demo.mp4 — superseded 2026-11-23: crossfades double the labels; hard-cut swap pending (see above)
- [x] Gallery recaptured badge-free: "Made in Framer" badge + edit button removed from the DOM before screenshot; all 11 PNGs, same filenames/sizes, each read back clean
- [ ] Manual, Cory only: Site Settings → Staging & Versions "Optimized" status; File → Copy Remix Link; the 3 live switch tests; Submit

## Build (from FRAMER_BUILD_SPEC.md)

- [x] CMS collections created; CSVs imported (Profile 1 item, Links 7)
- [x] Profile Card / Link Button / Socials Row components, all 10 Style variants
- [x] Color Styles created per style and applied (no raw hex on frames)
- [x] 10 style pages + Start here page + custom 404
- [x] Nocturne set as home page for the listing preview
- [x] All links are real — real platform homepages + working mailto: (example.com targets replaced 2026-11-23)
- [x] Footer Badge present on all style pages, linked to the listing (placeholder: Marketplace home until the listing URL exists)
- [x] Favicon + site title set

## Quality pass

- [x] Preview each style page at phone width — column centred, no overflow
- [ ] Switch test: edit one link label in CMS → confirm it changes on all 10 pages
- [ ] Variant test: flip one Link Button's Style → renders correctly
- [ ] Method 1 test: re-set home to another style page → publishes correctly
- [x] Start here page reads cleanly and its internal links work (all 10 style chips return 200, 2026-11-23)
- [x] No lorem ipsum anywhere; demo content is the June Calloway set (live text scan of all 12 pages, 2026-11-23)
- [ ] Avatar image has alt text (set it in the CMS image when a photo is added; demo uses initials); per-page title + description set on all pages (10 styles + Start here + 404) — titles/descriptions done
- [ ] Framer performance check reviewed on the published preview; avatar image compressed
- [x] Unused CMS entries/fields deleted (best practice: no empty or unused entries ship) — Profile → Email removed 2026-11-21; no unused entries
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
