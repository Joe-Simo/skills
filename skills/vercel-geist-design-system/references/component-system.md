## Geist Component Mapping

Before custom-building UI, check whether Geist already has the pattern. If it does, use the Geist reference as the behavioral and visual target, then implement it with the project's available primitives.

For every UI need, perform a docs-first mapping pass before designing or coding: identify the user intent, check the official Geist component list and the closest component page, then choose the official component, an official composition of multiple components, or a constrained custom composition. Do not start from generic SaaS, shadcn, Radix, Tailwind, or memory-derived patterns when a Geist component exists.

- Identity and object display: Avatar, Entity, Badge, Pill, Status Dot, Description.
- Actions and command surfaces: Button, Split Button, Toggle, Menu, Context Menu, Command Menu.
- Forms and selection: Input, Textarea, Checkbox, Radio, Switch, Select, Multi Select, Combobox, Choicebox, Slider, Calendar.
- Navigation, layout, and disclosure: Tabs, Pagination, Collapse, Drawer, Sheet, Modal, Grid, Show More, Scroller, Table.
- Feedback, help, and status: Toast, Feedback, Error, Note, Empty State, Progress, Spinner, Loading Dots, Skeleton, Tooltip.
- Developer and preview surfaces: Code Block, Snippet, Keyboard Input, Browser, Phone, MiddleTruncate, Relative Time Card, Context Card.
- Product, brand, and specialized surfaces: Project Banner, Gauge, Material, Book, Theme Switcher, Destructive Action Modal.
- Custom primitive aliases: IconButton -> Button; List -> Table, Entity, Description, Scroller, or Show More; Card/Panel/Surface -> Material, then Context Card, Relative Time Card, Project Banner, Entity, Description, or Table by content; AppShell -> CSS grid/flex plus Menu, Tabs, Drawer, Sheet, Button, Avatar, Badge, and Status Dot as used. Use Geist Grid only when visible cell/guide layout is intentionally part of the design. These aliases are not escape hatches; they inherit applicable Best Practices from every adjacent official component.
- Common library-name aliases: Dialog -> Modal; AlertDialog/ConfirmDialog -> Destructive Action Modal only for high-stakes destructive flows requiring deliberate typed confirmation, otherwise Modal for routine confirmations, unsaved-change prompts, and low-stakes confirmations; DropdownMenu -> Menu; ContextMenu -> Context Menu; Command/CommandDialog -> Command Menu; Accordion/Collapsible -> Collapse; DataTable -> Table; ToggleGroup/SegmentedControl -> Switch for 2-3 mutually exclusive same-surface options, Toggle only for a single boolean setting, Tabs for sibling views when tab semantics are intended, and Select when option count or label length exceeds Switch guidance; Popover/HoverCard -> the closest checked Geist component such as Menu, Tooltip, Context Card, Sheet, or Modal. These aliases inherit Best Practices and require `Docs Evidence` rows for each selected or rejected Geist page.
- If a needed pattern is not in Geist, first check adjacent official components that may cover the intent. Only then compose it from Geist foundations: color roles, typography classes, material presets, spacing, interaction rules, and accessible project primitives.
- If the project uses shadcn, Radix, or another component library, treat it as behavior/accessibility infrastructure only. Restyle and compose it through Geist tokens and component references.
- Do not add custom visual variants to Geist-mapped primitives unless the variant is a direct alias of an official Geist variant, state, or documented semantic status from the consulted component page. Project-specific visual variants such as `brand`, `premium`, `ghost`, `glass`, `soft`, `elevated`, `ai`, `accent`, or `marketing` are rejected or moved to composition unless the user explicitly confirms a non-Geist visual-system override. Any allowed alias must cite the component page Best Practices in `Docs Evidence`.
- For official compositions and constrained custom patterns, open every checked adjacent Geist component page and apply all applicable Best Practices. Deviate only when a Best Practice is technically impossible; document the checked component, the impossible constraint, and the closest preserved Geist behavior. Explicit product requests should be satisfied through the closest official Geist component/composition rather than by replacing component-specific behavior.
- Custom patterns must name the checked Geist alternatives, reuse existing project primitives, keep semantics and keyboard behavior equivalent to the closest native/ARIA pattern, use only Geist tokens/classes/materials, avoid new colors/radii/shadows/typography scales, and include loading, empty, error, disabled, focus-visible, and reduced-motion behavior when relevant.
- Current component-index reconciliation: open `https://vercel.com/geist/introduction`, compare every Components nav item against `official-reference-map.md` and the mapping buckets; if a live component is missing locally, use the official nav URL, map it to the closest bucket, and mention the skill drift in the final response.

## Component Documentation Contract

For every UI component that maps to Geist, open and read its official component page in the current turn before designing or coding that component. A component page counts as consulted only when the agent records an exact section/anchor, a short official quote, all applicable Best Practices when the page provides them, and any relevant When to use, Behavior, Content, or Accessibility constraints. For components actually implemented or restyled, at least one page-specific quoted rule from the official component page must affect the implementation and appear in `Docs Evidence`. The `not applicable` path is allowed only for adjacent components that were checked and rejected during custom-pattern mapping, and the final evidence must name the rejected component and why it did not fit. Preserve component-specific rules such as button/link separation, destructive modal focus behavior, input label/id requirements, empty-state CTA limits, table semantics, and exact label/copy conventions. Generic component styling, matching class names, or memory of Geist patterns is insufficient when the official page gives a more specific rule.

## Component Rules

All components must have:

- Default, hover, active/pressed, focus-visible, disabled, loading, and error states when relevant.
- Keyboard accessibility for all interactive controls.
- ARIA only when it improves semantic clarity; do not add redundant ARIA to native elements.
- Use native semantics first: button for actions, a/Link for navigation, label for controls, table for tabular data. Do not substitute div/button for navigational links. App shells need a skip-to-content link, valid heading hierarchy, and a context-specific `<title>`. Name icon-only controls, provide accurate accessible names, give images meaningful `alt`, set decorative images to `alt=""`, set `aria-hidden="true"` on decorative SVG/icons/media, announce async updates with polite aria-live where appropriate, and verify names/states in the accessibility tree.
- Visible focus rings that match the system and meet contrast needs. Use `:focus-visible` for focus rings and `:focus-within` for grouped/composite controls. On desktop screens with a single primary input, autofocus that input. Avoid mobile autofocus unless explicitly justified.
- Stable sizing across content, loading, and state changes.
- Icon alignment that does not distort row height or button height.

Component direction:

- Buttons: clear hierarchy. One primary action per surface. Secondary and tertiary actions should stay quiet. Destructive actions require confirmation or Undo with a safe window; irreversible destructive actions require confirmation.
- Inputs/Textareas: restrained borders, visible focus state, inline validation, associated labels, mobile input font-size >=16px, browser zoom left enabled, hydration-safe value/focus, paste allowed, no blocked typing, correct type/inputmode/name/autocomplete, selective spellcheck, explicit native select colors for Windows dark mode, and no oversized fields unless the task requires it.
- Forms: Enter submits when a text input is the only control or the last relevant control in a multi-control form; in `<textarea>`, Cmd/Ctrl+Enter submits and Enter inserts a newline. Every control has an associated label, clicking a label activates the control, submit remains enabled until submission starts, in-flight submission disables the submit control, shows progress, and uses an idempotency key when a mutation can repeat. Do not pre-disable submit to hide validation; submit incomplete forms to reveal validation, show errors next to fields, focus the first error on submit, warn before navigation when unsaved data could be lost, and preserve password-manager, autofill, OTP, paste, and text-replacement compatibility. Placeholders should signal emptiness with an ellipsis and use example values or patterns. Avoid password-manager triggers on non-auth fields with appropriate `name` and `autocomplete` values. Trim text-replacement trailing whitespace before validation errors are shown.
- Select/Combobox/Menus: keyboard-navigable, typeahead/search when data volume needs it, concise option labels.
- Tabs: use for peer views. Do not use tabs as decoration.
- Modals/Drawers/Sheets/Menus/Comboboxes: follow WAI-ARIA Authoring Patterns; set initial focus, trap or scope focus while open, restore focus to the trigger on close, support Escape, and verify the full flow by keyboard. Modal/drawer/sheet surfaces still need clear primary/secondary actions and escape/cancel behavior.
- Toasts/Feedback: concise, state-specific, dismissible when appropriate, and never a replacement for inline validation.
- Tables: compact, scannable, sortable/filterable when the workflow needs it, with empty/error/loading states.
- Code Blocks/Snippets: use Geist Mono, copy affordance, language/file label when useful, and clear line wrapping/overflow.
- Empty States: direct next action, no oversized illustration unless the product context needs it.
- Scroller: use for overflowing peer items on one axis; pick `vertical`, `horizontal`, or `free` based on real content. Use virtualization or `content-visibility` for large lists when the Web Interface Guidelines audit/prompt flags the list size or when profiling shows rendering cost; otherwise document the performance justification. Keep horizontal widths/gaps consistent, expose edge affordances, and give scroll buttons specific `aria-label`s such as `Scroll customer logos left`.
- Skeletons/Spinners/Loading Dots: use only while real data or work is pending; preserve final layout dimensions. Loading buttons keep the original label visible with a progress indicator. Local heuristic, not `Docs Evidence`: spinner/skeleton UI should avoid flicker with a short show delay and minimum visible duration unless the consulted component or project primitive defines exact timing.

## Iconography

Icon and asset decisions are source-gated: use Geist component pages for icon-bearing component behavior, Button for icon-only/svg-only button guidance, Brands for official marks, and Web Interface Guidelines for hit targets and accessible names. Do not claim official Geist icon compliance from an icon package name alone.

- For official logos, follow Brand Assets And Trademark Gate below.
- For generic UI symbols, use the project's existing icon library or installed assets unless a current non-redirecting official Geist icons source is consulted. While Geist resource/icon links redirect to Introduction, they do not authorize package-specific icon compliance claims. Size and align icons through the consulted Geist component, existing mapped primitive, or shared token. Do not introduce exact icon-size mandates unless a current official source or existing Geist-mapped primitive supplies them.
- Buttons that perform common tool actions may use familiar icons only when the control still has an accessible name and follows the consulted Button/icon-only guidance.
- Icon-only buttons and compact controls must satisfy Web Interface Guidelines hit-target rules: visual targets below 24px need expanded hit targets, and mobile targets are 44px.
- Local heuristic, not `Docs Evidence`: do not use decorative icon clusters to fill space.

## Brand Assets And Trademark Gate

Use official Vercel brand assets only for truthful references. Do not modify marks, make them more prominent than the app's own brand, use them in product/company names, or imply endorsement. Follow `https://vercel.com/geist/brands` for Vercel, Next.js, Turbo/Turborepo/Turbopack, v0, and AI SDK assets, logo imports, spacing, attribution, permitted usage, and misuse rules.

## Motion And Interaction

- Motion should clarify state changes: open/close, loading, selection, reordering, hover/focus, success/error.
- Do not invent universal timing ranges. Use durations from consulted component docs when they exist; otherwise keep motion minimal, interruptible, and purpose-driven without claiming numeric timing as `Docs Evidence`.
- Prefer CSS animations/transitions first, then Web Animations API, and avoid main-thread JavaScript-driven animation when possible.
- Prefer opacity/transform transitions. Avoid layout-thrashing animations. Never use `transition: all`; explicitly list intended properties such as `opacity` and `transform`.
- Choose easing based on what changes: size, distance, and trigger.
- Respect reduced motion preferences.
- Make animations cancelable/interruptible and input-driven. Set `transform-origin` to the perceived origin of the motion.
- For SVG transforms or animations, apply transforms to `<g>` wrappers and set `transform-box: fill-box` plus `transform-origin` to avoid browser origin bugs.
- Do not add scroll-triggered spectacle, parallax, bouncing, or decorative motion to product surfaces.

## Performance-Relevant UI Gate

Apply performance rules when a task touches rendered UI, animations, data views, media, forms, or interaction-heavy surfaces:

- Test or reason explicitly about iOS Low Power Mode and macOS Safari when those environments are available or the surface is user-facing.
- Profile perf-sensitive flows with CPU and network throttling when local tooling makes that feasible. Disable browser extensions that can distort measurement when using a real browser profile.
- Keep input loops cheap. Prefer uncontrolled inputs when appropriate, minimize re-renders, track re-renders with React DevTools or React Scan when available, and make controlled keystrokes fast enough for typing.
- Minimize layout work: batch reads/writes, avoid unnecessary reflows/repaints, avoid render-time layout reads such as `getBoundingClientRect`, `offsetHeight`, `offsetWidth`, and `scrollTop`, and do not use main-thread JavaScript for layout that CSS can handle.
- Treat mutation latency as product UI quality: `POST`, `PATCH`, and `DELETE` interactions should target completion under 500ms where the backend and network make that feasible, with optimistic UI, rollback, or Undo where appropriate.
- Virtualize large lists instead of rendering every row/card into the main layout. When using the official Web Interface Guidelines agent prompt or manual fallback, treat lists over 50 rendered items as requiring virtualization unless the current fetched prompt says otherwise; use `content-visibility: auto` only as a measured supplement, not a replacement for required virtualization.
- For images/media, set explicit dimensions or reserve space to avoid CLS. Preload only above-the-fold images and lazy-load the rest.
- Preload critical fonts, subset fonts to the scripts/code points and axes actually used, and avoid font loading that shifts layout.
- Use preconnect only for real external asset origins the project already needs.
- Move long main-thread work to Web Workers or existing background processing so interaction remains responsive.

## Copy Rules

- Product UI headings and buttons use Title Case: `Create Project`, `Deploy`, `Copy`, `Invite`, `Upgrade`, `Cancel`, `Delete`. Marketing pages use sentence case.
- Use active voice, second person, concise action-oriented language, consistent nouns, numerals for counts, `&` where it fits Vercel style, and the ellipsis character for follow-up/loading labels: `Rename…`, `Loading…`, `Saving…`.
- Avoid technical jargon unless the audience is explicitly developer/operator and the term is useful.
- Error messages should use positive, problem-solving language: say what failed, why when known, and what the user can do next. Buttons and links in error states must provide a clear exit or fix path.
- Empty states should describe the current absence and offer the next action.
- Use consistent placeholder and currency formats within a context. Format dates, times, numbers, delimiters, and currencies for the user's locale. Prefer curly quotes and use non-breaking spaces or word joiners for glued terms such as `10&nbsp;MB`, `⌘&nbsp;+&nbsp;K`, and `Vercel&nbsp;SDK`.
- Detect language from explicit user/account settings, the `Accept-Language` header, or `navigator.languages`; never infer language from IP or GPS location alone. Tidy widows, orphans, rag, and line breaks where the text-rendering stack supports it.
- Prefer inline help before tooltips. Tooltips are a last resort for supplemental explanation and must not hide required information.
- Anchored headings need `scroll-margin-top` so deep links do not hide headings under sticky headers.
- Mark brand names, product names, code tokens, and technical identifiers with `translate="no"` when browser translation could corrupt them.
- Layouts must handle short, average, and very long user-generated content without clipping, overlap, or broken controls.
- Local heuristic, not `Docs Evidence`: avoid redundant visible instructional text when labels and affordances already make a control clear.
- No screen may dead-end: empty, sparse, dense, permission, offline, and error screens must include a clear next step, retry, back path, request-access path, or contact/support path as appropriate.

## Vercel Web Interface Guidelines Overlay

Apply `https://vercel.com/design/guidelines` to every Geist-styled app:

- Keyboard works everywhere; focus is visible and managed; visual targets below 24px need expanded hit targets and mobile targets are 44px; mobile inputs use at least 16px text; never disable browser zoom or add zoom-limiting viewport settings such as `user-scalable=no`; every screen has empty, sparse, dense, loading, and error states.
- Persist view-affecting or workflow-affecting client state in the URL: search text, filters, sort, tabs, pagination, expanded panels, selected views, mode, drawer/detail selection, date ranges, comparison views, and any state stored in a client store that affects the visible view or workflow. Back/Forward and refresh must restore state and scroll position. Ephemeral focus, hover, in-flight request, and unsaved draft state may remain local.
- Use optimistic updates when success is likely, reconcile on server response, and on failure show an error plus rollback or Undo.
- Use tooltip timing that delays the first tooltip in a group and makes subsequent peer tooltips immediate.
- Set `overscroll-behavior: contain` intentionally for modals, drawers, and similar contained scroll regions.
- Clean drag interactions disable text selection and apply `inert` to prevent simultaneous hover/selection/interaction while dragging.
- Keyboard shortcuts are locale-aware and show platform-specific symbols.
- If any part of a control looks interactive, it must be interactive. Labels activate controls; checkbox/radio labels and controls share one generous target. Set `touch-action: manipulation` on controls and define `-webkit-tap-highlight-color` to match the design.
- No screen dead-ends; headings and buttons in product UI use Title Case; labels are specific; counts use numerals; numbers and units use a space/non-breaking space.
- Browser chrome is implementation work, not a final-only check. Official guideline: browser UI should match the page background, and the root should set the appropriate `color-scheme` for the active theme so browser/device UI keeps contrast. Geist implementation recommendation: align `<meta name="theme-color">` with the active Background 1 color; use media-specific meta tags when both light and dark OS themes are supported, and set `color-scheme` on the root according to the app's theme model.
