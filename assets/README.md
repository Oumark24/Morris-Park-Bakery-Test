# Morris Park Bake Shop — Asset Handoff Guide

This static site uses a CSS-only bakery-box visual system until approved business photography and a clean logo are supplied. It intentionally contains no stock food photography, generated food images, remote placeholder images, or encoded image data.

## Recommended local assets

Place approved files in the following folders and update the nearby `<!-- ASSET: ... -->` comments in `index.html`.

| Suggested file | Use | Recommended treatment |
|---|---|---|
| `logo/morris-park-bake-shop-logo.svg` | Header and optional favicon source | A clean, approved vector or transparent PNG; do not use a raw screenshot. |
| `hero/morris-park-storefront.webp` | Optional storefront/hero image | Real approved storefront photography, landscape crop, roughly 1600px wide, compressed WebP. |
| `gallery/cake-display.webp` | Optional below-fold custom-cake image | Real approved photography, responsive WebP, lazy-loaded. |
| `gallery/pastry-case.webp` | Optional below-fold pastry-case image | Real approved photography, responsive WebP, lazy-loaded. |
| `social/morris-park-social-preview.jpg` | Optional sharing card | Approved photo or graphic, 1200 × 630px JPG/PNG. |

Do not use base64-encoded images. Do not use unapproved food photography, random stock images, or AI-generated food imagery as a substitute for approved business assets.

## Premium motion-hero visual treatment

| File | Purpose | Public-facing constraint |
|---|---|---|
| `visuals/hero-package-world.svg` | Local abstract mint, cream, crimson, and cocoa package-material study used with CSS dimensional planes in the homepage hero | This is non-documentary art direction only. Do not describe or present it as the shop, its packaging, food, staff, storefront, menu, inventory, or logo. It is not a factual business photograph. |

The homepage keeps a strong readability overlay and complete customer actions independent of this decorative material. Replace it only with owner-approved documentary imagery or an equally non-documentary local treatment.
