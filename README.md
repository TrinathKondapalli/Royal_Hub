# Royal Hub Mini Screen – Website

One-page website for Royal Hub Mini Screen, a private theatre in Ramachandrapuram.
Plain HTML, CSS and JavaScript. No build step, no packages.

## Files
- `index.html` – the whole site (styles and script are inside)
- `assets/` – photos and logos

## Change the business details (one place)
Open `index.html`, find `const CONFIG` near the bottom, and edit:
- `whatsapp` – country code + number, digits only, e.g. `919876543210`
- `phone` – e.g. `+919876543210`
- `phoneText` – how the number is shown, e.g. `+91 98765 43210`
- `address`, `hours`, `mapsUrl`, `instagram`

Every WhatsApp button, Call button, map link and phone text updates from this.
Also update the same number in the `tel:` links and the JSON-LD block in `<head>` (search for `9000000000`).

## Replace the photos
The current photos are AI-generated placeholders. Replace files in `assets/` with real photos,
keeping the same file names (JPG, about 1200 px wide, under 200 KB each).

## Deploy (GitHub + Vercel)
1. Open this folder in Antigravity.
2. `git init` → `git add .` → `git commit -m "Royal Hub website"`.
3. Create a GitHub repo and push.
4. In Vercel: Add New → Project → import the repo → Framework preset "Other" → Deploy.
5. Later: add your custom domain in Vercel → Project → Settings → Domains.

## What the page does
- Every "Book / Check Availability" button opens WhatsApp with a pre-filled message (date, time, guests, package).
- Mobile: menu, swipe carousels, sticky WhatsApp/Call bar after the hero.
- Animations: hero entrance, scroll reveals, film-reel booking steps, curtains opening on the final section.
  All animations switch off when the visitor's phone has "Reduce motion" on.
