## Foundation Gate

For any task that creates or materially changes rendered UI, complete the Geist foundation layer before screen design or screen implementation. For tiny primitive-only fixes, verify the touched primitive still composes these foundations. Do not design or implement individual screens until these foundations are present, wired through the real app entrypoints, and used by shared primitives.

- Fonts: install or use the host project's Geist asset setup. In Next.js, prefer the `geist` package and wire Geist Sans and Geist Mono variables in the root layout. Add Geist Pixel variables from `geist/font/pixel` only when a constrained display/brand accent is actually used. Apply Sans to the app root, reserve Mono for code, command text, shortcuts, technical identifiers, versions, environment variables, commit hashes, terminal/log output, and official mono classes, and keep Pixel out of ordinary product UI text. Numeric product data should use Sans label/copy utilities with tabular numeric treatment unless the consulted Typography page or existing Geist-mapped primitive maps that context to Mono.
- Tokens: define a single semantic token layer for backgrounds, foregrounds, muted text, borders, rings, destructive, success, warning, link, and info states. Optional accent aliases must resolve to a specific official Geist role or scale for focus, selection, link, or status. Map these tokens to Geist Background 1/2, component backgrounds 1-3, borders 4-6, high-contrast backgrounds 7-8, and text/icons 9-10.
- Typography: define or map reusable Geist typography utilities before writing screen copy styles: `text-heading-*`, `text-button-*`, `text-label-*`, `text-copy-*`, mono variants, and tabular numeric treatment. Screen files should not rely on ad hoc `text-sm`, `font-bold`, arbitrary line heights, or arbitrary tracking for primary hierarchy.
- Materials and radii: define shared material utilities or variants for `material-base`, `material-small`, `material-medium`, `material-large`, `material-tooltip`, `material-menu`, `material-modal`, and `material-fullscreen`. Define radius tokens/utilities for the Geist scale: 6px, 12px, and 16px. Do not use arbitrary large radii or one-off `rounded-*` choices in screen files.
- Focus rings: define one app-wide focus-visible treatment using the project semantic `ring` token mapped to a specific consulted Geist color role/scale. Treat the focus-ring behavior as an accessibility implementation rule verified separately through the Vercel Web Interface Guidelines, not as a Geist foundation token or source-of-truth rule. All interactive primitives must consume that treatment instead of inventing per-component outline, box-shadow, or ring styles.
- App shell: create or verify a shared app shell before screen work: root background, content gutters, navigation/header/sidebar structure when needed, dividers, max-width behavior, mobile behavior, and one clear primary action zone per view.
- Component primitives: create or verify the shared primitives needed by the work before composing screens. At minimum, route new UI through Geist-styled primitives for Button/IconButton, Input/Textarea, Select/Combobox when needed, Checkbox/Radio/Switch, Tabs, Modal/Sheet/Drawer, Menu/Tooltip, Toast/Feedback, Table/List, Empty/Error/Loading/Skeleton states, Surface/Material, and AppShell. Composition primitives are not official Geist components: IconButton must follow Button icon-only/svg-only guidance; List must map to Table, Entity, Description, Scroller, or Show More; Surface/Panel/AppShell must be built from Grid, Material, Menu/Tabs/Drawer/Sheet as applicable and pass the custom-pattern gate.
- State system: create or verify shared state variants/primitives before screen work for hover, active/pressed, selected/current, disabled, loading, empty, error, validation, focus-visible, and reduced-motion behavior. Screen files must consume these shared state APIs/classes instead of defining state styles locally.
- Screen composition rule: screens must compose the shared Geist tokens, typography, materials, focus rings, app shell, primitives, and state system. Do not create one-off screen-local visual systems unless the existing project architecture explicitly requires that location for the shared implementation.

## Geist Essence

The target feel is a restrained developer-tool interface:

- Neutral-first, high-contrast, accessible surfaces.
- Typography and spacing do most of the hierarchy work.
- Color is functional: status, focus, selection, destructive state, success, warning, links, and sparse brand accents.
- Layouts are orderly, dense where useful, and easy to scan repeatedly.
- Borders are hairline structure, not decoration.
- Motion is short, subtle, and state-driven.
- Empty space is intentional, not a substitute for missing product thinking.
- Copy is concrete and operational. Avoid marketing fluff inside product UI.

## Layout Rules

- Product apps should open directly into the usable workspace, not a marketing landing page.
- Dashboards should favor a clear primary workflow, quiet secondary controls, and compact information density.
- Existing app shells should keep one canonical navigation/footer/contact model. If a sticky or primary navigation already owns section links, do not duplicate the same link set in the footer. If a contact section already owns contact actions, do not repeat the same contact/social list in the footer unless the user explicitly asks for redundant footer navigation.
- Use full-width page bands or unframed layouts for sections. Do not put page sections inside decorative cards.
- Cards are for repeated items, modals, individual panels, and genuine framed tools. Do not nest cards inside cards.
- Use a predictable grid and stable dimensions for toolbars, boards, tables, counters, and repeated tiles.
- Treat "grid" as layout first for ordinary responsive UI: use CSS grid/flex,
  columns, rows, borders, and spacing to organize content. When the user asks
  for a Vercel.com-like grid, Vercel grid art, visible guide lines, cells, a
  full-page Grid treatment, or supplies a design that clearly contains those
  elements, implement an intentional Geist/Grid-style cell-and-guide surface
  instead of stripping the lines out. Visible grid treatments should be content
  surfaces with real cells, aligned borders, clipping/solid cells where useful,
  and responsive row/column behavior. Do not add accidental graph-paper,
  blueprint, or repeating-gradient decoration behind unrelated UI when the
  request is only for a clean or ordinary responsive layout.
- Local implementation heuristic, not `Docs Evidence`: when the project lacks an official spacing token source, use a restrained 4px-compatible rhythm such as 8, 12, 16, 20, 24, 32, 48, and 64 to preserve compact Geist composition. If official or project Geist-mapped spacing tokens exist, use those instead.
- Keep page gutters responsive: about 16px on mobile, 24px on tablet, 32px on desktop, with a sensible max-width for reading surfaces.
- Do not let hover, loading, selected, or error states resize components or shift layout.
- Tables and logs should use tight rows, clear column alignment, sticky headers when useful, and monospaced numerals/IDs.
- Verify layout at mobile, laptop, desktop, and ultra-wide viewport widths. Zooming out may supplement visual review, but it is never a substitute for recorded ultra-wide viewport screenshot evidence when Browser or Playwright can set the viewport.
- Respect safe-area insets with `env(safe-area-inset-*)` for fixed headers, bottom bars, drawers, sheets, and full-screen surfaces.
- Test with scrollbars always visible when possible. Fix unwanted horizontal or nested scrollbars; only render scrollbars that serve an intentional workflow.
- Prefer flex/grid/intrinsic CSS layout over JavaScript measurement. Avoid layout thrash by letting CSS handle flow, wrapping, and alignment.
- Align deliberately to a grid, baseline, edge, or optical center. Allow deliberate +/-1px optical alignment when perception beats geometry, and balance text/icon lockups for contrast, weight, size, and spacing.

## Color Rules

Follow the Geist color model:

- Background 1: default page and component background.
- Background 2: secondary background, used sparingly for subtle separation.
- Colors 1-3: component backgrounds. Map Color 1/2/3 to default/hover/active only when the component owns a component background. If the rest state is Background 1, use Color 1 for hover and Color 2 for active. Small badges may use Color 2 or Color 3 as their background.
- Colors 4-6: borders: default, hover, active.
- Colors 7-8: high-contrast component backgrounds and hover states.
- Colors 9-10: accessible secondary and primary text/icons.

Implementation guidance:

- When defining custom CSS/Tailwind tokens, prefer raw Geist scale variables first: Background 1/2 plus the applicable official Color 1-10 steps for each used scale. If the project already exposes official Geist/Core tokens or generated CSS variables, map semantic aliases to those without duplicating the raw layer. Semantic names are local aliases, not Geist source tokens.
- Use current Colors page values for Background 1/2, Colors 4-6 for borders, and Colors 9-10 for text/icons; do not choose arbitrary near-neutral values unless mapping an existing project token to those official roles.
- In dark mode, map to the same official Geist roles rather than inventing a separate near-black palette.
- Use alpha grays for subtle hover/focus layers when the project token system supports them.
- Status colors are allowed only for status: red/destructive, amber/warning, green/success, blue/info/link, teal/purple/pink only when the product meaning requires them. `accent` must alias a specific official Geist role or scale for focus, selection, link, or status; default/primary actions must follow the consulted Button/component page rather than a broad accent token. Never create decorative accent colors.
- For charts and status-heavy views, use redundant cues such as labels, shape, texture, icon, or position alongside color. Use color-blind-friendly palettes and verify contrast with APCA where available.
- Hover, active, and focus states should increase contrast over the rest state instead of becoming softer or less legible.
- Do not build a one-note purple/blue gradient interface.
- Do not use decorative gradient orbs, bokeh blobs, glassy rainbow panels, or loud shadows.
- Do not make color carry meaning alone; pair it with text, icon, shape, or state.

## Typography Rules

Use the full Geist type family when available:

- Geist Sans: headings, body text, navigation, buttons, forms, tables, dialogs.
- Geist Mono: code, command text, shortcuts, IDs, versions, environment variables, commit hashes, terminal/log output, and inline technical tokens. Metrics, prices, timestamps, and numeric columns should use the official label/copy typography utility with tabular numeric treatment first; use Mono only when the consulted Typography page or an existing Geist-mapped primitive maps that context to a mono class.
- Geist Pixel: local restraint, not Vercel Font source-of-truth usage guidance. Use it sparingly for one intentional display/brand moment such as a wordmark, small campaign lockup, highly constrained hero accent, banner accent, or constrained dashboard/product accent. Never use it for body copy, dense tables, forms, settings copy, navigation, long headings, metric grids, or ordinary dashboard/product text unless current official Pixel or Font guidance explicitly supports that exact use.
- In Next.js with the `geist` package, import Pixel variants from `geist/font/pixel`: `GeistPixelSquare`, `GeistPixelGrid`, `GeistPixelCircle`, `GeistPixelTriangle`, and `GeistPixelLine`.

Use the official Geist type categories:

- Headings introduce pages or sections.
- Buttons use button-specific text styles only inside button components.
- Labels are single-line UI text with generous enough line-height to align with icons.
- Copy is for multiline text.

Use official Geist Tailwind typography classes first. If the project lacks these classes, add or map them through the project's Tailwind/theme/CSS token layer before building new UI. Raw font-size, line-height, letter-spacing, and font-weight values may appear only inside named Geist typography utility definitions, using installed Geist/Core CSS values or computed official class values gathered during the current docs pass.

The following typography names are implementation mappings only. They do not satisfy the docs gate and must not be used as proof unless the official Typography page was opened, read, and influenced the implementation in the current turn.

- Headings: `text-heading-72`, `text-heading-64`, `text-heading-56`, `text-heading-48`, `text-heading-40`, `text-heading-32`, `text-heading-24`, `text-heading-20`, `text-heading-16`, `text-heading-14`.
- Buttons: `text-button-16`, `text-button-14`, `text-button-12`. Use these only inside button components.
- Labels: `text-label-20`, `text-label-18`, `text-label-16`, `text-label-14`, `text-label-14-mono`, `text-label-13`, `text-label-13-mono`, `text-label-12`, `text-label-12-mono`.
- Copy: `text-copy-24`, `text-copy-20`, `text-copy-18`, `text-copy-16`, `text-copy-14`, `text-copy-13`, `text-copy-13-mono`.
- Use descendant `<strong>` inside a Geist typography class for Strong treatment.
- Use Subtle modifiers only through the project's official Geist class/token implementation. Do not fake subtle text by making it unreadably gray.
- Use `tabular-nums` for metrics, timestamps, table numbers, counters, and numeric label/copy styles; use Geist Mono only for official mono classes or technical/code-like content.

Official usage guidance:

- `text-heading-72`: marketing heroes.
- `text-heading-32`: marketing subheadings, paragraphs, and dashboard headings.
- `text-button-14`: default button text.
- `text-button-12`: tiny button inside an input field.
- `text-label-14`: most common label/menu text style.
- `text-label-13`: secondary line next to labels; use tabular alignment when conveying numbers.
- `text-label-12`: tertiary text in busy views, Show More, comments, and calendar capitals.
- `text-copy-16`: simpler larger views such as modals.
- `text-copy-14`: most common copy style.
- `text-copy-13`: secondary copy or dense views.
- `text-copy-13-mono`: inline code mentions.

Fallback when official classes are absent:

- Define named `text-heading-*`, `text-button-*`, `text-label-*`, and `text-copy-*` mapped equivalents before writing screen styles.
- The mapped equivalents must preserve the official category, size, line-height, letter-spacing, and weight relationships from the Typography page, installed Geist/Core CSS, or computed values from the current official docs pass.
- Raw sizes are allowed only inside those shared typography utility definitions. Route, page, screen, and feature files must consume the named utilities and must not use broad ad hoc heading/body/button size ranges as proof of Geist typography.

Typography constraints:

- Do not default an entire interface to `text-base`.
- Do not make every heading bold. Prefer medium/semi-bold and hierarchy through size, spacing, and placement.
- Do not use negative letter spacing globally. Apply tight tracking only to large display/headline text if the existing system does.
- Keep long-form prose readable; do not use Geist Mono for paragraphs.

## App-Wide Setup

This section is an implementation checklist for the mandatory Foundation Gate; it cannot narrow, delay, or exempt any Foundation Gate requirement.

For any task that creates or materially changes rendered UI, create or verify the shared Geist foundation before styling individual screens, routes, pages, or feature components.

- Fonts: use Geist Sans and Geist Mono through the host project's font setup. In Next.js, prefer the `geist` package with `geist/font/sans` and `geist/font/mono`; add `geist/font/pixel` only when a constrained display/brand accent is actually used.
- Root layout: apply Geist Sans as the default UI font, expose Geist Mono for code, command text, shortcuts, technical identifiers, versions, environment variables, commit hashes, terminal/log output, and official mono classes, and expose Geist Pixel variables only for constrained display accents. Numeric product data should stay in Sans label/copy utilities with tabular numeric treatment unless the consulted Typography page or an existing Geist-mapped primitive maps that context to Mono.
- Typography: define or map the official `text-heading-*`, `text-button-*`, `text-label-*`, and `text-copy-*` classes. New components and screens must use these classes or mapped equivalents; raw `text-sm`, `font-bold`, arbitrary line-height, and arbitrary tracking are allowed only inside shared token/utility definitions or inside third-party/generated code that cannot consume project utilities. The final response must name the file, constraint, and why a mapped utility was impossible.
- Colors: define semantic tokens for `background`, `foreground`, `muted-foreground`, `border`, `ring`, `accent`, `link`, `info`, `destructive`, `success`, and `warning`, mapped to Background 1/2, component backgrounds 1-3, borders 4-6, high-contrast backgrounds 7-8, and text/icons 9-10. Components should consume semantic tokens, not hard-coded grays.
- Materials: define or map `material-base`, `material-small`, `material-medium`, `material-large`, `material-tooltip`, `material-menu`, `material-modal`, and `material-fullscreen` when the project does not already have them. Also define radius tokens/utilities for 6px, 12px, and 16px, and require screen files to consume those tokens rather than one-off `rounded-*` classes.
- Primitives: create or adapt shared primitives for Button/IconButton, Input/Textarea, Select/Combobox when needed, Checkbox/Radio/Switch, Tabs, Modal/Sheet/Drawer, Menu/Tooltip, Toast/Feedback, Table/List, Empty/Error/Loading/Skeleton states, Surface/Material, and AppShell before composing multiple screens. App shells, panels, and surfaces use CSS grid/flex plus Geist tokens/materials by default; consult Geist Grid when the user asks for Vercel.com-like visible guide/cell layout, a supplied design clearly includes it, or the Grid component itself is the intended UI surface. Panels/surfaces still inherit Context Card, Relative Time Card, Project Banner, Entity, Description, or Table Best Practices as applicable to the content.
- Borders and focus: define one shared focus-visible utility/variant using the project semantic `ring` token mapped to a specific consulted Geist color role/scale, then verify the focus behavior separately through the Vercel Web Interface Guidelines accessibility checks. Wire that utility into every interactive primitive and prohibit screen-local outline, box-shadow, or ring definitions.
- App shell: use Geist foundations and Vercel Web Interface Guidelines for root background, content gutters, header/sidebar/navigation structure when needed, restrained dividers, predictable max-width behavior, mobile behavior, one obvious primary action zone per view, skip-to-content, valid heading hierarchy, and context-specific `<title>`.
- State system: provide consistent hover, active/pressed, selected/current, disabled, loading, empty, error, validation, focus-visible, and reduced-motion states across the app.
- Dark mode: support dark mode only when the app already has it or the user asks for it; if implemented, map the same Geist roles rather than inventing a second palette.
- Existing projects: adapt to the existing architecture and component library, but route all new styling through Geist tokens and classes. This adaptation cannot bypass the Foundation Gate.

## Materials Rules

The following material names are implementation mappings only. They do not satisfy the docs gate and must not be used as proof unless the official Materials page was opened, read, and influenced the implementation in the current turn.

Use official Geist Material presets first when the project has them. Materials are presets for radii, fills, strokes, and shadows.

Surface materials sit on the page:

- `material-base`: everyday surface. Radius 6px.
- `material-small`: slightly raised surface. Radius 6px.
- `material-medium`: further raised surface. Radius 12px.
- `material-large`: further raised surface. Radius 12px.

Floating materials sit above the page:

- `material-tooltip`: lightest shadow. Corner 6px. Tooltips are the only floating element with a triangular stem.
- `material-menu`: lifted menu surface. Radius 12px.
- `material-modal`: further lifted modal surface. Radius 12px.
- `material-fullscreen`: biggest lift. Radius 16px.

Material constraints:

- Do not invent larger radii for a softer look. Existing token names may differ only if their resolved values preserve the official 6px, 12px, and 16px material radii for the mapped preset; otherwise strict Geist compliance is blocked.
- Do not use heavy decorative shadows. Elevation should clarify layering, not create a floating-card aesthetic.
- Use the component-specific material level: menus get menu material, modals get modal material, and ordinary page cards/panels use base/small/medium/large surface materials.
- Do not nest multiple elevated materials unless the interaction genuinely requires layered floating UI.

## Vercel Design Details

Apply the Design section of `https://vercel.com/design/guidelines` when the UI uses shadows, borders, nested containers, non-neutral surfaces, text transforms, charts, masks, fades, or browser chrome:

- If shadows are used, layer ambient and direct-light shadows and pair them with crisp borders for edge clarity.
- Nested radii must be concentric: child radius is less than or equal to parent radius and curves align.
- On non-neutral backgrounds, tint borders, shadows, and text toward the same hue instead of mixing arbitrary hues.
- Avoid scaling text nodes directly; animate a wrapper instead, and use GPU promotion only when text anti-aliasing artifacts persist.
- Avoid gradient banding in masks and fades, especially when fading content to dark colors.
- Charts must use color-blind-friendly palettes, and contrast should be checked with APCA where available.

## Implementation Rules

- Use existing project tokens and primitives only after mapping or adapting them to the required Geist foundation roles. If they cannot express Geist fonts, tokens, typography utilities, materials/radii, focus rings, states, and app shell composition, establish those shared layers first.
- If tokens are missing, define a small semantic token layer in CSS variables before styling components.
- Keep component APIs explicit and small. Avoid boolean prop proliferation; use explicit variants or composition.
- Do not add mock/sample data to make UI look filled. Use real data pathways or honest empty/loading states.

## Tailwind Guidance

Use Tailwind through the host project's setup only.

- When defining custom CSS/Tailwind variables, prefer raw Geist scale roles first, then derive semantic aliases such as `background`, `foreground`, `muted-foreground`, `border`, `ring`, `link`, `info`, `destructive`, `success`, and `warning`. If the project already exposes official Geist/Core tokens or generated CSS variables, map semantic aliases to those without duplicating the raw layer. If an `accent` alias exists, it must resolve to a specific official Geist role/scale for focus, selection, link, or status, never to a decorative palette.
- Keep class lists readable and consistent with existing project conventions.
- Prefer semantic component classes or variants for repeated patterns.
- Arbitrary color, typography, radius, shadow, focus, ring, material, and state values may appear only inside shared token, utility, variant, or primitive definitions. Route, page, screen, and feature files must consume named tokens, utilities, variants, or primitives instead of one-off arbitrary values.
