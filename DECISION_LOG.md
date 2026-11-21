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

## D6 — The five originals restored as riffs (2026-11-17, Cory's call)

Cory directed adding the Astro original's remaining looks back —
D2's drop is superseded. Dev, Glassy, Pastel, Resume and Retro
join as **riffs**, not ports: each is grounded in its original
config (Glassy's dark slate + backdrop image, Pastel's watercolor
wash, Retro's black + retro-grid + neon palette, Resume's slate
professionalism, Dev's code-first identity) and rebuilt to the
Waymark token standard — every text pair re-verified ≥ 4.5:1
(Pastel's muted needed darkening to `#755C4C`, 5.46:1, to pass).
Ten styles total. The original's eighth variant, Modern, stays
out: it was the default baseline look, not a style. Cost of the
change: component variant count doubles (20 Link Button states)
and the in-Framer build estimate rises to 60–75 minutes — worth
it, per Cory: more options is the point of a link-in-bio template,
and the originals are what the Astro theme's 19★ audience knows.

## D5 — Sequencing note (2026-11-17)

Built before the paid listings are live in Framer (Cory's call,
overriding the earlier sequence-after-paid recommendation). The
guide's style table therefore names the paid templates without
links; the checklist carries an aftercare step to add listing
URLs to the Start here page once Nocturne and Wagesmith are live.

## D7 — In-Framer build notes (2026-11-21)

Built in a new, empty Framer project ("Waymark — Link in Bio",
https://framer.com/projects/ilbNe2m8lZoHDjilIuyB) with the Framer
connector, then checked page by page against `marketplace/*.png`.
Where the build differs from the spec, and why:

- **Link Button hover.** Framer won't put a hover effect on a variant's
  root, so each variant wraps a "Surface" frame that holds the
  styling, the link and the hover (lift 1px; Brutalist moves its
  shadow from 4px to 6px). There are still 20 variants (10 styles,
  each with a Highlight version). On the pages the variant comes from
  the CMS Highlight toggle, and the Vermilion number (01–07) comes
  from the list's item index.
- **Socials Row props.** The Socials Row sits inside the Profile Card,
  and the card passes its four label + link props through. Buyers
  edit socials on the Profile Card, and switching the card's variant
  switches its Socials Row too. The guide was updated to say this.
- **Text Styles.** Each style has one Text Style, `<Style> / Name`
  (the display font). UI text is set inline per variant, because one
  fixed-size style per role × 10 looks would add 50+ near-identical
  styles. The Start here page has its own `Guide / …` text and colour
  styles.
- **Backgrounds.** Framer fills take one gradient, so Glassy's aurora
  is a linear base plus two radial glow layers, Pastel's wash is a
  linear gradient, and Retro's 28px grid is an SVG pattern layer.
  Each style page has a Desktop and a Phone breakpoint.
- **Footer Badge.** A single component with a Text Color prop and a
  Listing Link prop. The link points at the Marketplace home until
  the listing URL exists (checklist aftercare). The badge always uses
  Manrope; the preview mock switched it to mono on Brutalist, Dev
  and Retro.
- **Demo location.** It now reads "Savannah, GA", to match the mock;
  `cms/profile.csv` was updated to the same text.
- **Canvas linter.** Component variants are deliberately transparent
  (they sit on each page's style background, including the gradient
  pages), so Framer's "opaque background" / contrast warnings on the
  component canvas are expected. The real backgrounds on the pages
  pass.
