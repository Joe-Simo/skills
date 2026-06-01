## Award Readiness And Verification

This is a local readiness gate inspired by public design-award evaluation
concepts and Awwwards' published evaluation categories. It is not official
Awwwards scoring and cannot predict nomination, judging, or award outcomes.

Hard blockers:

- App does not build, load, or complete the primary flow.
- Console has runtime errors, broken first-party assets, or failed required
  requests.
- Primary viewport has overlapping, clipped, unreadable, or off-screen UI.
- Mobile, tablet, laptop, desktop, or wide layouts break materially.
- Keyboard users cannot complete the primary flow.
- Critical contrast, focus, label, reduced-motion, or screen-reader failures
  exist.
- Placeholder/mock content remains where real content is expected.
- API keys, tokens, secrets, or sensitive config are exposed client-side.
- Official implementation docs evidence is missing for an advanced technology
  used in the work.
- The result is recognizable as a clone of a named reference or template.
- Animated, canvas, WebGL, Three.js/R3F, shader, image-sequence, or video-led
  surfaces render blank, are misframed, are hidden behind overlays, fail resize,
  fail route-change cleanup, lack loading/error/low-power/no-WebGL/static/
  reduced-motion fallbacks, or fail context-loss/fallback behavior.
- Required performance budget rows fail for initial JS, route chunk, media
  weight, texture size, DPR cap, draw calls, long tasks, frame pacing,
  LCP/INP/CLS where measurable, or fallback trigger.

Local website-evaluation critique dimensions:

| Dimension | Calibration Weight | Local Judge |
|---|---:|---|
| Design | 40% | Visual craft, hierarchy, typography, spacing, color, media quality, polish, first-viewport impact, responsive composition, and coherent system. |
| Usability | 30% | Primary task clarity, navigation, control affordance, forms, states, recovery, scanning, touch/mouse/keyboard ergonomics, and orientation. |
| Creativity | 20% | Distinctive concept, memorable interaction, domain-specific metaphor, non-template feel, originality, and surprise that supports meaning. |
| Content | 10% | Real, specific, structured copy/media/data; credible IA; no filler; content fits the interface and remains understandable without motion. |

Local developer critique lenses:

| Dimension | Calibration Weight | Local Judge |
|---|---:|---|
| WPO | 20% | Production build performance, optimized images/fonts/media, low JS/CSS waste, Core Web Vitals posture, and no avoidable blocking work. |
| RWD / Mobile | 20% | Verified mobile/tablet/laptop/desktop/wide layouts, no horizontal scroll, clipped text, broken grids, tiny targets, or layout collapse. |
| Markup / Metadata | 15% | Valid clean markup, no hydration/runtime warnings, complete favicon/social/app metadata, and sensible form/input attributes. |
| Semantics / SEO | 20% | Document outline, headings, landmarks, alt text, canonical/meta basics, meaningful URLs, and indexable content when relevant. |
| Animations / Transitions | 15% | Purposeful motion, smooth frame pacing, no layout jank, reduced-motion support, and no blocked interaction. |
| Accessibility | 10% | Keyboard path, focus states, contrast, labels, names/roles/values, target sizes, and screen-reader sanity. |

Official process wording guardrail:

- Do not say a project is likely to win, qualify, or receive a score.
- Do not invent SOTD, SOTM, SOTY, HM, Developer Award, or Mobile Excellence
  thresholds beyond published facts.
- Do not imply submission alone creates a nominee, jury review, public voting,
  visible score, or approval; Awwwards manually checks minimum requirements
  before approving a site and sending it to the Jury.
- Do not state numeric award thresholds or status mechanics unless verified
  live from official public documentation in the current task.
- Treat the Awwwards Status System as user privilege/voting status, not project
  quality status.
- Do not list Mobile Excellence as a fifth core website-evaluation criterion.
  Use Mobile Excellence checks only when the user asks for mobile-award posture
  or mobile-specific audit work.

Creative-director review must happen before assigning a pass label:

- Concepts considered:
- Chosen direction and why:
- Weakest dimension before revision:
- Taste issues found:
- Revisions made:
- Remaining risk:

Pass labels:

Rate each critique dimension as `weak`, `acceptable`, `strong`, or
`exceptional`. `Strong` requires a subject-native concept, polished system,
real content, usable interaction, and no generic template feel. Any `weak` or
`acceptable` dimension prevents `Strong local candidate`.

- `Strong local candidate`: no hard blockers, benchmark calibration completed,
  multiple concepts considered, one direction selected through
  creative-director review, every critique dimension at least strong, official
  docs evidence captured, browser evidence captured, measurable
  performance/accessibility checks passed, originality verified, and the result
  was revised after audit findings. This label is allowed only after the work
  has a clear original thesis, a memorable content-native interaction, strong
   first-viewport impact, real rights-cleared content/media, no failed budget
   row, and no unresolved weak or acceptable dimension in Design, Usability,
   Creativity, Content, performance, accessibility, or responsive behavior.
- `Production pass`: no hard blockers, primary flow works, responsive and
  accessibility checks pass, required performance budget rows pass, and
  remaining issues are minor and reported.
- `Fix required`: any hard blocker, unverified claim, inaccessible interaction,
  broken responsive state, poor performance, template feel, clone risk, or
  missing real content.

Do not average away weak dimensions. Excellent animation cannot compensate for
poor accessibility, broken mobile, fake content, or clone risk.

Required verification when a local app can run:

1. Run the app with the project's normal command and record command plus URL.
   For animation, WebGL/canvas, Three.js/R3F, GSAP/ScrollTrigger, video, or
   heavy media work, final browser verification must run against a production
   build or production-equivalent preview. Dev-server-only screenshots or
   profiles cannot support `Strong local candidate` or `Production pass`; if
   production preview cannot run, report the blocker and use `Fix required`
   unless the user explicitly scoped a non-production prototype.
2. Create a route/surface/state inventory for the requested scope: route,
   surface, required states, mobile screenshot, tablet screenshot, laptop or
   desktop screenshot, wide screenshot, interaction audit, status.
3. Capture screenshots at minimum: 375x812, 768x1024, 1440x900, and a wide
   desktop viewport. Include changed states: menus, overlays, galleries,
   loading, error, reduced-motion, 3D/canvas fallback, and primary interaction.
4. For animated/canvas/WebGL/video work, verify nonblank rendering, correct
   framing, resize behavior, reduced-motion behavior, console cleanliness, and
   no obvious scroll jank. For WebGL/canvas, include profiler/trace notes,
   DPR/back-buffer size, draw calls/triangles/textures/programs when available,
   context-loss/fallback behavior, and disposal checks after route changes.
5. Every custom cursor, hover reveal, drag, scroll, gesture, spatial
   navigation, 3D control, or media control must be exercised in browser at
   desktop pointer and mobile/touch sizes. Verify start, update, completion,
   cancel/Escape/reset, keyboard or touch equivalent, resize behavior, and
   recovered state after route changes; any failed or untested path is `Fix
   required`.
6. For video, audio, image-sequence, and authored media experiences, verify
   source loads, poster/fallback display, responsive encodes, preload/lazy
   behavior, controls, captions/transcripts when meaningful, autoplay-policy
   behavior, mute state, reduced-motion/reduced-data or low-power branch, and
   keyboard/touch control access. Failures block candidate labels when the
   media is part of the experience.
7. Run keyboard-only checks for navigation, controls, overlays, galleries,
   forms, skip/close behavior, focus trap/restore, Escape/Enter behavior, and
   visible focus.
8. Check WCAG 2.2 AA fundamentals: accessibility names, labels, contrast,
   target sizes, semantic outline, keyboard flow, visible focus, 200% zoom,
   forced colors/high contrast where supported, reduced motion,
   captions/transcripts where relevant, and hidden decorative media.
   Apply `accessibility-and-inclusive-experience.md` for the full protocol.
9. Check performance: production build if possible, route/media chunk sizes,
   image/video optimization, lazy loading, LCP path, long-task risk, Core Web
   Vitals lab/field evidence, low-end simulation, and offscreen animation
   pauses.
10. Run the project's lint, typecheck, build, and relevant tests. Fix issues caused
   by the work.
11. Apply the originality gate from `source-and-originality-gate.md`.
12. Revise, then re-run affected screenshots/checks.

Final evidence report:

```text
Scope:
References:
Benchmark calibration:
Concepts considered:
Chosen direction:
Weakest dimension before revision:
Official docs evidence:
Budgets:
Commands:
URL:
Viewports:
States/flows checked:
Motion/3D/canvas checks:
Accessibility checks:
Performance checks:
Profiler artifacts:
Core Web Vitals:
Evidence artifact paths:
Viewport/state pass-fail table:
Low-end checks:
Reduced-motion checks:
Originality check:
Taste review:
Creative-director revisions:
Decision: Strong local candidate / Production pass / Fix required
Award honesty note:
Blockers or whole-app not verified:
```

If the app cannot run or screenshots cannot be captured, state the exact
blocker and do not claim a strong local candidate or final visual verification passed.

Plan-only output contract:

When the user asks for strategy, concept, design direction, or a build plan
without implementation, output the concept brief, benchmark plan, concept
direction table, chosen direction, scene/flow map, content spine, visual thesis,
motion spec, media/audio/3D decisions, accessibility/performance budgets,
official docs needed, validation plan, and risks. Label the result `design plan
only`. Do not claim browser verification, production pass, or strong local
candidate until implementation and checks are completed.
