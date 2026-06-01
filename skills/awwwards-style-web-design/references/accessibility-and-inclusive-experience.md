## Accessibility And Inclusive Experience Gate

Baseline: target WCAG 2.2 Level AA for all rendered UI in the verified scope.
Do not claim WCAG AA, inclusive experience, or production accessibility from
automated checks alone. Automated axe, Lighthouse, and accessibility-tree checks
are supporting evidence only; they never replace manual keyboard, screen
reader, zoom, forced-colors, media-alternative, and reduced-motion checks.

Required evidence matrix for each changed route/surface/state:

`surface | WCAG target | automated result | keyboard result | pointer/gesture alternatives | screen reader/accessibility tree result | forced colors | zoom/text spacing | media alternatives | reduced motion/motion control | cognitive/orientation result | inclusive content/localization result | blockers`

Automated checks:

- Run existing axe tooling, `@axe-core/playwright`, Lighthouse accessibility, or
  the closest project-native automated check against every changed route and
  important state: default, open menus, dialogs/sheets, validation errors,
  loading, empty, dense media/canvas state, and destructive/confirmation flows.
- Use WCAG 2.2 A/AA rules when supported by installed tooling; otherwise record
  the tool version and ruleset limitation.
- Treat violations as blockers. Treat `needs review`, contrast edge cases,
  focus order, names, live regions, media alternatives, and custom widgets as
  manual checks, not passes.

Manual keyboard protocol:

- Start before page content, Tab through the full page, Shift+Tab backward, and
  verify visible focus, logical order, no traps, skip-to-content where useful,
  and focus not hidden by sticky headers, drawers, cookie banners, or overlays.
- Operate every control without a pointer: Enter/Space for buttons and toggles,
  arrow keys/Home/End/Page keys where the WAI-ARIA pattern expects them, Escape
  to dismiss overlays, and locale-aware shortcuts only when documented.
- For overlays, verify initial focus, trapped/scoped focus while open, inert
  background where appropriate, Escape/cancel behavior, and focus restoration to
  the trigger.
- For drag, drawing, sliders, reordering, maps, canvases, gestures, and
  motion/device-orientation input, provide keyboard and simple single-pointer
  alternatives that reach the same content and outcome. Do not rely on
  path-based, multipoint, dragging, tilt, shake, or gesture-only input unless it
  is genuinely essential; if essential, document the reason and keep an
  alternate content path for the primary flow.
- Confirm target sizes: WCAG 2.2 AA minimum 24px pointer targets, plus 44px
  mobile touch targets for this skill's product-quality bar.

Screen reader and semantics protocol:

- Test with a real screen reader/browser pair when possible. If unavailable,
  state the exact blocker and limit claims to accessibility-tree inspection.
- Navigate by headings, landmarks, links, buttons, form controls, tables, and
  regions. Then read linearly from the top and operate the primary workflow.
- Verify name, role, value/state, current/selected/expanded/pressed/invalid
  state, dialog boundaries, table headers, form labels/descriptions/errors,
  live-region announcements, loading completion, route/title changes, and hidden
  decorative content.
- Prefer native HTML semantics. Use ARIA only to express behavior that native
  HTML cannot, and follow the matching WAI-ARIA Authoring Practices pattern for
  custom widgets.

Forced colors, zoom, and text spacing:

- Inspect forced colors/high contrast when tooling supports it. Do not rely on
  box-shadow, color alone, background images, gradients, opacity, or subtle
  borders for required affordances.
- Verify 200% browser zoom with no loss of content or functionality.
- Verify 400% zoom or 320 CSS px equivalent reflow with no two-dimensional
  scrolling except for content that genuinely requires it, such as data tables,
  maps, diagrams, games, or fixed tool workspaces.
- Apply WCAG text-spacing overrides during review: line-height 1.5, paragraph
  spacing 2em, letter spacing 0.12em, and word spacing 0.16em. Fix clipping,
  overlap, hidden controls, broken sticky regions, and unreadable truncation.

Media, captions, and transcripts:

- Inventory every audio/video/animation/media surface.
- Prerecorded synchronized media with audio needs captions. Live synchronized
  media needs captions for AA. Prerecorded video needs audio description or an
  equivalent media alternative as applicable.
- Audio-only and video-only content need equivalent alternatives. Provide
  transcripts for meaningful prerecorded audio/video by default. If source
  material is unavailable, treat the media alternative as a production-readiness
  blocker unless the media is decorative, is already a clearly labeled media
  alternative for text, or is removed/replaced for the verified scope.
- Captions/transcripts must include meaningful speech, speaker changes when
  needed, important non-speech audio, and visual information needed to understand
  the content. Do not treat unreviewed auto-captions as production-ready.

Reduced motion and sensory safety:

- Test with `prefers-reduced-motion: reduce`. Disable or greatly simplify
  non-essential motion, parallax, scroll-linked animation, animated gradients,
  cursor effects, smooth scrolling, looping decorative animation, and large
  transform/zoom transitions.
- For high-motion or immersive experiences, provide a visible,
  keyboard-accessible `Reduce motion`/`Static mode` control before non-essential
  motion starts. It must persist for the session/user, default on when
  `prefers-reduced-motion: reduce` matches, and disable or replace
  interaction-triggered camera movement, parallax, scroll scrubbing, cursor
  trails, zoom/pan transitions, animated backgrounds, and non-essential
  WebGL/canvas loops.
- Keep essential state changes understandable without motion. Do not use motion,
  color, sound, position, or shape as the only cue.
- Nothing may flash more than three times per second. Auto-updating or moving
  content must be pausable, stoppable, hideable, or genuinely essential.

Cognitive and orientation protocol:

- Verify users can understand where they are, what changed, what is
  interactive, how to skip/exit immersive scenes, and how to complete the
  primary action without memorizing instructions or decoding motion-only cues.
- Check plain-language labels/instructions, predictable navigation, no
  unnecessary time pressure, recoverable errors, consistent help/contact paths
  where relevant, and comprehension without sound, color, motion, or spatial
  metaphor.

Inclusive experience checks:

- Avoid unnecessary demographic assumptions, binary-only personal data, rigid
  name parsing, location/IP language inference, idioms that block comprehension,
  and placeholder examples that imply only one kind of user or organization.
- Support long names, non-Latin text, browser translation, user locale formats,
  right-to-left or mixed-direction content when the product supports those
  languages, and clear recovery paths for errors, permissions, empty states, and
  offline states.
