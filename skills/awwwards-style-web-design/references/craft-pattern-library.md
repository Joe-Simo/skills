## Craft Pattern Library

Use these patterns as craft prompts, not templates. Choose only patterns that
serve the subject, content, accessibility, and performance budget. Define the
project-specific reason before implementation.

Patterns are vocabulary, not page layouts, visual identities, animation
sequences, starter kits, or winner lookalikes.

## Surface Archetype Prompts

These are starting prompts, not layouts.

| Surface | First Viewport | Composition | Motion/Media | Risk |
|---|---|---|---|---|
| Luxury/product launch | Real product visible immediately, brand, primary action, next-section hint | Product-centered stage, side-rail facts, precise captions | Poster first, macro video/pre-render or justified 3D, 160-220ms controls, 600-1000ms reveals | Hidden product, black/gold cliche, fake scarcity, slow preloader |
| Editorial scroll | Chapter title, key image/data/story hook, clear continuation | Alternating full-bleed media, reading columns, caption bands | Chapter reveals, masks, restrained scroll-linked continuity | Scroll effect outruns comprehension |
| Portfolio/artist | Name, signature work, selected-work path, contact/archive cue | Work-first grid/acts, captions, detail pages, archive filters | Gallery-to-detail transitions, hover/tap/focus previews | Fake biography, inaccessible archive, WebGL without content reason |
| 3D showcase | Object visible via poster/static fallback before live scene | DOM facts and controls around scene, not inside canvas | Orbit/inspect/configure only if useful, DPR/texture caps | Canvas-only content, weak fallback, GPU cost |
| Campaign/culture world | Event/message/artifact visible, clear role for user | World, timeline, room, map, stage, or ritual tied to content | Sound/video/spatial layers only with controls and equivalents | Vibe without message, inaccessible spectacle |

## Motion Timing And Easing

Motion should feel authored, interruptible, and tied to cause/effect.

- Micro feedback: 120-220ms for button, link, toggle, hover, focus, cursor, and
  local control feedback. Prefer ease-out; avoid bounce unless the brand is
  explicitly playful.
- Small reveals: 220-420ms for captions, cards, overlays, local image reveals,
  and menu items. Use stagger only when it clarifies order.
- Section transitions: 500-900ms for chapter changes, route transitions,
  full-bleed media reveals, and major layout shifts. Keep content readable
  before and after the transition.
- Cinematic beats: 900-1600ms only when the user is not waiting for a primary
  task. Provide skip/static mode for long sequences.
- Easing grammar: use sharper ease-out for direct input, sine/in-out for
  ambient continuity, expo/circ for cinematic reveals, and linear only for
  continuous physical motion. Keep one easing family per surface.
- Stagger rhythm: 30-80ms for dense text/list items; 80-140ms for large media
  or scene layers. Stop stagger if it delays comprehension.

Required motion spec for meaningful animation:

`surface | trigger | purpose | property | duration | easing | delay/stagger | interrupt/cancel | reduced-motion behavior | verification`

Sequencing rules:

- Orient first, reveal the primary object/content second, then supporting
  text/actions. Do not animate all layers at once.
- Map scroll chapters to content beats, not decorative progress.
- Body copy should be readable before animation. Use line/word masks for display
  moments only, preserve reading order, and do not animate layout-critical type
  metrics.

## Transition Archetypes

- Cut: instant change for task flow, reduced motion, and clarity.
- Fade/reveal: text, captions, metadata, low-risk content swaps.
- Mask/wipe: product/material reveals, editorial chapter openings, before/after
  comparisons. Tie mask direction to reading order or object geometry.
- Shared element: gallery-to-detail, product-to-configurator, case-card-to-case
  page. Preserve focus, URL, title, and back behavior.
- Camera move: spatial story, 3D product inspection, room/world navigation.
  Keep a DOM navigation equivalent and reduce camera movement under static mode.
- Scroll chapter: a sequence of scenes where each section adds content. Avoid
  scroll-jacking; pinned sections need keyboard/touch escape and reduced motion.
- Material transition: blur, refraction, grain, light, paper, glass, fabric,
  ink, metal, or clay only when the material belongs to the subject.

Route or section transitions need entry, hold, exit, focus restoration,
URL/history behavior, and a reduced-motion cut/fade fallback.

## Typography And Composition

- Pick type roles before font names: display voice, reading voice, metadata,
  controls, captions, numerals, code/data, and labels.
- Use display type for moments, not every paragraph. Reading text should stay
  legible at mobile and desktop sizes without viewport-width scaling.
- Create contrast through scale, weight, width, spacing, alignment, and rhythm;
  do not rely on one huge headline to carry the page.
- Compose each viewport with a clear focal object, reading path, negative space,
  anchor alignment, and one dominant action or continuation cue.
- Use asymmetry deliberately: one stable anchor plus one expressive counterweight
  is stronger than random offsets.
- Dense editorial layouts need hierarchy through captions, labels, chapter
  markers, image crops, and repeated alignment rules.
- Full-bleed media needs readable anchored text, safe contrast, captions when
  useful, and a visible next step.

## Art Direction

- Define a metaphor that belongs to the subject: archive, instrument, map,
  stage, object lab, timeline, room, material study, signal, ritual, catalog, or
  cinema sequence.
- Color should come from brand, product, material, place, time, emotion, or
  content taxonomy. Avoid generic neon-on-black, purple gradients, and random
  shader palettes.
- Texture, grain, blur, lighting, depth, and distortion must support the
  metaphor. Remove decorative effects that do not improve orientation, emotion,
  or content meaning.
- Media treatment should be consistent: crop logic, color grade, masking,
  captions, hover/tap states, loading style, and fallback imagery.
- Audio, haptics, and sensory cues are optional layers. They must be
  user-controlled and never required for comprehension.

## Interaction Patterns

- Make the first interaction teach the mechanic. Users should know what changed,
  why it changed, and how to continue.
- Cursor effects can echo material or depth, but never replace pointer,
  keyboard, focus, labels, or hit targets.
- Drag, scrub, orbit, tilt, and spatial controls need keyboard and simple
  pointer alternatives plus reset/cancel behavior.
- Hover reveals need touch and keyboard equivalents. Do not hide essential copy,
  links, or actions behind hover.
- Progressive disclosure should reveal meaning, not delay basic information.

## GSAP, Motion, And Scroll Choreography

- Use CSS/framework animation for simple state transitions.
- Use GSAP/ScrollTrigger or an existing project library when timelines,
  scrubbing, pinning, sequencing, or cross-element orchestration are the real
  requirement.
- For GSAP, scope timelines to the component, use matchMedia-style branches for
  breakpoints/reduced motion, kill/revert on unmount, and avoid animating layout
  properties when transforms/opacity can do the job.
- GSAP timelines should use labels for meaningful beats and cleanup every
  timeline, trigger, observer, and listener on route change/unmount.
- For Motion-style component animation, keep variants/states semantic, avoid
  large layout thrash, and make exit/enter transitions preserve focus and route
  comprehension.
- Motion variants should use semantic state names, not decorative labels, and
  reflect real UI states such as `idle`, `open`, `selected`, `exiting`, or
  `reduced`.
- Scroll animation should follow content chapters. If the scroll effect is
  impressive but the page is harder to read, simplify it.

## Three.js, R3F, WebGL, And Canvas

- Choose realtime 3D only for inspection, spatial comprehension,
  configurability, simulation, or material/light behavior that flat media cannot
  communicate.
- Prefer pre-rendered video/image sequences when the scene is cinematic and not
  interactive.
- Keep text, navigation, forms, and core content in semantic DOM.
- Plan camera, lighting, material, interaction, fallback, and loading before
  adding post-processing.
- Define camera, material, and lighting intent before shader/post-processing
  decisions. If the scene's meaning survives as flat media, consider video or
  image sequence first.
- Cap DPR, texture sizes, particles, post-processing, and draw calls. Provide
  low-power/no-WebGL/static/reduced-motion branches.
- Verify canvas pixels, framing, resize, context loss/fallback, route cleanup,
  and first-interaction performance in a production-equivalent browser run.

## Media And Audio

- Use video/image sequences for authored cinematic transitions, product motion,
  performance-heavy effects, or footage that users need to inspect.
- Provide poster frames, responsive encodes, captions/transcripts where
  meaningful, mute/default controls, keyboard access, and reduced-data/static
  alternatives.
- Audio can add atmosphere, rhythm, or feedback only when user initiated or
  clearly controllable. Never autoplay unmuted or require sound for meaning.
- Build a cue map for audio/video changes: cue, trigger, narrative/state
  meaning, visible equivalent, control, fallback, and reduced-data/static branch.

## Strong Vs Weak Signals

Strong:
- The concept could only belong to this subject.
- Motion explains state, sequence, material, or narrative.
- Typography, media, layout, color, and interaction share one thesis.
- The first viewport shows the real object/story and invites the next action.
- The page still works without animation, audio, WebGL, or hover.

Weak:
- Generic agency slogans, fake awards, fake client grids, dark neon canvas, and
  decorative shaders stand in for content.
- Motion delays comprehension or hides broken hierarchy.
- 3D/WebGL is present because it looks expensive, not because it clarifies.
- Mobile is a stripped-down afterthought rather than a designed version.
- The design is recognizable as a winner, template, tutorial, or demo.
