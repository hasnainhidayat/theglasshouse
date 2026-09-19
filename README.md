# The Glasshouse — Website Package

## What's inside
- `index.html` — the complete website (HTML + CSS + JS in one file, no build step).
- `images/` — an empty folder, pre-wired to the site. Drop your photos in here using the exact filenames below and they'll appear automatically — no code editing required.

## How to use it
1. Unzip the folder, keeping `index.html` and `images/` next to each other.
2. Add your photos into `images/` using the filenames in the table below (jpg or png both work — just keep the same filename, or update the `src=""` in `index.html` if you'd rather use your own names).
3. Double-click `index.html` to preview in a browser, or upload the whole folder to any web host (Netlify, Vercel, GitHub Pages, cPanel, etc.).

Until a given file is added, that spot shows an elegant navy/gold placeholder panel instead of a broken image — so the site always looks finished, even before every photo is in.

## Image checklist

| Section                     | Filename (put inside `images/`)      | Suggested shape        |
|------------------------------|---------------------------------------|-------------------------|
| Hero (top of page)            | `hero-exterior.jpg`                   | Wide, landscape (1920×1080+) |
| Welcome section                | `welcome-interior.jpg`                | Portrait (4:5)          |
| Event card — Weddings           | `event-wedding.jpg`                   | Portrait (3:4)          |
| Event card — Wedding Receptions | `event-reception.jpg`                 | Portrait (3:4)          |
| Event card — Mehndi/Engagements | `event-mehndi.jpg`                    | Portrait (3:4)          |
| Event card — Corporate Events   | `event-corporate.jpg`                 | Portrait (3:4)          |
| Event card — Private Celebrations| `event-private.jpg`                  | Portrait (3:4)          |
| Venue showcase — main photo    | `venue-exterior-wide.jpg`             | Very wide (16:8)         |
| Architecture feature (night)   | `architecture-night.jpg`              | Wide, landscape          |
| Gallery — Architecture (×3)    | `gallery-architecture-1.jpg`, `-2.jpg`, `-3.jpg` | Mixed          |
| Gallery — Interiors (×2)       | `gallery-interiors-1.jpg`, `-2.jpg`   | Mixed                    |
| Gallery — Celebrations (×2)    | `gallery-celebrations-1.jpg`, `-2.jpg`| Mixed                    |
| Gallery — Weddings (×3)        | `gallery-weddings-1.jpg`, `-2.jpg`, `-3.jpg` | Mixed             |
| Gallery — Details (×2)         | `gallery-details-1.jpg`, `-2.jpg`     | Mixed                    |
| Instagram grid (×6)            | `insta-1.jpg` through `insta-6.jpg`   | Square (1:1)             |
| Contact — map                  | `map.jpg`                             | Very wide (21:8) — or see note below |
| Final call-to-action           | `final-cta-evening.jpg`               | Wide, landscape          |

Tip: search `images/` inside `index.html` if you ever want to see exactly where each file is referenced, or to rename one.

### Map — better option
Instead of a static `map.jpg`, you can embed a live, interactive Google Map. In `index.html`, find the `map-box` div near the Contact section and replace it with:
```html
<iframe src="https://www.google.com/maps/embed?pb=YOUR_EMBED_CODE" style="width:100%;aspect-ratio:21/8;border:0;" loading="lazy"></iframe>
```
Get `YOUR_EMBED_CODE` from Google Maps → Share → Embed a map, for your actual address.

## Other easy edits
- **Contact details**: search for `+92 300 555 0199`, `hello@theglasshouse.pk`, and `DHA Phase 6` and replace throughout.
- **Colors**: defined once at the top of the `<style>` block under `:root` (`--navy`, `--gold`, `--ivory`, etc.) — change them there and the whole site updates.
- **Copy/text**: every section is plain, readable HTML — edit directly.
- **Availability form**: currently shows a "Thank You" confirmation on submit but doesn't send data anywhere yet. To actually receive enquiries, connect `<form id="availForm">` to a form backend (e.g. Formspree, Netlify Forms) — happy to wire this up if you tell me which service you'd like to use.

## Notes
- Fully responsive (mobile sticky enquiry bar, collapsing nav, single-column layouts on small screens).
- Gallery has working filter tabs and a full-screen lightbox (click any image; use arrow keys or on-screen arrows to navigate).
- No pricing appears anywhere, per the brief.
