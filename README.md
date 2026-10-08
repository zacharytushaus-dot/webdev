# Godel Landing Page — Handoff Package

## What This Is

This package contains the final mockup for the redesigned Godel Terminal landing page. It's a single self-contained HTML file with all referenced assets in `assets/`.

## How to Use

1. **Open `godel-quartr-style.html` directly in a browser** — it works standalone, no server required.
2. **Feed the HTML to your LLM/frontend pipeline** — the file contains all markup, inline CSS, and inline JavaScript. Asset paths are relative (`assets/...`).

## File Structure

```
godel-landing-handoff/
├── godel-quartr-style.html    # Main landing page (all CSS/JS inline)
├── assets/
│   ├── adobe-logo.png          # Red Adobe logo (notification thumbnails)
│   ├── godel-app-icon.png      # Godel app icon (notification squircles)
│   ├── thomas-george-color.jpg # Testimonial headshot
│   ├── herobannerv3.mp4        # Hero banner video
│   └── DES-banner.mp4          # DES product demo video
└── README.md                   # This file
```

## Sections (top to bottom)

1. **Hero** — Full-viewport dark hero with animated banner video and CTA
2. **Stats Strip** — 4-column single-row metric strip (Sub-sec latency, 100% filings, >1B indexed, 18:1 seat ratio) with hairline dividers and source footnote
3. **Testimonial** — Thomas George (Grizzle / DARP ETF) quote with headshot
4. **Mobile Showcase** — "Stay ahead, from anywhere" — iPhone lock screen mockup with 3 post-market ADBE notifications (Price Alert, Chat, Earnings). Phone is cropped flush at the section's bottom border.
5. **Pricing / CTA** — Seat pricing table and final call-to-action
6. **Footer**

## Key Design Decisions

- **Brand spelling:** "Godel" — never with an umlaut.
- **Dark theme:** Pure black `#000000` page background, `#12151e` for the mobile section contrast layer.
- **Phone mockup:** 320×455px, Dynamic Island with camera lens, status bar (4:31 / 5G / signal / battery), iOS frosted glass notification cards. No home indicator or bottom hardware — flush crop.
- **Notification narrative:** Post-market ADBE earnings sequence at 4:31 PM — Price drop alert → Desk chat catalyst → Earnings summary.
- **Typography:** Inter / SF Pro Display system stack.

## Notes for Frontend Dev

- All CSS is inline in `<style>` tags within the HTML `<head>`.
- SVG icons (status bar, star ratings, arrows) are inline SVG — no icon library dependency.
- The phone mockup is pure HTML/CSS — no images of a phone, it's built with divs and gradients.
- Video assets are large-ish (8MB total). Consider compressing or serving from CDN for production.
- The page is not responsive-optimized for mobile/tablet viewports yet — designed at 1440px desktop width.
