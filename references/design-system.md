# Design system — Cinematic Precision

## Art-direction architecture
Define a product-specific design thesis before tokens:
1. Personality in 3 concrete adjectives (e.g. precise, humane, exploratory).
2. Audience expectation, emotional outcome, and primary action.
3. An original, domain-specific visual motif (e.g. research networks as carefully mapped relationships, not generic particle blobs).
4. One framing rule (e.g. editorial asymmetry), one image rule (e.g. natural directional light), one interaction rule (e.g. progressive reveal only at milestones).
5. What this project deliberately refuses to look like.

Separate *stable identity* (precision, art direction, intentional movement, strong hierarchy) from *variable expression* (palette, imagery, typeface, density, animation scale).

## Tokens and type
Build semantic roles: `--background`, `--surface`, `--surface-raised`, `--foreground`, `--muted`, `--border`, `--accent`, `--accent-foreground`, `--focus-ring`, `--danger`, `--success`. Define light and dark themes intentionally rather than naive inversion. Verify contrast on actual surfaces, including imagery overlays and disabled states; do not use muted text for critical labels.

Suggested *starting* palette, never a required brand identity:
- Obsidian #101114, graphite #292C31, ivory #F0EEE8, steel #9299A4.
- Optional electric blue #567CFF for digital or amber #C17C48 for warmth; choose project-specific accents.
- Neutral light mode: near-white background and near-black readable type with reduced border noise.

Define a responsive type scale with CSS `clamp()` and readable widths. Suggested intent:
- Display: 48–112 CSS px where space supports it, tighter leading and intentional wrapping.
- H1 40–72; H2 30–52; H3 22–34; body 16–18; small 13–15 (avoid tiny functional UI).
- Body line-height ~1.45–1.7; displays ~0.95–1.12; labels based on font metrics.
- Body measure approximately 55–75 characters for prose; shorter for marketing support copy.
- Use localized fonts with genuine support for Kurdish Sorani, Arabic and Latin where applicable; evaluate font shaping, bidi and numeral styles. Do not assume a Latin font covers Arabic script.
- Use real font availability/licensing and font-display decisions; avoid stacking 4 novelty fonts.

## Layout grammar
- Use an underlying 12-column or simpler coherent grid with measured gutters; break it deliberately for art direction.
- Content max-width commonly 1120–1440 CSS px, with varied editorial text widths; adjust to product density and display size.
- Vertical rhythm can use 4/8-based tokens, but prioritize optical relationships.
- Let sections differ in composition (narrative, image essay, product demonstration, proof, CTA) instead of repeated center-aligned 3-card modules.
- Responsive: stack or reorder according to reading sequence, not mechanical shrinking. On touch devices avoid hover-only controls. At 200% zoom content must reflow without horizontal loss.
- Grids: ensure consistent edges; make asymmetry legible via aligned anchor lines. An off-grid element needs a compositional reason.

## Image direction
Create an image brief for each asset: subject, source/rights, composition, focal point, shot scale, direction of light, tonal range, mobile crop, text-safe region, and performance format. Images should be relevant evidence or storytelling, not arbitrary placeholders. Avoid fake before/after claims, fictional medical credentials, and invented testimonials. Use real client photography where available.

Use realistic image treatment: restrained grades, no forced teal-orange everywhere, balanced blacks, highlight detail, consistent white balance, natural light/material relationships. Prefer AVIF/WebP where supported, responsive `srcset` / `sizes`, explicit dimensions, sensible `object-position` and lazy loading for offscreen media. Ensure meaningful alt text and decorative blank alt when applicable.

## Material & shape
Pick one dominant surface language: crisp editorial, warm tactile, translucent layered (only where legible), architectural panels, etc. Apply shadow, translucency, texture and blur sparingly. Avoid default rounded-3xl cards, glowing borders, ubiquitous gradient text, faux-3D icons and hero dashboards unless intrinsically relevant. Shape repetition should convey function.

## UI pattern constraints
- Primary CTA must be unmissable and descriptive.
- Clear focus, hover, active, loading, disabled, error and success states.
- Skeleton loaders only for genuinely awaited content; avoid gratuitous spinners and shimmer.
- Avoid fake browser chrome or mock device frames when a direct product view would be clearer.
- No fake client logos, reviews, numbers or results.
