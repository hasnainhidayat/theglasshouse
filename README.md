# The Glasshouse — Website Package

## What's inside
- `index.html` — the complete, self-contained website (HTML + CSS + JS in one file, no build step, no dependencies to install).

## How to use it
1. Unzip the folder.
2. Double-click `index.html` to preview it in any browser, or upload it to any web host (Netlify, Vercel, GitHub Pages, cPanel, etc.) as your homepage.
3. That's it — no npm install, no build tools required. Fonts (Cormorant Garamond, Manrope) load from Google Fonts via CDN, so an internet connection is needed for those to render with the correct typefaces (the site falls back to system fonts gracefully offline).

## Photos — action needed
Every photo area in the file is currently an elegant navy/gold placeholder panel (a `<div class="ph">`), NOT a real photo — this avoids using any stock or scraped images that aren't actually yours. To finish the site:

1. Search your `index.html` for `class="ph"` — each one marks a spot meant for a real photo, and most carry a `data-caption="..."` telling you what should go there (e.g. "Replace with exterior photo of The Glasshouse").
2. Replace each `<div class="ph ...">...</div>` with:
   ```html
   <div class="ph" style="background:url('images/your-photo.jpg') center/cover;"></div>
   ```
   or swap in a plain `<img src="images/your-photo.jpg" alt="...">` and adjust the CSS class as needed.
3. Recommended shots to gather: exterior (day + night), main hall/interior, table/reception setup, a wedding in progress, close-up décor/detail shots, and a landscaped-grounds shot.

## Easy edits
- **Contact details / phone / email / address**: search for `+92 300 555 0199`, `hello@theglasshouse.pk`, and `DHA Phase 6` and replace throughout.
- **Colors**: all defined once at the top of the `<style>` block under `:root` (`--navy`, `--gold`, `--ivory`, etc.) — change them there and the whole site updates.
- **Copy/text**: every section is plain, readable HTML — edit directly.
- **Availability form**: currently shows a "Thank You" confirmation on submit but doesn't send data anywhere yet. To actually receive enquiries, connect the `<form id="availForm">` to a form backend (e.g. Formspree, Netlify Forms, or your own endpoint) — happy to wire this up if you tell me which service you'd like to use.
- **Map**: the placeholder near Contact can be swapped for a real Google Maps embed (`<iframe>`) once you share the exact address/pin.

## Notes
- Fully responsive (mobile sticky enquiry bar, collapsing nav, single-column layouts on small screens).
- Gallery includes working filter tabs and a full-screen lightbox (click any image, use arrow keys or on-screen arrows to navigate).
- No pricing appears anywhere, per the brief — all CTAs point to "Check Availability" / "Request Details" style actions.
