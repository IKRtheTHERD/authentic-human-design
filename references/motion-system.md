# Purposeful motion system

## Motion taxonomy
Every animation should serve at least one category:
- Orientation: show where the user is / what changed.
- Hierarchy: stage information reveal in the correct order.
- Causality: indicate interaction response, state change, or spatial continuity.
- Feedback: acknowledge a valid action, loading progress, validation or failure.
- Atmosphere: strengthen brand mood without delaying navigation or tasks.
Remove any motion without a clear answer.

## Default motion tokens (starting guidance, not hard laws)
- Micro feedback: ~100–180 ms; modest easing; never delay button interaction.
- Interface state transitions: ~160–280 ms.
- Section entrance: ~350–650 ms if the context merits it.
- Cinematic staged sequence: ~650–1200 ms only for special storytelling moments, skippable/interruptible.
- Stagger: usually ~30–90 ms across limited elements, avoiding long cascades.
- Distance: ~6–24 px for UI; ~24–64 px for expressive editorial reveals; never animate essential copy far from its natural reading position.
- Use opacity/transform composited paths when possible; avoid animating huge filters or layout-heavy properties on scroll.

## Motion choreography
1. List triggers (load, scroll, interaction, navigation) and user outcomes.
2. Establish priority: first content and primary action remain accessible without effects.
3. Assign motion to moments of meaning, not all DOM elements.
4. Use rhythmic contrast: stillness makes motion intentional. Do not animate every section in the same way.
5. Provide an equivalent immediate state for reduced motion, low power and JS failure.
6. Test repeated navigation, rapid scrolling, resizing, mobile touch and focus changes.

## Tool selection
- Native CSS: hover, focus, simple transitions, discreet reveal.
- Motion/Framer Motion: React component entrance/exit, state changes, shared layout transitions where justified.
- GSAP + ScrollTrigger: complex orchestration, scrub timelines, pinned narrative chapters, measured scroll-linked choreography.
- Lenis (optional): carefully integrated smooth scrolling only if it materially helps experience. Preserve browser/history anchor behavior, keyboard navigation, touch scrolling, accessibility, overscroll expectations, scroll restoration and GSAP synchronization. Never add it by default to dashboards, POS, forms, or content-heavy apps.
- 3D/WebGL (optional): only for a genuinely interactive subject or story with performance budgets and static fallback. Do not use for generic decorative floating blobs.

## Engineering safeguards
- Respect `@media (prefers-reduced-motion: reduce)` and disable large parallax, scroll-scrub, pinned scenes, and camera movement. Do not merely shorten durations if movement remains disorienting.
- Avoid animation gating readable content (`opacity:0`) permanently on animation failure.
- Initialize timelines after DOM readiness, clean up event handlers and ScrollTrigger instances, use GSAP context cleanup or framework equivalent.
- Use dynamic import/code splitting for heavy animation features when appropriate.
- Avoid scroll-jacking and lockouts; ensure browser back, anchors, keyboard, swipe, and user interruption work.
- Avoid critical data behind scroll reveal or hover. Never animate primary operational tasks slower for cinematic effect.
- Use `will-change` only shortly before expensive changes, not on entire pages.

## Acceptance examples
Good: entering a case-study chapter crossfades a contextual image while the text remains readable, with accessible skip behavior.
Bad: every paragraph fades in only after scrolling, leaving blank screens on low-power devices.
Good: a 150ms cart-added feedback animation confirms a POS action.
Bad: an 800ms card flip prevents a cashier from serving the next customer.
