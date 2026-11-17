# Waymark — CMS schema

Two collections. **All five style pages bind to these same two
collections** — that is the whole switching trick: content is edited
once, every style shows it, and the buyer previews all five looks
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
| Email | Text | Used by the "Say hello" link + socials row |

## Links

| Field | Type | Notes |
|---|---|---|
| Label | Title | The button text |
| URL | Link | Full URL or mailto: |
| Note | Text | Small line under the label (optional) |
| Highlight | Boolean | Renders the accent-filled variant |
| Sort | Number | Display order (collection sorted ascending) |

Socials are NOT a collection — they are four fixed buttons on the
Profile Card component with editable link + label properties
(Instagram, YouTube, Pinterest, Email in the demo). Simpler for a
one-page template, and the guide explains how to relabel them.
