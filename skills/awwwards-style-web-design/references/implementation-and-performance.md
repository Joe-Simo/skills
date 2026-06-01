## Implementation And Performance

Use the host project's stack and conventions. Add dependencies only when they
solve a concrete problem and are compatible with production constraints.

Implementation discipline:

- Prefer TypeScript/TSX in typed projects.
- Use local packages and assets; do not rely on CDN-hosted Tailwind, Monaco,
  fonts, runtime libraries, or production-critical scripts.
- Do not clone templates, starters, boilerplates, demo apps, unofficial source
  code, or generated template code as the implementation route. This skill
  should guide original work inside the user's actual codebase using
  project-local packages and official library documentation.
- Use established libraries for specialized behavior instead of hand-rolled
  engines.
- Keep design tokens, layout primitives, motion primitives, media primitives,
  and accessibility behavior shared rather than one-off per section.
- Preserve existing routes, content, real data paths, analytics/privacy
  settings, auth boundaries, and forms unless the user requests changes.
- Do not expose API keys, tokens, private config, or sensitive data client-side.

Framework guidance:

- Next.js: use the App Router conventions already present; keep server/client
  boundaries deliberate; load fonts and metadata through framework-supported
  APIs; optimize images and route-level code splitting.
- React/Vite: split heavy experiential components, lazy-load below-fold media
  and 3D, and keep global state minimal.
- Astro/Svelte/Vue/HTML: preserve the project's architecture and use native
  islands/components or progressive enhancement instead of forcing React.
- Tailwind: use local configured Tailwind; map visual decisions to tokens and
  utilities rather than ad hoc long class strings when shared behavior is
  needed.
- Use existing project-local accessible primitives or already-installed
  headless UI libraries for behavior; do not import generated component
  templates solely for this skill.

Performance requirements:

- Declare project-specific budgets before adding heavy media or animation:
  initial JS, media weight, font files, route chunks, image/video sizes,
  texture sizes, DPR, animation FPS target, and acceptable fallback.
- Starter budgets when the project has none, to be tightened or relaxed with
  evidence: keep first-viewport poster near 300KB, first-viewport media near
  900KB, lazy-load 3D/heavy animation chunks, cap DPR around 1.5 on mobile and
  2 on desktop, cap textures near 1024px mobile and 2048px desktop, keep
  interaction long tasks under 50ms, and define a fallback trigger for low-power
  or failed media/WebGL.
- Use a budget table with target, measured value, tool, pass/fail, and revision
  decision for: initial JS, largest route chunk, total route JS, critical CSS,
  font files, LCP element, image/video media, texture dimensions, DPR cap, draw
  calls, long tasks, frame budget, and fallback trigger.
- Treat Core Web Vitals as release criteria where measurable: LCP <= 2.5s, INP
  <= 200ms, and CLS <= 0.1 at the 75th percentile across mobile and desktop
  when field data exists. In lab-only work, record the lab tool, throttling, and
  limits instead of pretending field data exists.
- Optimize LCP path: critical text/media, font loading, image priority, poster
  frames, and no unnecessary client-only blocking work.
- Lazy-load below-fold 3D, video, image galleries, and animation timelines.
- Avoid hidden long tasks, scroll jank, forced sync layout, unbounded
  `requestAnimationFrame`, and always-on offscreen rendering.
- Compress and size images/video for the actual responsive layout.
- Preload only what is truly critical.
- Use reduced-quality modes for low-power/mobile devices when needed.
- For animation, WebGL, canvas, or heavy media, capture a production-build
  browser profile for first load and the primary interaction. Include low-end
  simulation when possible: CPU throttle, network throttle for media-heavy
  routes, long-task notes, frame pacing, memory/GPU risk, and fallback trigger.

Accessibility requirements:

- WCAG 2.2 AA fundamentals are the default accessibility target unless the
  project has a stricter requirement.
- Semantic DOM and logical heading order remain mandatory.
- Keyboard users must complete the primary flow.
- Focus-visible states must be clear on custom controls, overlays, menus,
  sliders, galleries, and spatial navigation.
- Text, captions, controls, and overlays need readable contrast over media.
- Interactive targets must be reachable and large enough on mobile.
- Announce loading/error/complete states when they affect task completion.
- Keep decorative canvas/SVG/media hidden from assistive tech.
- Use accessible names, roles, values, and labels for icon-only and custom
  controls.
- Run an automated accessibility check when tooling exists, then manually check
  keyboard order, focus visibility, zoom to 200%, forced colors/high contrast
  where supported, reduced motion, labels/names/roles, captions/transcripts,
  and screen-reader sanity for the primary flow. Automated checks do not replace
  manual interaction checks.

SEO and metadata:

- Keep meaningful titles, descriptions, canonical/social metadata, favicons, and
  share images for public marketing/editorial sites.
- Do not bury all content in canvas, images, or client-only effects when it
  should be indexable.
- Alt text and captions should describe content purpose, not visual decoration.

Validation:

- Run the project's lint, typecheck, build, and relevant tests after
  implementation.
- If commands are missing, inspect package scripts and use the closest
  production validation available.
- Fix warnings/errors caused by the work instead of lowering standards.
