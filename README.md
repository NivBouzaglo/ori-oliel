# אורי אוליאל — ספר גברים, אשדוד

Single-file static site for a men's barbershop in Ashdod, Israel. Hebrew/RTL, dark + brass visual identity, real photos sourced from the client's Instagram.

**Live:** https://claude.ai/artifact/VkA9S472QHPyStrHd5og8D
**Links page (same file, `#links`):** https://claude.ai/artifact/VkA9S472QHPyStrHd5og8D#links

## Features

- Single `index.html` — no build step, no dependencies beyond Google Fonts
- Hero, services/pricing, gallery, about, Google reviews, hours (live open/closed status), location
- In-page Linktree-style view at `#links` — same file, same domain, no separate deploy
- Custom scissors cursor that "snips" as you scroll
- Scroll-reveal animations, live stat count-up, hero parallax
- Accessibility widget: text scaling, high contrast, grayscale, forced underlines, reduced motion, cursor toggle — preferences persist via `localStorage`

## Structure

```
index.html      — the entire site (both views)
images/         — gallery, hero, and avatar photos
```

## Deploying elsewhere

This is a plain static file — drop `index.html` and `images/` onto any static host (GitHub Pages, Vercel, Netlify, S3, etc.) and it works as-is, including the `#links` view, which needs no server-side routing.

Hosted on Cloudflare Pages: https://ori-oliel.com
