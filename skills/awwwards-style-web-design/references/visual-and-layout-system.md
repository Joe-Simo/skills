## Visual And Layout System

An award-caliber experiential site does not have one fixed aesthetic. The shared pattern
is a coherent art-directed system: concept, typography, layout, media, color,
motion, and interaction all serve the same subject.

Visual system requirements:

- Define a visual thesis before styling: typographic voice, palette, material,
  image treatment, layout rhythm, depth model, and interactive motif.
- Use a compact, intentional palette. Avoid broad random gradients, one-note
  monochrome palettes, and color chosen only for mood.
- Pick type for the concept and content. Use readable text, deliberate display
  moments, consistent hierarchy, and responsive scale. Do not rely on huge
  headlines to fake drama.
- Use real media whenever the product, person, object, place, art, or gameplay
  needs inspection. Avoid purely atmospheric stock-like imagery for concrete
  products.
- Build reusable tokens and primitives for spacing, color, type, focus, motion,
  overlays, controls, captions, and media frames.
- Treat navigation as part of the concept only when it remains understandable,
  keyboard reachable, and mobile usable.

Layout patterns that can work:

- Scene-based scroll, where each section has a clear role and the transitions
  create continuity.
- Full-bleed media with readable anchored text and visible next-step affordance.
- Editorial grids that mix large and small moments without breaking reading
  order.
- Spatial canvases or 3D scenes with semantic DOM controls, captions, and
  alternate content.
- Dense galleries or archives with deliberate filters, labels, hover/tap states,
  and responsive image behavior.
- Split attention layouts only when both sides remain meaningful at mobile and
  desktop sizes.

Anti-template checks:

- Reject generic agency/AI startup sections, fake logo bands, vague value props,
  card piles, shader blobs, noisy parallax, and ornamental cursor effects when
  they are not tied to subject or content.
- Reject dark-canvas-plus-neon as a default "Awwwards look".
- Reject scroll-jacking, hidden navigation, mystery-meat interactions, tiny
  text, invisible focus, hover-only content, and unreadable contrast.
- Reject canvas/WebGL-only text, links, forms, or navigation. Keep meaningful
  content in the DOM.
- Reject fake awards, fake clients, fake metrics, placeholder case studies, and
  invented press.
- Reject mobile as an afterthought. Mobile can simplify the mechanic, but it
  still needs a designed experience.

Taste review gate:

- State the intended first impression in one sentence, then verify the screen
  actually creates it.
- Check whether the page could belong to the specific brand, product, artist,
  place, or story only. If it could be swapped into any agency template, revise.
- Remove one decorative move that does not support content, orientation, or
  emotion.
- Check type, spacing, media, color, and motion as one system, not separate
  effects.
- Identify the memorable moment users would recall after closing the page.
- If spectacle weakens comprehension, trust, accessibility, or speed, simplify
  the spectacle and raise craft elsewhere.

Responsive craft:

- Define stable dimensions with aspect ratios, container queries, grid tracks,
  or clamp boundaries for hero media, cards, galleries, canvases, and controls.
- Avoid viewport-width font scaling that breaks long words or mobile text.
- Check narrow mobile, common tablet, laptop, desktop, and wide desktop.
- Ensure text never overlaps media or controls incoherently.
- Keep tap targets usable, captions readable, and controls reachable with
  thumbs.
- Provide safe-area handling for fixed controls and immersive scenes.

UI states:

- Every control needs rest, hover, active/pressed, focus-visible, disabled,
  loading, selected/current, and error states when relevant.
- Experiential pages still need loading, error, offline/unavailable media,
  reduced-motion, no-results, and recovery states.
- Long loading sequences must show progress or meaningful skeleton/fallback
  content; do not trap users in a preloader.

Content quality:

- Copy should be specific, concrete, and structured around the experience.
- Content order should make sense without animation.
- Captions, labels, units, dates, and microcopy should add orientation.
- Media should have intent: reveal, compare, demonstrate, teach, or create
  atmosphere tied to the subject.
