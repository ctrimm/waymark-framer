# Waymark — Framer Build Spec

Build this in Framer exactly as specified, then work the
SUBMISSION_CHECKLIST. Estimated build time: **45–60 minutes** (the
components do the heavy lifting — five pages assemble from three
components).

**The product in one line:** a free link-in-bio template with five
switchable styles, where all content lives in CMS so the buyer
previews every style with their own links before choosing.

---

## 1. Project setup

- New project, **blank**, Desktop breakpoint first (designs are
  phone-first: the page column is **430px max**, centred, with the
  style's background filling the whole viewport).
- Fonts (Google, via Framer's font picker): **Fraunces** (600, 700
  + italic), **Manrope** (400–800), **Archivo** (700, 800),
  **Space Mono** (400, 700).
- Create the two CMS collections from `cms/SCHEMA.md`; import
  `cms/profile.csv` (1 item) and `cms/links.csv` (7 items).

## 2. Components (build these first)

### Profile Card — 5 variants (Style: Nocturne / Vermilion / Crumb / Ledger / Brutalist)

One vertical stack, centred: Avatar (CMS image, initials fallback),
Name (H1), Role, Location (small caps), Bio, Socials Row (nested
component). All text bound to the **Profile** collection's single
item. Per-variant styling per the token table in §3.

### Link Button — 5 variants × Highlight on/off (10 states)

Full-width row bound to the **Links** collection (used inside a CMS
list, sorted by Sort ascending): Label (semibold), Note (small,
muted), arrow "→" at right. Highlight ON = accent fill + on-accent
text. Hover: translateY(-1px) + border/accent deepens (skip on
Brutalist — hover swaps shadow from 4px to 6px offset).

### Socials Row — 5 variants

Four text-labelled pill buttons (Instagram / YouTube / Pinterest /
Email in the demo) with editable link + label properties. Text
labels, not icon fonts — they must survive a remix intact.

### Footer Badge (single component, no variants)

"Made with Waymark — free Framer template" small centred line,
linking to the Marketplace listing. Present on every style page;
the guide tells buyers they may delete it.

## 3. Style tokens

| Token | Nocturne | Vermilion | Crumb | Ledger | Brutalist |
|---|---|---|---|---|---|
| Page BG | `#1C1412` | `#F8F3EC` | `#FAF5EC` | `#FAF7F1` | `#FFFFFF` |
| Surface | `#2A1D18` | `#FFFDF8` | `#FFFDF6` | `#FFFFFF` | `#FFFFFF` |
| Text | `#F1E8D8` | `#201713` | `#2B1D11` | `#171512` | `#111111` |
| Muted | `#A08B6D` | `#6E5D4F` | `#7A5F45` | `#5F6A61` | `#555555` |
| Accent | `#C98A4B` | `#B3401E` | `#9C4415` | `#1B5E43` | `#FFD02E` |
| On-accent | `#1C1412` | `#F8F3EC` | `#FAF5EC` | `#FAF7F1` | `#111111` |
| Border | `#C98A4B` 40% | `#201713` 18% | `#9C4415` 30% | `#1B5E43` 25% | `#111111` 2px |
| Radius | 14px | 4px | 20px | 10px | 0 |
| Shadow | none | none | soft warm | none | 4px 4px 0 `#111` |
| Name font | Fraunces 700 | Fraunces 700 italic | Fraunces 700 | Fraunces 700 | Archivo 800 upper |
| UI font | Manrope | Manrope | Manrope | Manrope | Space Mono |
| Signature | copper ring avatar, arch top on highlight button | numbered links (01–07, Space Mono… use Manrope 700) | pill buttons, soft shadow | small-caps labels, ruled top border on card | hard shadows, uppercase labels |

All text/background pairs verified ≥ 4.5:1 (worst case: Vermilion
accent on paper, 5.18:1). Do not introduce new pairs without
checking.

Create matching **Color Styles** per style (`Nocturne / BG`, …) and
apply them — Method 3 in the guide depends on styles existing, not
raw hex on frames.

## 4. Pages

| Page | Route | Contents |
|---|---|---|
| Start here | `/start` | The SWITCHING_GUIDE, laid out as a designed page: how it works, the 3 methods, task table, style table. NOT set as home; linked from every style page's footer ("New here? Start here") |
| Nocturne | `/nocturne` | Profile Card (Nocturne) + CMS list of Link Buttons (Nocturne) + Footer Badge |
| Vermilion | `/vermilion` | Same, Vermilion variants |
| Crumb | `/crumb` | Same, Crumb variants |
| Ledger | `/ledger` | Same, Ledger variants |
| Brutalist | `/brutalist` | Same, Brutalist variants |
| 404 | custom | "This link wandered off." + button to home, Ledger styling |

Set **Nocturne** as the home page (`/`) for the listing preview —
it's the most striking at thumbnail size. Buyers re-set it per
Method 1.

## 5. Interactions & polish

- Page load: links stagger in (fade + 8px rise, 40ms steps) on all
  styles. Keep it subtle; no other motion.
- Every button is a real link (demo URLs point to example.com
  paths; "Say hello" is a real mailto:).
- Favicon: a simple signpost glyph — draw with two rotated frames
  on a square, accent yellow on black works across styles.
- Site title: "Waymark — link in bio"; each style page's SEO title
  "Your name — links" placeholder via CMS binding where Framer
  allows, else static "June Calloway — links".

## 6. What NOT to build

- No CMS collection pages (single-page template).
- No code components, no analytics embeds, no cookie anything.
- No sixth style. The original Astro theme's Dev / Glassy / Pastel
  / Resume / Retro looks are deliberately out (DECISION_LOG D2).
