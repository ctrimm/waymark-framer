# Waymark — a free Framer link-in-bio template with five switchable styles

**Status: build package complete; the in-Framer build is the
remaining step.** This repo is the full template package — build
spec, the switching guide that ships inside the template, CMS
content, listing copy and submission checklist. Framer has no API
for creating template projects, so the project itself gets built
in Framer from `FRAMER_BUILD_SPEC.md` (~45–60 min).

Waymark is the Framer edition of
[astro-link-in-bio-theme](https://github.com/ctrimm/astro-link-in-bio-theme)
(19★), re-cast as a sampler of this catalog's design languages.

## Screenshots

The preview's style switcher — the same mechanism the template
teaches (content lives in the CMS once; styles are pages/variants
reading from it):

![The style switcher with the Nocturne style active](marketplace/01-switcher.png)

![Nocturne style](marketplace/02-nocturne.png)

![Vermilion style — numbered links](marketplace/03-vermilion.png)

![Crumb style](marketplace/04-crumb.png)

![Ledger style](marketplace/05-ledger.png)

![Brutalist style](marketplace/06-brutalist.png)

## The idea

Most link-in-bio templates make you pick a look before you've seen
your own page in it. Waymark keeps the profile and links in the
CMS — one place — and ships five style pages that all read from
it. Fill in your links once, preview your page in all five looks,
set the winner as home, publish. Switching later takes a minute
because the content never moves.

| Style | Look | Free taste of |
|---|---|---|
| **Nocturne** | espresso + copper, dark editorial | Nocturne (supper-club sites, $59) |
| **Vermilion** | paper + vermilion, numbered links | Vermilion Folio (editorial portfolios) |
| **Crumb** | cream + burnt crust, warm pills | Crumb Culture (bakery/café) |
| **Ledger** | paper + ledger green, small caps | Wagesmith (payroll/SaaS, $79) |
| **Brutalist** | black/white + signal yellow, hard shadows | the original Astro theme's signature look |

## Switching, three ways (the guide in one paragraph)

1. **Pick a page** — preview all five with your content, set one
   as home. Zero skill required.
2. **Flip a variant** — Profile Card, Link Button and Socials Row
   each carry all five styles as a variant property; re-skin a
   page in place.
3. **Edit the styles** — every token exists as a named Color/Text
   Style per look; change the style, change the look.

The full buyer-facing version is `SWITCHING_GUIDE.md` — it ships
inside the template as the "Start here" page.

## Package contents

```
FRAMER_BUILD_SPEC.md      Pages, components, variants, tokens (all contrast-verified)
SWITCHING_GUIDE.md        The buyer guide / in-template Start here page
MARKETPLACE_LISTING.md    Paste-ready free listing (price: FREE)
SUBMISSION_CHECKLIST.md   Build → quality → publish → list → aftercare
DECISION_LOG.md           Why Waymark, why five styles, why CMS-first
cms/                      SCHEMA.md + import-ready Profile and Links CSVs
preview/                  Interactive style-switcher preview (open index.html)
marketplace/              Listing screenshots from the verified preview
SOURCES.md                Framer's official template guidance, retrieved 2026-11-16
```

## Why free?

Waymark's job is discovery: Framer signups through the remix link
(creators earn 50% of a referred subscription's first year) and a
working sample of the paid catalog's four design languages in
every download. It's provided as-is, without support — the Start
here page is the manual.

## License

Template design and package © Cory Trimm. Demo content (June
Calloway) is fictional.
