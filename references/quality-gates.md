# Quality gates and design review rubric

## Gate 0 — Fit
- [ ] Primary audience, tasks and brand positioning explicitly represented.
- [ ] Concept is specific enough that replacing the logo would not make this a generic startup page.
- [ ] Project mode correctly chosen; primary success path accessible immediately.

## Gate 1 — Composition & aesthetic
- [ ] Typographic hierarchy clear on mobile and desktop, with meaningful line breaks.
- [ ] Alignment and spacing have a coherent underlying grammar.
- [ ] Sections vary for a reason; no repeated three-card filler.
- [ ] Photography and graphics have relevant subject matter and consistent art direction.
- [ ] Color contrast, surface separation, and focus/interaction states are legible.
- [ ] Imagery is authentic, licensed, approved, or explicitly marked as a placeholder.
- [ ] Details withstand close inspection: crop, baseline, icon size, borders and white space.

## Gate 2 — UX
- [ ] Within seconds a user can identify what this is, who it is for, and what to do next.
- [ ] Primary action works; navigation and search/findability fit task needs.
- [ ] Loading, empty, error, success, validation and disabled states exist where relevant.
- [ ] No faux controls, fake metrics, broken actions, inaccessible hover-only features.
- [ ] Mobile touch and keyboard navigation support primary journeys.

## Gate 3 — Accessibility
- [ ] Heading order, landmarks, labels, alternatives, form help and errors are accessible.
- [ ] Keyboard and focus order work, including overlays and dynamically updated content.
- [ ] Contrast appropriate for text, focus, UI components and image overlays.
- [ ] Reduced-motion users can complete every task without scroll-linked travel.
- [ ] Zoom, large text, short viewport and RTL/localized content do not break workflows.

## Gate 4 — Motion
- [ ] Every animated element has an explicit reason (orientation, hierarchy, causality, feedback, atmosphere).
- [ ] Content is readable without waiting for animation to finish.
- [ ] Animations are interruptible; repeated navigation and fast scrolling do not corrupt state.
- [ ] No persistent render/layout thrash, event-listener leaks or janky giant blurs.

## Gate 5 — Production
- [ ] Appropriate source of truth for data, no fabricated UI facts.
- [ ] Responsive widths validated including ~320–375, ~768, ~1280, ~1600, plus 200% zoom if possible.
- [ ] Lint/build/typecheck/test run where available; report actual results.
- [ ] Main images dimensioned and optimized; fonts and animation libraries justified.
- [ ] No exposed secrets, obvious unsafe HTML injection, or broken basic privacy behaviors.

## Prioritization rubric
Evaluate each area 0–4 (0 absent/broken; 1 poor; 2 workable; 3 strong; 4 exceptional). Multiply by weight:
- Functional UX × 5
- Accessibility × 5
- Brand specificity / anti-genericity × 4
- Information and content hierarchy × 4
- Craft: typography, grid, imagery × 4
- Performance and robustness × 4
- Motion intent and quality × 2

Weighted maximum = 112. Use the score as review organization, not a scientific metric. **Hard stop:** a critical flow broken, an inaccessible primary interaction, misrepresentative factual content, or significant exposed security issue blocks sign-off regardless of total score. In a product mode, give the operational workflow veto power over dramatic presentation.

## Review output
For each actionable finding: `Priority (P0/P1/P2) | location | observed evidence | user impact | exact fix | how to verify`. Distinguish directly observed facts from guesses. If visual proof is missing, say it is unverified rather than claiming a pass.

## Specific anti-AI-slop tests
1. Logo-swap: does design become interchangeable with another industry?
2. Section-swap: could any section reorder without affecting narrative or task flow?
3. Card inflation: are card shells used where a direct editorial layout or table would be clearer?
4. Gradient dependence: would layout work without glow, blur and noise?
5. Copy audit: count vague phrases lacking proof or specificity; replace with grounded content.
6. Motion audit: remove any animation that merely announces its own existence.
7. Detail audit: compare every action, state, image and breakpoint to a specific purpose.
