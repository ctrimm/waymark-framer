# Decision Log — Waymark (Framer)

## D1 — Name: Waymark (Signpost was taken) (2026-11-17)

The working title "Signpost" failed the collision screen: the
Framer Marketplace already has a premium template named Signpost
(a SaaS documentation site, verified by search + scrape
2026-11-17). Candidates checked by scraping their Marketplace
URLs: Postmark — taken (wedding invite template); Waymark and
Linkpost — "Page not found", i.e. free. **Waymark** chosen: a
waymark is literally a marker that points the way — the same
metaphor, no collision on the Marketplace. (A healthcare company
shares the word; different space, and a template name is not a
product brand. Revisit if this ever becomes a standalone product.)

## D2 — Five styles: the four catalog languages + Brutalist (2026-11-17)

The source Astro theme (`ctrimm/astro-link-in-bio-theme`, 19★)
ships seven looks (brutalist, dev, glassy, modern, pastel, resume,
retro) driven by one config file — the multi-style mechanism is
the original's own, kept. The Framer style set is re-cast:

- **Nocturne, Vermilion, Crumb, Ledger** — the paid catalog's four
  design languages. Each is a free, working sample of a paid
  template (Nocturne $59 live-first; Wagesmith/Ledger $79; Crumb
  Culture and Vermilion Folio next in the port queue). This is the
  lead-gen mechanism: the style table in the guide names the full
  version of each look.
- **Brutalist** — the original's most distinctive look, kept for
  the Framer community's taste and as the nod to the source theme.

Dev / Glassy / Pastel / Resume / Retro dropped: five styles is
already a 45–60 min build; seven adds buyer choice paralysis
without adding a catalog story.

## D3 — Switching architecture: CMS single-source + variants (2026-11-17)

Three supported switch methods, in the order the guide teaches
them: (1) pick-a-page — all five style pages bind to the same
Profile + Links CMS collections, so the buyer previews their real
page in every look and sets the winner as home; (2) component
Style variants — Profile Card / Link Button / Socials Row each
carry all five looks as a variant property, so a single page can
be re-skinned in place; (3) Color/Text Styles — each style's
tokens exist as named Framer styles, so re-branding a look is a
style edit, not a frame hunt. The pick-a-page method is primary
because it needs zero Framer skill; variants are the power path.

## D4 — Free, public repo, as-is (2026-11-17)

Unlike Nocturne/Wagesmith (private repos — the package is the paid
product), Waymark's product is distribution itself, so the repo is
public, matching the public Astro original. Revenue is indirect:
Framer referral share (50% of a referred subscription's first
year) + paid-catalog discovery. Listing states "as-is, no
support" — at free, support time would eat the sprint.

## D5 — Sequencing note (2026-11-17)

Built before the paid listings are live in Framer (Cory's call,
overriding the earlier sequence-after-paid recommendation). The
guide's style table therefore names the paid templates without
links; the checklist carries an aftercare step to add listing
URLs to the Start here page once Nocturne and Wagesmith are live.
