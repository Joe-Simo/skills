## Motion, Interaction, And 3D

Motion is part of the information architecture. It should clarify cause and
effect, reveal content, create continuity, or deepen the concept. It should not
exist because an award-site aesthetic was requested.

Technology decision gate:

| Need | Prefer | Avoid |
|---|---|---|
| Simple hover, fade, disclosure, or small transition | CSS or framework-native animation | GSAP just for basic effects |
| Complex timeline, pinned/scrubbed scroll, orchestration | GSAP/ScrollTrigger or proven project library | Scroll hijacking, fragile custom scroll engines |
| Route/shared-element continuity | View Transitions API or framework/library support | Full-page reload illusions that break history/focus |
| Realtime 3D, shaders, particles, spatial product interaction | Three.js or React Three Fiber in React apps | Raw WebGL unless required |
| Authored vector motion | Rive or Lottie with controls/fallbacks | Heavy JS animation for static decoration |
| Cinematic motion cheaper as pre-render | Optimized video/image sequence with poster/fallback | Live rendering that drains battery |
| Procedural 2D effect | Canvas/SVG/p5/Pixi only when justified | Canvas-only content or navigation |

Advanced Effect Decision Record:

Before shipping any GSAP timeline, smooth-scroll layer, Three.js/R3F/WebGL
scene, canvas effect, shader, video-led transition, audio-reactive behavior, or
custom pointer/gesture system, record:

- Selected stack and installed package/version.
- Official docs URL and section/anchor used.
- Simpler option rejected and why.
- SSR/hydration risk and client boundary.
- Cleanup/disposal plan for listeners, timelines, textures, geometries,
  materials, animation frames, scroll triggers, observers, and media streams.
- Reduced-motion branch and no-WebGL/static fallback.
- Performance budget: initial JS/media, texture sizes, DPR cap, draw calls,
  long-task target, FPS/frame pacing target, and fallback trigger.
- Browser evidence: screenshots, canvas pixel check, console check, resize
  check, profiler/trace notes, and low-end simulation result.

Every advanced effect must answer:

- Why this technology?
- What simpler option was rejected and why?
- What is the fallback?
- What happens with `prefers-reduced-motion`?
- What is the performance budget?
- How was it verified in a browser?

Motion rules:

- No `transition: all`; animate compositable properties when possible.
- Keep motion interruptible and input-responsive.
- Do not block navigation, scrolling, form use, or primary action completion.
- Avoid scroll-jacking. Smooth scroll must preserve anchors, keyboard behavior,
  browser history, and user control.
- Pinned/scrubbed sections must not trap touch, keyboard, or reduced-motion
  users.
- Page transitions must preserve focus, state, title, and back/forward behavior.
- Infinite animation loops should pause offscreen, on tab backgrounding, when
  hidden, and under reduced motion when non-essential.

Reduced motion:

- `prefers-reduced-motion` must reduce or replace non-essential motion.
- Stop or simplify parallax, camera movement, large scale/pan, scroll scrubbing,
  long transitions, cursor trails, and non-essential WebGL loops.
- Do not hide content as the reduced-motion fallback.
- Keep essential state transitions immediate, clear, and accessible.
- Verify the reduced-motion branch in a browser and capture evidence. For GSAP,
  prefer current `gsap.matchMedia()` and cleanup/revert patterns for breakpoint
  and reduced-motion branches.

3D/WebGL/canvas rules:

- Use 3D only when it carries the concept: product inspection, spatial
  storytelling, material/lighting, configurator behavior, simulation, game-like
  navigation, or impossible-to-film visual explanation.
- Keep semantic text, navigation, forms, and controls in the DOM.
- Provide loading, error, low-power, no-WebGL, reduced-motion, and static
  fallback states.
- Cap DPR, texture sizes, particle counts, post-processing, and draw calls based
  on device capability.
- Dispose geometries, materials, textures, event listeners, animation frames,
  and scroll triggers.
- Verify canvas pixels are nonblank, correctly framed, responsive, and not
  hidden behind overlays.
- Capture first-load and primary-interaction profiler evidence for WebGL/canvas
  work. Record DPR/back-buffer size, draw calls/triangles/textures/programs
  when available, long-task/frame-pacing notes, context-loss fallback, resize
  behavior, and disposal checks after route changes/unmount.
- On mobile, simplify camera movement, gestures, hit targets, lighting,
  particles, and post-processing.

Video/audio:

- Use video when authored cinematic motion is cheaper and more stable than live
  rendering.
- Provide poster frames, responsive encodes, controls when appropriate,
  captions/transcripts when meaningful, and no unmuted autoplay assumption.
- Audio should be user-initiated or clearly controllable, non-essential to
  comprehension, and respectful of mute/reduced-motion contexts.

Interaction design:

- Make the primary mechanic discoverable within the first interaction.
- Cursor effects must never replace standard pointer affordances or obscure
  controls.
- Gesture interactions need desktop and mobile alternatives.
- Hover-only reveals need touch, keyboard, and reduced-motion equivalents.
- Custom drag/scroll/gesture behavior needs escape, reset, and state recovery.
