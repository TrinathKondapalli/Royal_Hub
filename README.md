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
Then search the file for `9000000000` and replace it everywhere (WhatsApp links, `tel:` links and the JSON-LD block in `<head>`).

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
- Mobile: menu, swipeable add-ons strip, sticky WhatsApp/Call bar after the hero.
- Motion (the page plays like one private screening):
  - Intro: 3-2-1 film countdown on closed curtains, under 2 seconds, once per visit. Any tap, key or scroll skips it.
  - Hero: projector beam with drifting dust; the hall dims as you scroll away.
  - Occasions ("Now Showing"): a pinned screen shows the photo of the occasion you scroll to.
  - Packages: curtains slide in, tickets are dealt, prices count up, the ticket stub tears when you tap to book.
  - Add-ons sit on a film strip; gallery photos switch on like a screen and zoom open.
  - Final section: velvet curtains part as you scroll in.
- No libraries and no build step. Everything is in `index.html`.
- With "Reduce motion" on, or if JavaScript fails, the page is a calm, fully visible version and every booking link still works.
