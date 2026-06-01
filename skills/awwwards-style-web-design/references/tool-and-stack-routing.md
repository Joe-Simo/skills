## Tool And Stack Routing

Official library docs, project-local packages, and local verification tools can
help implementation, but none replace the originality gate, concept work,
browser verification, accessibility, or performance checks in this skill. This
skill does not depend on external templates, starter kits, boilerplates,
plugins, unofficial source code, or demo code. It owns its design process.

## Owned Synthesis Rules

Use these rules when deciding whether a technology belongs in the experience:

- Do not make a template the design system or implementation path. Demo content,
  deployment commands, framework versions, and default animation stacks are not
  design authority.
- Do not force one stack. React, Next.js, Vite, Tailwind, GSAP, Lenis,
  smooth-scroll libraries, Motion, Anime.js, Three.js, R3F, Canvas, Rive, and
  Lottie are options only after the concept, host project, and performance
  constraints justify them.
- Do not treat animation libraries as taste. Motion quality comes from purpose,
  timing, restraint, cleanup, responsiveness, and reduced-motion behavior.
- Do not treat a single UI sample as the Awwwards aesthetic. Light mode, Inter,
  4px spacing, specific hex colors, fixed desktop canvas sizes, or specific
  heading sizes are sample-system traits, not universal rules.
- Keep specialized animation knowledge inside this skill's own gates: choose
  the simplest capable library, scope effects, clean up listeners/timelines,
  avoid layout animation, verify scroll behavior, and test reduced motion.
- Treat smooth scroll as risky infrastructure. Use it only when the concept
  needs it, preserve anchors/history/keyboard/touch behavior, and disable or
  simplify it for overlays, reduced motion, and low-power contexts.
- Treat generated/geometric/audio-reactive/physics effects as authored media
  systems. They need a concept reason, controls or fallbacks, performance
  limits, and browser evidence.

Official Implementation Docs Gate:

- Use official documentation or project-local source as implementation authority
  for libraries and platform APIs: Three.js, WebGL/MDN, GSAP, React, Next.js,
  Vite, Tailwind, CSS, HTML, WCAG/WAI, browser performance APIs, Playwright,
  and the host framework's official docs.
- Use package docs only for the package actually installed or intentionally
  selected in the user's project.
- Do not use blogs, personal demos, CodePen, StackOverflow, template pages,
  starter code, demo code, or non-authoritative award-style pages as authority
  for implementation decisions.
- Before final claims, report official docs evidence for every advanced
  technology used: URL, section/anchor, installed package/version when relevant,
  decision affected, and fallback if docs access was blocked.

Implementation tools:

- Use the host project's existing framework, package manager, component
  primitives, routing, and validation commands first.
- Use project-local product UI primitives when the host app already has them.
  This skill should own only the requested experiential surface and should not
  route users to any external skill, repository, template, starter, or
  boilerplate.
- Use local React/Next/Vite/framework knowledge for architecture, routing, build
  performance, metadata, and server/client boundaries.
- Use existing project-local accessible primitives or already-installed
  headless UI libraries for behavior; restyle them to the chosen art direction.
- Use Three.js/R3F/WebGL/game knowledge for real 3D, shaders, particles, or
  game-like scenes only when the project needs those capabilities.
- Use video tooling only for generated videos or motion graphics, not normal
  interactive web pages.
- Use Figma tooling when the user asks to create or implement a design file.
- Use image generation only for original assets the user has rights to
  use, never to recreate a winner's protected visuals.

Verification tools:

- Use Browser, Playwright, or agent-browser helpers for screenshots, responsive
  checks, interaction tests, reduced-motion checks, console inspection, and
  canvas/WebGL pixel checks.
- Use before/after or visual comparison helpers when the user asks for visual
  diffs or when a redesign needs evidence.
- Use deployment helpers only when the user asks to publish; deployment success
  does not replace design verification.
