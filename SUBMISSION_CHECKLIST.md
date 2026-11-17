# Waymark — Submission Checklist

Framer mechanics verified against Framer's official help centre
(2026-11-16, see SOURCES.md): templates publish **immediately** on
submit — no manual review. Creators keep 100% of template sales;
Waymark is free, so the economics here are the **referral share
(50% of a referred Framer subscription's first year)** — which is
why the remix flow must be frictionless.

## Build (from FRAMER_BUILD_SPEC.md)

- [ ] CMS collections created; CSVs imported (Profile 1 item, Links 7)
- [ ] Profile Card / Link Button / Socials Row components, all 10 Style variants
- [ ] Color Styles created per style and applied (no raw hex on frames)
- [ ] 10 style pages + Start here page + custom 404
- [ ] Nocturne set as home page for the listing preview
- [ ] All links are real (example.com demo targets, real mailto:)
- [ ] Footer Badge present on all style pages, linked to the listing
- [ ] Favicon + site title set

## Quality pass

- [ ] Preview each style page at phone width — column centred, no overflow
- [ ] Switch test: edit one link label in CMS → confirm it changes on all 10 pages
- [ ] Variant test: flip one Link Button's Style → renders correctly
- [ ] Method 1 test: re-set home to another style page → publishes correctly
- [ ] Start here page reads cleanly and its internal links work
- [ ] No lorem ipsum anywhere; demo content is the June Calloway set

## Publish + list

- [ ] Publish the preview site; open the Preview URL in a private window
- [ ] Remix link copied from the share dialog; test it in a private window
- [ ] Creator → New Template: name, byline, description (from MARKETPLACE_LISTING.md)
- [ ] Categories: Link in Bio / Personal / Portfolio
- [ ] Price: **Free** (no Stripe step for this one)
- [ ] Upload the 11 marketplace images from `marketplace/`
- [ ] Submit → template is live immediately
- [ ] After it's live: add the listing URL to the Footer Badge link in the project and republish the preview
- [ ] Live check: open the Marketplace page, remix it as a stranger would, confirm the Start here page is intact

## Aftercare

- [ ] Add the listing URL + launch date to this repo's README
- [ ] When Nocturne / Wagesmith listings go live, update the guide's style table links in the Framer project (one edit on the Start here page)
