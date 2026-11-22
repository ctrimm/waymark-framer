# Waymark — CMS schema

Two collections. **All ten style pages bind to these same two
collections** — that is the whole switching trick: content is edited
once, every style shows it, and the buyer previews all ten looks
with their real content before choosing.

## Profile (exactly 1 item)

| Field | Type | Notes |
|---|---|---|
| Name | Title | e.g. "June Calloway" |
| Role | Text | One line under the name |
| Location | Text | Optional; shown small |
| Bio | Text | 1–2 sentences |
| Avatar Image | Image | Optional — falls back to initials |
| Avatar Initials | Text | 1–2 characters, e.g. "JC" |

## Links

| Field | Type | Notes |
|---|---|---|
| Label | Title | The button text |
| URL | Link | Full URL or mailto: |
| Note | Text | Small line under the label (optional) |
| Highlight | Boolean | Renders the accent-filled variant |
| Sort | Number | Display order (collection sorted ascending) |

There is no Email field. Your email address lives in two places,
both edited directly: the **"Say hello" row in Links** (its URL is a
`mailto:` link) and the **Email social button** on the Profile Card
component (its link property is a `mailto:` link). An earlier draft
had a Profile → Email field, but nothing was bound to it, so it was
removed (2026-11-21) rather than ship an unused field.

Socials are NOT a collection — they are four fixed buttons on the
Profile Card component with editable link + label properties
(Instagram, YouTube, Pinterest, Email in the demo). Simpler for a
one-page template, and the guide explains how to relabel them.
