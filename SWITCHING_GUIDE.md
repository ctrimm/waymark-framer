# Switching styles in Waymark — the buyer guide

*This guide ships inside the template as the "Start here" page, and
as the support doc linked from the Marketplace listing. It is
written for the buyer, in plain language.*

---

## How Waymark works (30 seconds)

Your name, bio and links live in **one place**: the CMS collections
called **Profile** and **Links**. Every style page reads from those
same collections. So you edit your content **once**, and all ten
styles instantly show *your* page — you pick the look you like
best, and you can change your mind any time without re-typing
anything.

## Method 1 — Pick a style page (recommended)

1. Open the **CMS** (left sidebar) → **Profile** and **Links**.
   Replace the demo content with yours.
2. Click through the ten style pages — **Nocturne, Vermilion,
   Crumb, Ledger, Brutalist, Dev, Glassy, Pastel, Resume,
   Retro** — and look at your page in each.
3. On the page you want: open its **Page Settings** and set its
   route to `/`. Framer moves the home page to your pick.
4. Delete the other nine style pages (or keep them — unpublished
   pages cost nothing, and you can re-test a new look later).
5. **Publish.**

That's it. Switching later = repeat steps 3–5 with a different
page. Your links never move.

## Method 2 — Flip the Style variant

Every building block (Profile Card, Link Button, Socials Row) has the
ten looks as variants. The Profile Card brings its Socials Row along
when you switch it.

1. Select the block on any page.
2. In the right-hand properties panel, change its variant from, say,
   *Crumb* to *Ledger*.
3. Do the same for the other blocks, and set the page background
   to the matching colour (each style's background hex is in the
   table below).

Useful when you want one page but a different look — or a mix
(a Nocturne profile card over Ledger buttons is surprisingly good).

## Method 3 — Make a style your own

Each style is driven by named **Color Styles** (Assets → Waymark
Colors: `Nocturne / Background`, `Nocturne / Accent`, …) and a
**Text Style** for its display name (Assets → Waymark Text:
`Nocturne / Name`, …). Edit the style and every block using it
updates:

- Change the accent colour to your brand colour.
- Swap the display font (all styles use free Google fonts:
  Fraunces, Manrope, Archivo, Space Mono).
- Keep text readable: body text should stay at least 4.5:1
  contrast against its background — all ten stock styles pass.

## Everyday tasks

| Task | How |
|---|---|
| Add a link | CMS → Links → **+** → fill Label, URL, Note → set Sort |
| Reorder links | Edit the **Sort** numbers (1 shows first) |
| Feature a link | Turn on **Highlight** — it renders in the accent fill |
| Change your photo | CMS → Profile → **Avatar Image** (or clear it to use initials) |
| Change socials | Select the Profile Card → edit each Social label + link in the properties panel |
| Remove the footer badge | Select it on your home page → Delete. No hard feelings. |
| Custom domain | Site Settings → Site Domains (a Framer plan feature) |

## The ten styles

| Style | Background | Accent | Type | The full version |
|---|---|---|---|---|
| Nocturne | `#1C1412` espresso | `#C98A4B` copper | Fraunces + Manrope | **Nocturne** — the supper-club site template |
| Vermilion | `#F8F3EC` paper | `#B3401E` vermilion | Fraunces + Manrope | **Vermilion Folio** — the editorial portfolio |
| Crumb | `#FAF5EC` cream | `#9C4415` burnt crust | Fraunces + Manrope | **Crumb Culture** — the bakery/café template |
| Ledger | `#FAF7F1` paper | `#1B5E43` ledger green | Fraunces + Manrope | **Wagesmith** — payroll & SaaS, done warmly |
| Brutalist | `#FFFFFF` white | `#FFD02E` signal yellow | Archivo + Space Mono | From the original Astro link-in-bio theme |
| Dev | `#0B0E14` terminal black | `#4ADE80` terminal green | Space Mono | From the original Astro theme — the developer look |
| Glassy | `#0F172A` deep slate + aurora gradient | `#7DD3FC` sky | Fraunces + Manrope | From the original Astro theme — glass over a night city |
| Pastel | watercolor wash (peach → blush → lavender) | `#C2542F` terracotta | Fraunces + Manrope | From the original Astro theme — the watercolor look |
| Resume | `#F1F5F9` slate tint | `#1E40AF` professional blue | Archivo + Manrope | From the original Astro theme — the CV look |
| Retro | `#07070D` black + grid | `#22D3EE` cyan / `#FF5DA2` pink highlight | Archivo + Space Mono | From the original Astro theme — synthwave grid |

## Fine print

Waymark is free and provided **as-is, without support** — this
guide is the support. If a style made you smile and you later need
a full website, the paid templates in the table above are the same
design languages, grown up.
