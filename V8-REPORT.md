# Crestpane V8 — colour & visual refinement report

Brand name, logo, palette values, content, structure and static architecture are unchanged. No new colours, no new dependencies, no fake features. Changes live in one block at the end of `_generator/css.py` (section "V8"), rebuilt with `python3 build.py`.

## What was checked
- All 52 pages x light + dark: 0 JavaScript errors, 0 broken images.
- All 52 pages at 320, 360, 390, 430, 600, 768, 900, 1024, 1280, 1440, 1920 px: 0 horizontal overflow (was 16 failures at 320 px).
- Automated WCAG AA text-contrast scan of every text node, both themes.
- Screenshot review: homepage (light, dark, 390 px), pricing, philosophy section.

## Changes
1. **Contrast (AA):** small accent text (project/blog categories, service and industry numbers) now uses the deep brand orange `#B0430A` on light surfaces (was `#E0540A`, 3.86:1). Footer copyright uses the lighter muted token (was 4.27:1). Featured industry card description uses the stronger text token (was 3.83:1). Nav hover uses the deep accent.
2. **Small-phone layout:** hero trust bar and split sections no longer force a 2 px overflow at 320 px.
3. **Section boundaries:** hairline borders where two light tones meet (cream, peach).
4. **Cards and images:** one hover language (3 px lift, warm border, soft shadow, slow 2.5% image zoom), hover-capable devices only; disabled under reduced motion.
5. **Design-philosophy dark section:** empty right half now carries a quiet charcoal ring motif (palette tokens only).
6. **Pricing:** equal-height cards with the CTA pinned to the bottom so buttons align across packages.
7. **Type rhythm:** tighter heading tracking, balanced/pretty text wrapping.

## Colour map vs your brief
Announcement bar black, header ivory, hero peach/ivory, services ivory + white cards, portfolio ivory/cream frames, process peach with ivory cards, pricing cream + white cards, final CTA and footer black, dark theme tokens as specified. This was already in place from v5; V8 verified it.

## Remaining limitations (honest)
- **No testimonials section exists**, and none was invented (all projects are labelled concept work). Add real ones when available and use the black/charcoal dark section.
- Hero device mockup uses raster/illustration greys; the decorative "forward." in the mockup is `#F36B21` on ivory (2.83:1, aria-hidden, not readable content).
- Not tested on real devices or with a screen reader. The contrast scanner cannot resolve semi-transparent `color-mix` header backgrounds, so it reports a false positive on nav items; they read black on ivory in screenshots.
- I did not individually eyeball all 52 pages at all 11 widths; checks were automated plus the screenshots listed above. Page-by-page visual sign-off is still recommended before launch.
- No images were replaced in this pass.
