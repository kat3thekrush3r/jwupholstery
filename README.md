# JW Upholstery — Website

A 5-page editorial-luxury site for Jason White's Tallahassee upholstery atelier.

## Pages

- `index.html` — Home (hero, services preview, before/after, process, CTA)
- `services.html` — Three services (Reupholstery, Restoration, Headboards & Cushions)
- `gallery.html` — Selected work, magazine-style layout
- `about.html` — Jason's story, three "quiet rules", workshop info
- `contact.html` — Phone-first contact card, hours, message form

## What's hard-coded that you'll want to swap

These all use placeholders — search & replace across all 5 HTML files:

| Find | Replace with |
|---|---|
| `(850) 555-1234` | Jason's actual shop number |
| `+18505551234` | Same number, in `tel:` / `sms:` format (no spaces/dashes) |
| `jason@jwupholstery.com` | His real email (set this up on Cloudflare Email Routing) |
| The Jason bio paragraphs in `about.html` | His actual story when you've talked to him |

## What's NOT wired up yet

**The contact form** currently just shows an alert. To make it work when deployed:

- **Easiest:** Use [Formspree](https://formspree.io) (free tier) — just paste your endpoint into the form's `action` attribute and remove the `onsubmit` handler.
- **If deploying on Vercel:** Use Vercel Forms or a serverless function.
- **If deploying on Netlify:** Add `netlify` attribute to the `<form>` tag and Netlify handles it automatically.

## Deploy

Drop this folder onto Vercel (drag-and-drop in the dashboard, or `vercel` CLI in the folder) and you're live. Domain `jwupholstery.com` is already on Cloudflare — point it at Vercel via DNS.

## Brand assets included

Full logo package in `assets/logos/`:
- `horizontal-black.svg` — nav logo
- `full-gold.svg` — footer logo
- `monogram-gold.svg` — hero watermark
- `favicon.svg`, `apple-touch.png` — browser tab / iOS home screen

Brand photos in `assets/photos/` — Jason's actual before/after work.

## Aesthetic notes

- **Type:** Playfair Display (display), Cinzel (small caps/eyebrows), Cormorant Garamond (italic accents), Inter Tight (body)
- **Colors:** Antique brass `#C8B88A`, Ink black `#1A1916`, Cream paper `#FAF6EC`
- **Style:** Editorial / atelier — generous whitespace, italic flourishes, magazine-style numbered sections (i. ii. iii.)

All defined as CSS variables in `styles.css` if you want to tune anything.
