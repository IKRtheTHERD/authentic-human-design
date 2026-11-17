# Production frontend engineering

## Repository-first execution
Inspect package manifests, routing, component hierarchy, styles and existing assets before choosing libraries. Preserve conventions, API contracts and CMS content. Show the smallest maintainable change set. Avoid introducing GSAP, Motion, Lenis or WebGL unless their use case is justified.

## Component architecture
- Use semantic HTML and compositional patterns; design tokens in CSS custom properties or existing theme system.
- Components should have clear responsibility, typed interfaces where supported, predictable states, and no fragile global selectors.
- Build accessible controls with native elements first. Dialogs/menus require keyboard behavior, focus management and appropriate semantics.
- Establish typography, container, surface, interactive and spacing primitives before proliferating page-specific components.
- In React/Next.js: distinguish server/client needs, minimize hydration, use image optimization and suspense responsibly; clean up animated effects.
- In Laravel/Blade/Livewire: preserve server validation and semantic forms, minimize JS entanglement, ensure dynamic updates are accessible and reversible.
- In Vue/Inertia: preserve lifecycle cleanup, route progress indication and focus after navigation.

## Responsive and localization
Test at representative widths: ~320/375 mobile, ~768 tablet, ~1280 laptop and ~1600 desktop; also content-driven intermediate sizes. Support dynamic text, longer translations, 200% zoom, text resizing, and mixed-direction text. Where Sorani/Arabic is used, set `lang` and `dir` appropriately; test bidirectional icons, tables, forms, numerals, font fallback and alignment. Do not merely mirror the entire design mechanically.

## Performance strategy
- Set a performance budget appropriate to hosting/device and measure rather than invent scores.
- Prevent layout shift with reserved media dimensions, stable font loading and predictable async elements.
- Prioritize main content and hero LCP media; defer below-the-fold media, animation bundles, maps, charts and 3D.
- Avoid heavy CSS `filter`, huge blurs, high-cost backdrops, constant scroll handlers; prefer observers and performant transforms.
- Review JS size, images, network requests, font weights, hydration boundaries and animation teardown.
- Target good real-world Web Vitals; diagnose LCP, CLS and INP with appropriate tools if available.

## Accessibility and robustness
Use WCAG 2.2 AA as a practical target (verify specifics relevant to the task): color contrast, non-text contrast, keyboard reachability, visible focus, labels and errors, headings, landmarks, meaningful alternative text, reduced-motion behavior, accessible authentication and form feedback. Ensure critical content is in DOM and accessible without animation; avoid focus loss on route/scene changes.

## Security and integrity
Never put secrets in client code. Sanitize/untrust external content as required by the framework; do not create dangerous HTML injection to reproduce an effect. Add dependency only with project consent/standards, assess maintenance and licensing. Do not fake backend success or invent testimonials, analytics, physician profiles or clinical certifications. No unrequested destructive rewrites.

## Verification commands
Use the repository's own existing scripts: install only when appropriate; run lint/typecheck/tests/build; check errors; capture browser screenshots and inspect visual quality if tooling exists. Do not report tests as passing if not run. If browser testing unavailable, report a concrete manual checklist rather than invented outcomes.
