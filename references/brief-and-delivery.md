# Discovery, concept and delivery protocols

## Minimal project brief
Capture:
- Product/brand and domain.
- Audience and top 1–3 tasks.
- Intended emotion and positioning (e.g. calm premium medical confidence, not 'futuristic').
- Real content/assets available; any claims requiring verification.
- Screens and feature scope.
- Preferred tech and repository constraints.
- Languages/RTL, device targets, accessibility and performance requirements.
- Existing brand rules and nonnegotiables.
- Competitor/reference qualities to borrow vs reject.

## Design thesis formula
`For [audience], this [experience/product] should feel [3 specific qualities], using [domain-specific visual idea] to help users [primary outcome]. We will avoid [category clichés], preserve [crucial usability constraint], and make [distinctive proof/content] the focus.`

## Creative exploration (before code)
Draft 2–3 genuinely different *concept directions* when a project is ambiguous, each with distinct composition, imagery source, typography treatment, storytelling strategy, and restrained animation concept. Do not create superficial palette swaps. Select the best-fit direction and articulate trade-offs. For a clear user brief, select directly and implement.

## Page/system specification
Define for each screen or section:
- User question answered and target action.
- Content and its source.
- Layout/grid and type hierarchy.
- Image/art direction and mobile crop.
- Interactive controls and all states.
- Motion trigger/purpose/reduced-motion behavior.
- Responsive and localization edge cases.
- Acceptance criteria.

## One-shot implementation prompt template
```
ROLE: Senior digital art director + production frontend engineer.
DESIGN PHILOSOPHY: Cinematic Precision (apply the installed skill).
PROJECT: [name, context, audience, brand requirements].
GOAL: [primary outcome and observable success criteria].
MODE: [experience/product/hybrid] with justification.
CONCEPT: [specific narrative/visual motif unique to business].
CONTENT: [real pages, features, factual claims, supplied assets, missing-content policy].
INFORMATION ARCHITECTURE: [routes, sections, tasks, navigation].
VISUAL SYSTEM: [type hierarchy, font strategy, semantic palette, grid, spacing, image direction, surfaces, responsive rules].
MOTION: [where, why, triggers, tool choice, reduced-motion fallback, performance budget].
TECH: [existing stack, dependency policy, data flows, security and backend boundaries].
ACCESSIBILITY: [WCAG target, keyboard, focus, semantic structure, mobile, languages/RTL].
ACCEPTANCE: [working behavior, viewport review, lint/typecheck/build/tests, screenshots if available].
EXECUTION: Inspect repo -> state plan and assumptions -> implement -> test -> audit -> report verified results and limitations.
ANTI-PATTERNS: No generic 'AI slop', fake facts, purposeless cards/gradients/motion, inaccessible effects, or unsupported claims of tests passed.
```

## Handoff criteria
Report what files/screens changed; notable visual and technical decisions; dependencies added and why; what was tested, with concrete results; what couldn't be verified; any known accessibility/performance tradeoffs; how to run locally. For review-only work, report issues ranked by impact rather than a vague aesthetic score.
