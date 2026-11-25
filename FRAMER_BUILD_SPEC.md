# Waymark — Framer Build Spec

Build this in Framer exactly as specified, then work the
SUBMISSION_CHECKLIST. Estimated build time: **60–75 minutes** (the
components do the heavy lifting — ten pages assemble from three
components).

**The product in one line:** a free link-in-bio template with ten
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

### Profile Card — 10 variants (Style: Nocturne / Vermilion / Crumb / Ledger / Brutalist / Dev / Glassy / Pastel / Resume / Retro)

One vertical stack, centred: Avatar (CMS image, initials fallback),
Name (H1), Role, Location (small caps), Bio, Socials Row (nested
component). All text bound to the **Profile** collection's single
item. Per-variant styling per the token table in §3.

### Link Button — 10 variants × Highlight on/off (20 states)

Full-width row bound to the **Links** collection (used inside a CMS
list, sorted by Sort ascending): Label (semibold), Note (small,
muted), arrow "→" at right. Highlight ON = accent fill + on-accent
text. Hover: translateY(-1px) + border/accent deepens (skip on
Brutalist — hover swaps shadow from 4px to 6px offset).

### Socials Row — 10 variants

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

All text/background pairs verified ≥ 4.5:1 across all ten styles
(worst case: Pastel accent on white, 4.56:1). Do not introduce
new pairs without checking.

The five originals (riffs of the Astro theme's looks, DECISION_LOG D6):

| Token | Dev | Glassy | Pastel | Resume | Retro |
|---|---|---|---|---|---|
| Page BG | `#0B0E14` | `#0F172A` + aurora gradient (violet top-left, sky right) | watercolor wash gradient `#FDEEE3` → `#FBE7EE` → `#EFE9FB` | `#F1F5F9` | `#07070D` + 28px grid lines, white 5% |
| Surface | `#131A24` | white 9% + blur 6px | `#FFFFFF` | `#FFFFFF` | `#101018` |
| Text | `#E6EDF3` | `#FFFFFF` | `#473A32` | `#17222E` | `#EDEDF2` |
| Muted | `#8B98A9` | `#C3CAD9` | `#755C4C` | `#5B6B7B` | `#9D9DB0` |
| Accent | `#4ADE80` | `#7DD3FC` | `#C2542F` | `#1E40AF` | `#22D3EE` (highlight fill: `#FF5DA2`) |
| On-accent | `#0B0E14` | `#0F172A` | `#FFFFFF` | `#FFFFFF` | `#0A0A0F` |
| Border | `#26303E` | white 25% | `#C2542F` 25% | `#D9DEE5` | `#26263A` |
| Radius | 6px | 18px | 24px | 3px | 8px |
| Shadow | none | none | soft terracotta | none | none |
| Name font | Space Mono 700 | Fraunces 700 | Fraunces 700 | Archivo 700 | Archivo 800 upper |
| UI font | Space Mono | Manrope | Manrope | Manrope | Space Mono |
| Signature | role line prefixed `//` in accent; square-ish avatar (10px radius) | frosted cards (surface blur is required, not optional) | the wash is the identity — never a flat BG | role in accent small caps; hairline rows, no shadows | avatar ring in pink `#FF5DA2`, initials in cyan; highlight button is pink, not cyan |

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
| Dev | `/dev` | Same, Dev variants |
| Glassy | `/glassy` | Same, Glassy variants |
| Pastel | `/pastel` | Same, Pastel variants |
| Resume | `/resume` | Same, Resume variants |
| Retro | `/retro` | Same, Retro variants |
| 404 | custom | "This link wandered off." + button to home, Ledger styling |

Set **Nocturne** as the home page (`/`) for the listing preview —
it's the most striking at thumbnail size. Buyers re-set it per
Method 1.

## 5. Interactions & polish

- Page load: links stagger in (fade + 8px rise, 40ms steps) on all
  styles. Keep it subtle; no other motion.
- Every button is a real link to a real, loading destination
  (stable platform homepages — Cargo, INPRNT, Society6, Substack,
  Cal.com, Vimeo, Instagram, YouTube, Pinterest); "Say hello" and the
  Email social are a working mailto:. No example.com placeholders
  (moderation pass, 2026-11-23).
- Favicon: a simple signpost glyph — draw with two rotated frames
  on a square, accent yellow on black works across styles.
- **Alt text:** the Profile avatar image carries alt text
  ("[Name]'s photo"); the initials fallback is decorative text,
  no alt needed. Any image a buyer adds follows the same rule.
- **Per-page title + description:** set in Page Settings for all
  ten style pages, the Start here page, and the 404 — Framer's
  accessibility guidance asks for it on every page, not just home.
- No Framer **Layout** on purpose: every page is the same three
  components in one column, so a Layout layer would add structure
  without saving a single edit. (Best practice says "where
  appropriate" — here it isn't.)
- Site title: "Waymark — link in bio"; each style page's SEO title
  "Your name — links" placeholder via CMS binding where Framer
  allows, else static "June Calloway — links".

## 6. What NOT to build

- No CMS collection pages (single-page template).
- No code components, no analytics embeds, no cookie anything.
- No eleventh style. The original Astro theme's Modern (its
  default look) is the one variant not ported — it was the
  generic baseline, not a look. (DECISION_LOG D2, D6.)
