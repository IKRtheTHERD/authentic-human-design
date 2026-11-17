---
name: authentic-human-design
description: Human-directed anti-AI-slop design skill. Design, implement, refine, and audit distinctive premium web interfaces using cinematic art direction, Swiss-inspired editorial typography, purposeful GSAP/motion, strong UX, and production-grade frontend engineering. Use for websites, landing pages, portfolios, clinics, research platforms, SaaS dashboards, POS interfaces, and whenever the user asks for non-generic high-end UI/UX, layout, animation, or visual polish.
---

# AUTHENTIC HUMAN DESign — Cinematic Precision Design & Engineering Skill

> **Identity:** Designed to be experienced. Engineered to be understood.
>
> **Aesthetic principle:** Cinematic atmosphere + architectural composition + disciplined interaction + functional clarity.
>
> **Priority order:** user goals and content → accessibility and usability → concept and art direction → implementation quality → expressive polish.

This skill is a **human-directed, anti-AI-slop design decision framework**, not a fixed template, color scheme, or animation preset. Create a distinct design for each product. Do not automatically force dark mode, full-screen hero imagery, 3D, giant text, glassmorphism, or animations onto every page.

## When to activate

Use this skill when asked to design, build, critique, redesign, or polish frontend experiences; establish a visual direction; implement scroll/interaction systems; or assess whether an interface feels generic/AI-generated. Also use on brand-relevant product interfaces where visual quality must coexist with operational usability.

## Required operating method

1. **Inspect before proposing.** When working in a repository, inspect files, routes, tech stack, styles, components, fonts, assets, tests, and existing design constraints. Preserve established workflows and user data. Never claim to have inspected a file, UI, or browser if you have not.
2. **Define the brief.** Extract audience, primary user goal, conversion/task, brand positioning, content, platform, accessibility requirements, performance budget, and project constraints. If information is missing, make reversible assumptions and state them; ask only if a truly blocking decision exists.
3. **Choose a project expression.** Use `experience` for story-led marketing, portfolios, campaigns, and cinematic landing pages; `product` for SaaS, research, admin, POS and operational screens; `hybrid` when an expressive marketing layer leads to highly usable application screens. See [references/modes.md](references/modes.md).
4. **Write a design thesis** (2–4 sentences): audience, emotional tone, distinctive visual metaphor, functional success criterion. Create at least one clear reason the result is specific to this brand or business.
5. **Establish tokens and page grammar.** Define typography, layout grid, spacing scale, color roles, radius/shape language, media treatment, interaction hierarchy, and responsive behavior before styling components. Use [references/design-system.md](references/design-system.md).
6. **Design with actual content.** Prioritize credible copy, product facts, task flow, states, information hierarchy, and visual assets. Do not pad with empty slogans, generic metrics, stock-card grids, or meaningless decorative dashboards.
7. **Implement in functional passes.** Semantic structure → responsive layout → typography/color → imagery/materials → interactions → motion → edge states → optimization. Avoid polishing an unworkable concept.
8. **Audit before completion.** Run the applicable checks in [references/quality-gates.md](references/quality-gates.md). Fix critical usability/accessibility/performance defects before cosmetic improvements. Report verified results and remaining uncertainties.

## The 7 governing principles

1. **Visual authority, not visual noise.** Strong hierarchy, refined type, controlled contrast, and spatial intention are more premium than numerous effects.
2. **Cinematic composition, not theatrical UI.** Use framing, depth, atmosphere, editorial pacing, and light as a storytelling medium; never obstruct the user's task.
3. **Every movement has a job.** Motion must reveal hierarchy, explain causality, preserve continuity, provide feedback, or reinforce emotion. Otherwise remove it.
4. **Concept over template.** Use brand/product-specific imagery, interaction metaphors, typography, and page rhythm. Do not repeat the same hero–3 cards–testimonials–CTA blueprint by default.
5. **Precision is visible.** Alignment, typography metrics, image crops, state consistency, touch targets, focus treatment, and spacing matter more than clever flourishes.
6. **Function changes the art direction.** A POS sales screen requires clarity and speed; a cinematic portfolio may invite exploration. The same principles apply with different intensity.
7. **Deliver production quality.** Prefer semantic HTML, predictable component APIs, measured performance, reduced-motion alternatives, robust keyboard navigation, secure dependencies, and tested responsive layouts.

## Visual direction: strong defaults, not rigid rules

- **Composition:** controlled negative space, strong focal point, asymmetry when balanced, intentional grid breaks, contextual editorial sections, occasional full-bleed imagery.
- **Typography:** typographic scale with disciplined line length; confident headlines, sharp labels, readable body copy. Candidate families: Geist, Inter, Satoshi, Neue Montreal (subject to licensing/availability), and a context-appropriate editorial serif. Avoid loading unnecessary font weights.
- **Color:** neutral foundations and one meaningful contextual accent. Example dark roles: obsidian `#101114`, graphite `#292C31`, ivory `#F0EEE8`, muted steel `#9299A4`; optional accent blue `#567CFF` or amber `#C17C48`. **Do not assume these values suit all brands.** Design equally strong light themes.
- **Photography & media:** authentic brand-relevant imagery where possible; plausible materials, cropping, lighting and spatial depth. Avoid generic AI imagery, indiscriminate gradients, or fake product visuals. Make attribution and usage rights explicit when required.
- **Shape:** prefer purposeful, consistent radii and border weights over ubiquitous oversized pills. Use generous spacing where content allows, denser rhythms where tasks demand it.
- **Motion:** choreographed, fast enough to remain efficient, interruptible, composited when possible, and respectful of `prefers-reduced-motion`. See [references/motion-system.md](references/motion-system.md).

## Anti-genericity gate (mandatory)

Before delivering, ask:
- Could I replace the logo and the page would still fit any random startup? If yes, increase domain-specific storytelling and structural differentiation.
- Are visuals or effects present only because they are fashionable? Remove them.
- Does each section have a distinct user/job-to-be-done role? Cut repetition.
- Is typography doing real hierarchy work, or is everything uniform cards and badges?
- Are real client/project facts and meaningful workflows more prominent than generated filler?
- Does a user understand what to do in the first few seconds without waiting for animations?

## Interaction & animation decision tree

**Default: native behavior first.** Use CSS for simple hover/focus/transitions; use a component motion library for state transitions; use GSAP/ScrollTrigger when sequencing, complex coordination or scroll timelines demand it. Smooth-scrolling libraries such as Lenis are optional and must not interfere with accessibility, browser behaviors, native anchors, focus, or touch. Parallax and WebGL must have measurable value and viable fallbacks. Never install a major library for one trivial fade.

Read [references/motion-system.md](references/motion-system.md) before implementing complex motion.

## Modes and situational constraints

Read [references/modes.md](references/modes.md) to determine the correct intensity, including:
- **Cinematic experience:** storytelling, portfolio, premium campaign, exploratory website.
- **Precision product:** operational interfaces, POS, research platform, complex forms, dashboards.
- **Hybrid:** expressive exterior with task-efficient interior.

For dental/medical sites, additionally preserve accessibility, consent-sensitive photography, credible clinical information, appointment discoverability and trust. For research/education, prioritize findability, language support, legitimacy and accessible information architecture. For POS, prioritize speed, error prevention, keyboard use, recoverability and legible density.

## Implementation standards

Read [references/engineering.md](references/engineering.md) when writing or reviewing code. In summary:
- Work within the project's existing stack unless change is justified.
- Compose reusable semantic components; establish design tokens rather than unmaintainable ad-hoc styling.
- Support mobile, tablet, desktop, zoom, keyboard, screen reader, and reduced motion.
- Avoid layout shifts, scroll hijacking, render-blocking fonts, massive JS bundles and uncompressed media.
- Use actual breakpoints dictated by content, not just framework defaults.
- Optimize interactions for touch as well as pointer; hover is never the only route to an action.
- Handle loading, empty, error, success, disabled and validation states.
- Do not invent benchmarks, Lighthouse scores, screenshots, user research, or test passes.

## Review modes

**If asked to build:** implement functioning UI with appropriate states. Design quality is not a substitute for working navigation, actions, or data handling.

**If asked to critique:** produce prioritized findings supported by observable UI/code evidence: severity, user impact, exact issue, recommended correction. Do not pretend a taste preference is a defect.

**If asked to improve an existing UI:** preserve successful interaction patterns and brand equity; identify leverage points before redesign. Confirm the old flows still work.

**If asked for a one-shot prompt:** include brief, constraints, project-specific concept, screens/sections, design tokens, interaction specification, stack, accessibility/performance constraints, acceptance criteria, and clear evidence required from the implementing agent. See [references/brief-and-delivery.md](references/brief-and-delivery.md).

## Required deliverable format

For substantial design/build tasks, end with concise sections: **Concept** (what makes it specific), **Implemented** (what changed), **Validation** (what was actually checked), **Trade-offs** (intentional limits), and **Next priorities** (only unresolved work). Adapt length to task. Do not imply browser testing or pixel inspection without actually doing it.

## References

- [Design system, color, typography, layout, imagery](references/design-system.md)
- [Motion choreography, GSAP, Lenis, accessibility](references/motion-system.md)
- [Experience/product/hybrid modes](references/modes.md)
- [Frontend engineering and performance](references/engineering.md)
- [Accessibility, anti-template tests, acceptance checks](references/quality-gates.md)
- [Discovery brief, project prompts and handoff](references/brief-and-delivery.md)
- [Project-specific application examples](references/examples.md)
