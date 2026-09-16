# אורי אוליאל — ספר גברים, אשדוד

Single-file static site for a men's barbershop in Ashdod, Israel. Hebrew/RTL, dark + brass visual identity, real photos sourced from the client's Instagram.

**Live:** https://claude.ai/artifact/VkA9S472QHPyStrHd5og8D
**Links page (same file, `#links`):** https://claude.ai/artifact/VkA9S472QHPyStrHd5og8D#links

## Features

- Single `index.html` — no build step, no dependencies beyond Google Fonts
- Hero, services/pricing, gallery, about, Google reviews, hours (live open/closed status), location
- In-page Linktree-style view at `#links` — same file, same domain, no separate deploy
- Scroll-reveal animations, live stat count-up, hero parallax
- Accessibility widget: text scaling, high contrast, grayscale, forced underlines, reduced motion — preferences persist via `localStorage`

## Accessibility

Built and audited for WCAG 2.1 AA / Israeli standard ת"י 5568:

- Skip-to-content link, proper landmark regions (`header`/`nav`/`main`/`footer`), single always-present `<h1>`, no skipped heading levels
- All text/background color pairs verified ≥4.5:1 contrast (computed, not eyeballed)
- `lang="en"` on embedded Latin text so screen readers switch voice/pronunciation correctly
- Every link that opens a new tab announces that to screen readers
- All decorative icons are `aria-hidden`; the dynamic "open now / closed" status is an `aria-live` region
- The accessibility panel is properly `inert` and hidden from keyboard/AT when closed (not just visually hidden), returns focus correctly on open/close
- `forced-colors` (Windows High Contrast Mode) support for all custom controls
- Full `prefers-reduced-motion` support, plus a manual "stop animations" toggle
- Scroll-triggered reveal animations have a fail-safe timeout so content can never get stuck hidden
- Keyboard-operable throughout — no mouse-only interactions

## Structure

```
index.html      — the entire site (both views)
images/         — gallery, hero, and avatar photos
```

## Deploying elsewhere

This is a plain static file — drop `index.html` and `images/` onto any static host (GitHub Pages, Vercel, Netlify, S3, etc.) and it works as-is, including the `#links` view, which needs no server-side routing.

Hosted on Cloudflare Pages: https://ori-oliel.com
