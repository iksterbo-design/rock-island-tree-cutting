# Rock Island County Tree Cutting — Website

Single-file static site. No build step, no dependencies (Google Fonts is the only remote asset).

## Files
- `index.html` — the full website (self-contained HTML/CSS/JS)
- `logo.svg` — standalone logo asset (512×512), also inlined in the page + used as the favicon

## Open it locally
Double-click `index.html`, or from this directory:
```
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Put it online (get a public link)
Any static host works — the site is one folder of files:

1. **Netlify Drop** — https://app.netlify.com/drop — drag the whole `rockisland-tree` folder into the browser, get a live URL in ~10 seconds (free, may ask you to sign in).
2. **Cloudflare Pages** — upload the folder via dashboard (free).
3. **GitHub Pages** — push to a repo and enable Pages (free).
4. **Vercel / any shared hosting** — same idea: serve the folder.

## Before you go live — replace the placeholders
Search `index.html` for these and swap in real info:
- Phone: `(309) 555-0183` (appears in nav, hero, contact, footer — all as `tel:+13095550183` links too)
- Email: `hello@rockislandtreecutting.com`
- The three testimonials are **sample copy** (marked with initials) — replace with real customer reviews
- Footer license line: "Fully Licensed & Insured" → add your actual license number

## The contact form
The form is front-end only right now: it validates and shows a success message but does not send anywhere.
To make it actually email you, wire it to a free form backend (Formspree, Basin, Web3Forms) — paste your
endpoint into the `fetch` in the `<script>` at the bottom, or set the form's `action`.
