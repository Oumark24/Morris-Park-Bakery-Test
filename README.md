# Morris Park Bake Shop

A single-page website for **Morris Park Bake Shop**, a Bronx bakery at 1007 Morris Park Avenue that has been making custom cakes and Italian pastries since 1980. One static `index.html` with committed WebP photography, no framework and no build step, deployed to GitHub Pages.

**Live site:** https://oumark24.github.io/Morris-Park-Bakery-Test/

## What it does

- **Custom cake inquiry form** — collects event date, guest count, theme and description with native HTML validation (`checkValidity()` / `reportValidity()`), saves the draft to `sessionStorage`, and then tells the customer to call the shop for confirmation. There is no mail server behind it, so instead of silently dropping the submission the form is honest about the hand-off.
- **Delivery provider hand-off** — a provider picker for Uber Eats, Grubhub, Seamless and Postmates with committed SVG logos, because that's how this bakery actually takes orders.
- **Menu and product sections** — signature cakes, classic pastries, and a "small-batch favorites" section.
- **WebP photography with a mobile-specific hero** — a separate `pastry-hero-mobile-fast.webp` so phones don't download the desktop hero image.
- **Accessibility and motion** — 18 `aria-label`s across interactive controls, and every scroll/animation path checks `prefers-reduced-motion` before animating.

## Why it's built this way

Everything is static and hand-editable. The bakery's owner needs to change a price or a photo, not run a build. Since there's no backend, the two places a user might expect one — the cake form and delivery ordering — are handled by handing off to a phone call or a delivery platform rather than pretending a submission was received.

Images are pre-converted to WebP and committed, with a smaller mobile hero variant, so the page loads quickly on a phone without any image pipeline.

## Running it

```bash
git clone https://github.com/Oumark24/Morris-Park-Bakery-Test.git
cd Morris-Park-Bakery-Test
open index.html
```

## Deployment

`.github/workflows/static.yml` publishes the repository root to GitHub Pages on every push to `main`.

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | Entire site — markup, CSS, form validation and provider picker logic |
| `assets/photos/` | WebP product and storefront photography, including the mobile hero |
| `assets/providers/` | Uber Eats, Grubhub, Seamless and Postmates SVG logos |
| `assets/social/` | Storefront social-preview image |
| `.github/workflows/static.yml` | GitHub Pages deployment |
