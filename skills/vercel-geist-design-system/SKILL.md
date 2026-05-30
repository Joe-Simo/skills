---
name: vercel-geist-design-system
description: >-
  Community skill for applying the Geist design system to Vercel-inspired UI
  across React, Next.js, Vite, Astro, Svelte, Vue, HTML/CSS, Tailwind, shadcn,
  and Radix surfaces. Use it for typography, spacing, color tokens, material
  treatment, component styling, app shells, dashboards, forms, tables, dialogs,
  empty/loading/error states, responsive layouts, and UI polish. This is a
  community-authored skill, not an official Vercel skill. Trigger on generic
  visual direction such as clean, modern, premium, beautiful, polished, SaaS,
  developer tool, product UI, app shell, navigation, data views, and marketing
  sections. Skip only when the user explicitly names a non-Geist final visual
  system/art direction as the final visual authority, supplies a non-Geist
  design artifact as the final visual authority, or asks for game/illustrative
  output where Geist UI is not the requested surface.
metadata:
  author:
    github: joe-simo
    x: "@joesimo"
    website: https://joesimo.com
  community: true
  official: false
  short-description: Default whole-app Vercel Geist for generic frontend/UI polish; library/framework mentions are not overrides; skip only explicit non-Geist final visual authority, supplied non-Geist design artifact as final authority, or game/illustration work where Geist UI is not the requested surface
  redirect-only-resources:
    - https://vercel.com/geist/icons
    - https://vercel.com/geist/geistcn-upgrade-guide
    - https://vercel.com/geist/geistcn-assets-guide
    - https://vercel.com/geist/geistcn-icons
    - https://vercel.com/geist/geistcn-logos
    - https://vercel.com/geist/guidelines
    - https://vercel.com/geist/changelog
  sources:
    - https://vercel.com/font
    - https://vercel.com/design/guidelines
    - https://vercel.com/geist/introduction
    - https://vercel.com/geist/colors
    - https://vercel.com/geist/typography
    - https://vercel.com/geist/materials
    - https://vercel.com/geist/brands
    - https://vercel.com/geist/brands#vercel
    - https://vercel.com/geist/brands#next-js
    - https://vercel.com/geist/brands#next-js-spelling
    - https://vercel.com/geist/brands#turbo
    - https://vercel.com/geist/brands#turborepo
    - https://vercel.com/geist/brands#turbopack
    - https://vercel.com/geist/brands#v0
    - https://vercel.com/geist/brands#ai-sdk
    - https://vercel.com/geist/brands#usage
    - https://vercel.com/geist/brands#misuse
    - https://vercel.com/geist/avatar
    - https://vercel.com/geist/badge
    - https://vercel.com/geist/book
    - https://vercel.com/geist/browser
    - https://vercel.com/geist/button
    - https://vercel.com/geist/calendar
    - https://vercel.com/geist/checkbox
    - https://vercel.com/geist/choicebox
    - https://vercel.com/geist/code-block
    - https://vercel.com/geist/collapse
    - https://vercel.com/geist/combobox
    - https://vercel.com/geist/command-menu
    - https://vercel.com/geist/context-card
    - https://vercel.com/geist/context-menu
    - https://vercel.com/geist/description
    - https://vercel.com/geist/destructive-action-modal
    - https://vercel.com/geist/drawer
    - https://vercel.com/geist/empty-state
    - https://vercel.com/geist/entity
    - https://vercel.com/geist/error
    - https://vercel.com/geist/feedback
    - https://vercel.com/geist/gauge
    - https://vercel.com/geist/grid
    - https://vercel.com/geist/input
    - https://vercel.com/geist/keyboard-input
    - https://vercel.com/geist/loading-dots
    - https://vercel.com/geist/material
    - https://vercel.com/geist/menu
    - https://vercel.com/geist/middle-truncate
    - https://vercel.com/geist/modal
    - https://vercel.com/geist/multi-select
    - https://vercel.com/geist/note
    - https://vercel.com/geist/pagination
    - https://vercel.com/geist/phone
    - https://vercel.com/geist/badge#pill
    - https://vercel.com/geist/progress
    - https://vercel.com/geist/project-banner
    - https://vercel.com/geist/radio
    - https://vercel.com/geist/relative-time-card
    - https://vercel.com/geist/scroller
    - https://vercel.com/geist/select
    - https://vercel.com/geist/sheet
    - https://vercel.com/geist/show-more
    - https://vercel.com/geist/skeleton
    - https://vercel.com/geist/slider
    - https://vercel.com/geist/snippet
    - https://vercel.com/geist/spinner
    - https://vercel.com/geist/split-button
    - https://vercel.com/geist/status-dot
    - https://vercel.com/geist/switch
    - https://vercel.com/geist/table
    - https://vercel.com/geist/tabs
    - https://vercel.com/geist/textarea
    - https://vercel.com/geist/theme-switcher
    - https://vercel.com/geist/toast
    - https://vercel.com/geist/toggle
    - https://vercel.com/geist/tooltip
---

# Vercel Geist Design System

Use this community-authored skill to make interfaces feel like they belong in Vercel's Geist design system: precise, calm, high-contrast, developer-focused, and production-ready. Treat the official Geist pages as the source of truth. This skill is not official Vercel guidance, and it is a style and implementation contract, not permission to copy Vercel product screens wholesale.

## Default App Policy

Use this skill as the default visual operating mode for any frontend app, site, page, component, dashboard, or UI polish work unless the user explicitly names a non-Geist final visual system/art direction as the final visual authority, supplies a non-Geist design artifact as the final visual authority, or asks for game/illustrative output where Geist UI is not the requested surface. Generic requests such as "clean", "modern", "premium", "beautiful", "polished", "SaaS", or "developer tool" still use Geist.

- Apply Geist style to the entire app surface: app shell, navigation, pages, forms, data views, dialogs, empty states, loading states, errors, toasts, command menus, and marketing sections.
- Scope is explicit. For greenfield apps, full redesigns, or broad UI polish requests, "entire app surface" means all routable app surfaces and shared states must be built or audited. For a narrow existing-project task, migrate the requested workflow and any shared primitives it touches; the final response must say `whole app not verified` unless every route/surface was audited.
- Do not create isolated Vercel-looking components inside an otherwise unrelated visual system. Establish shared tokens and primitives first, then build every new surface from them.
- If broader creative design guidance also applies, this skill owns the visual system whenever it is triggered. Treat generic frontend-design directives such as bold aesthetic direction, unforgettable visuals, unexpected layouts, distinctive font pairing, gradient meshes, dramatic shadows, textures, scroll-triggered spectacle, and surprising motion as disabled for Vercel/Geist work unless the user explicitly overrides Geist.
- If the user explicitly names another non-Geist final visual system/art direction as the final visual authority, such as Material, Apple, Linear, Stripe, Notion, a supplied non-Geist design artifact explicitly designated by the user as the final visual authority, or game/illustrative output where Geist UI is not the requested surface, respect that request and do not force Geist. Domain, industry, brand, product, company, API, integration, content subject, Tailwind, shadcn, Radix, or component library mentions are not visual-system overrides; for example, a Stripe webhook dashboard still uses Geist unless the user asks for Stripe-style visuals.
- Use the official Geist docs as the reference for every matching foundation or component before inventing a custom pattern.

## Reference-First Contract

The linked Geist docs are the design system. This skill is the enforcement layer that makes the agent use them.

- Do not rely only on this skill summary for design decisions when official docs are available.
- Before implementing any UI that creates or materially changes rendered output, consult the official Vercel Font page plus Geist Introduction, Colors, Typography, Materials, and Guidelines pages.
- Before implementing a specific UI pattern, consult the matching Geist component page from the reference map. A docs fallback is allowed only after attempting the required official URL in the current turn using every available browsing/docs tool.
- If current docs remain unavailable after those attempts, state the attempted URLs, tools, and exact failure mode. During blocked-doc fallback, local rules in this skill are advisory only; they cannot satisfy `Docs Evidence`, cannot support strict/docs-verified claims, and cannot be enforced as source-of-truth visual rules. If a needed decision has no current official source trace, mark that decision blocked and do not enforce an invented local visual rule. Shell/package-manager network failure alone is not enough if web/browser access exists. Do not use the fallback merely because the reference map, memory, or existing class names seem sufficient. When any required official page could not be read, label the result as `local Geist fallback, not docs-verified`; do not claim strict Geist, official Geist compliance, source-of-truth alignment, or Vercel Taste Gate passage for affected surfaces unless all required docs, screenshot checks, and interaction checks were completed.
- Do not treat using Geist fonts or class names as sufficient. The visual result must match the Geist/Vercel product language: restrained, precise, systematic, dense when useful, and visually coherent across every surface.
- If a generated design looks only generically "SaaS" or "clean" but not recognizably Vercel/Geist, revise it before finishing.
- The final UI should be judged as a product system, not a single screen: tokens, shell, navigation, controls, data displays, dialogs, feedback, and states must all belong together.

## Required Workflow

1. Identify the surface type: marketing hero, product dashboard, settings page, table/list view, command workflow, docs, or component library.
2. Check the existing project first: framework, Tailwind version, component library, icon library, font setup, theme tokens, and existing design-system conventions.
3. Open and read the required foundation pages for the surface, then complete the Foundation Gate before any screen-level work in this order: fonts, semantic color tokens, typography utilities, material/radius utilities, focus rings, shared app shell, component primitives, shared state system, and screen composition rules.
4. Do not edit route/page/screen-level styles until those shared layers are present in real app entrypoints, theme files, primitives, and app shell components.
5. Map every UI requirement to the closest Geist foundation or component, then open and read each matching official page before creating a custom pattern.
6. Prefer established packages and project primitives over custom implementations. For complex accessible primitives, use headless Radix primitives or existing shadcn code only as behavior/accessibility infrastructure after the Geist mapping pass; never import shadcn/Radix visual defaults, themes, or variants as design authority.
7. When implementing or composing any UI pattern, consult the matching official Geist page first. Use this skill's Official Reference Map only to locate the official URL, or as fallback after every available browsing/docs tool fails for the required official URLs in the current turn. In fallback mode, state that live docs were not checked, include exact failure modes, choose the closest official component conservatively, and treat local rules as advisory rather than enforceable source-of-truth requirements. When any required official page could not be read, label the result as `local Geist fallback, not docs-verified`; do not claim strict Geist, official Geist compliance, source-of-truth alignment, or Vercel Taste Gate passage for affected surfaces unless all required docs, screenshot checks, and interaction checks were completed.
8. Follow the host project's language, framework, package-management, and validation conventions.

## Official Source-Of-Truth Gate

For any task using this skill, current official Vercel docs are binding design input, not optional inspiration. Before visual implementation, open the relevant official pages for foundations, components, brand assets, and guidelines. Do not rely on memory, screenshots, generic SaaS heuristics, or Tailwind class names when an official Geist page covers the decision.

Required pages by decision type:

- Foundations: `https://vercel.com/geist/introduction`, `https://vercel.com/geist/colors`, `https://vercel.com/geist/typography`, `https://vercel.com/geist/materials`, `https://vercel.com/font`
- Guidelines: `https://vercel.com/design/guidelines`
- Brand/logo/assets: `https://vercel.com/geist/brands`
- Components: every concrete matching component URL from the reference map or live Geist component nav, such as `https://vercel.com/geist/button`

If a listed page redirects or cannot be loaded, do not treat it as source of truth. Use the closest accessible official Vercel page only as supplemental context and state the fallback. The original required URL remains `blocked` unless that exact official page or anchor was read; a substitute page cannot satisfy source-of-truth verification for the blocked required page.

For any task using this skill that creates, changes, critiques, specifies, or materially directs rendered UI, the final response must include a `Docs Evidence` table with one row for every required official page for the task, not merely pages claimed as consulted: all required foundation pages, the guidelines page, every mapped component page, and brand/assets pages when brand or logo decisions are made. Use columns: `official URL | status (consulted/blocked/not applicable) | exact official section/anchor | short exact quote or exact failure mode | implementation target | concrete decision/change | verification`. Keep any quote short, source-specific, and compliant with source quotation limits. Foundation and guidelines rows can be only `consulted` or `blocked`. Component rows split into required applied rows and adjacent rejected rows: rows for components actually implemented, restyled, or required by custom-pattern mapping can be only `consulted` or `blocked`; adjacent checked-and-rejected component rows can be `not applicable` only with a rejection reason and do not block strict claims by themselves. Brand/assets rows are required only when brand or logo decisions are made. A required applied page is blocked only if every available browsing/docs tool was tried in the current turn and the row names the tools and exact failures. A final answer may not claim Geist, strict Geist, docs-aligned Geist, source-of-truth verification, or Vercel Taste Gate passage if any required applied row is missing, blocked, lacks an exact section/anchor, or lacks a page-specific short quote that affected a concrete decision; if any required source is blocked, the only allowed claim for affected surfaces is `local Geist fallback, not docs-verified`. Strict Geist, docs-verified Geist, docs-aligned Geist, official Geist compliance, and source-of-truth alignment require complete `Docs Evidence` plus screenshot and interaction checks when those checks are possible. If screenshots or interaction checks are blocked, allowed wording is limited to `docs consulted; visual/interaction verification blocked`.

## Companion Skills Routing

These Skills.sh entries can help route work, but they are not design-system source of truth and they do not satisfy `Docs Evidence`. Official Vercel Geist docs, Vercel Font, Geist Brands, Geist component pages, and Vercel Web Interface Guidelines remain the only design-system authorities for strict Geist claims.

- `geist`: use `https://www.skills.sh/vercel-labs/vercel-plugin/geist` only for Geist Sans, Geist Mono, Geist Pixel, package installation, and font import guidance. Still verify `https://vercel.com/font` for strict Geist work.
- `geistdocs`: use `https://www.skills.sh/vercel-labs/vercel-plugin/geistdocs` only when the task is a documentation site, MDX/Fumadocs surface, or Geistdocs configuration. It does not replace the Geist foundation, component, brand, or Web Interface Guidelines checks for rendered docs UI.
- `web-design-guidelines`: use `https://www.skills.sh/vercel-labs/agent-skills/web-design-guidelines` as an audit helper when installed or accessible. It may route an audit against the latest Web Interface Guidelines, but the official guideline source remains `https://vercel.com/design/guidelines`, and findings must still be reconciled with Geist foundations/components. If the helper is unavailable, use the official page's Integrate with Agents fallback and fetch the raw command prompt directly from `https://raw.githubusercontent.com/vercel-labs/web-interface-guidelines/main/command.md` when network access allows. Skills.sh and raw GitHub prompts may only route or run an audit helper; they cannot supply design-system authority, cannot satisfy `Docs Evidence`, and cannot replace reading `https://vercel.com/design/guidelines` in the current turn.
- `geist-learning-lab`: use `https://www.skills.sh/vercel-labs/skill-geist-learning-labs/geist-learning-lab` only for interactive learning, tutorial, lab, or training products. Do not apply learning-loop, dark-first, or tutorial-specific rules to ordinary apps, dashboards, sites, or docs.
- `create-remotion-geist`: use `https://www.skills.sh/vercel-labs/skill-remotion-geist/create-remotion-geist` only for Remotion videos, motion graphics, or video-generation tasks. Do not apply video-specific dark-theme, spring-animation, or Remotion entrypoint rules to normal web UI.

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

## Official Reference Map

Use the non-redirecting official Vercel pages below as source-of-truth references. Redirect-only resources are listed only for routing/drift awareness and do not satisfy `Docs Evidence` unless they become non-redirecting official pages in the current turn.

- Main: `https://vercel.com/geist/introduction`
- Foundations: `https://vercel.com/font`, `https://vercel.com/geist/introduction`, `https://vercel.com/geist/colors`, `https://vercel.com/geist/typography`, `https://vercel.com/geist/materials`
- Guidelines: `https://vercel.com/design/guidelines`
- Resources: these current resource URLs redirect to `https://vercel.com/geist/introduction` and do not satisfy `Docs Evidence` unless they become non-redirecting official pages in the current turn: `https://vercel.com/geist/icons`, `https://vercel.com/geist/geistcn-upgrade-guide`, `https://vercel.com/geist/geistcn-assets-guide`, `https://vercel.com/geist/geistcn-icons`, `https://vercel.com/geist/geistcn-logos`, `https://vercel.com/geist/guidelines`, `https://vercel.com/geist/changelog`.
- Brands: `https://vercel.com/geist/brands`, `https://vercel.com/geist/brands#vercel`, `https://vercel.com/geist/brands#next-js`, `https://vercel.com/geist/brands#next-js-spelling`, `https://vercel.com/geist/brands#turbo`, `https://vercel.com/geist/brands#turborepo`, `https://vercel.com/geist/brands#turbopack`, `https://vercel.com/geist/brands#v0`, `https://vercel.com/geist/brands#ai-sdk`, `https://vercel.com/geist/brands#usage`, `https://vercel.com/geist/brands#misuse`
- Legacy/resource caution: do not rely on `https://vercel.com/geist/icons`, `https://vercel.com/geist/geistcn-upgrade-guide`, `https://vercel.com/geist/geistcn-assets-guide`, `https://vercel.com/geist/geistcn-icons`, `https://vercel.com/geist/geistcn-logos`, `https://vercel.com/geist/guidelines`, or `https://vercel.com/geist/changelog` as source-of-truth pages unless they resolve to non-redirecting official pages during the current task.
- Components:
  - Avatar: `https://vercel.com/geist/avatar`
  - Badge: `https://vercel.com/geist/badge`
  - Book: `https://vercel.com/geist/book`
  - Browser: `https://vercel.com/geist/browser`
  - Button: `https://vercel.com/geist/button`
  - Calendar: `https://vercel.com/geist/calendar`
  - Checkbox: `https://vercel.com/geist/checkbox`
  - Choicebox: `https://vercel.com/geist/choicebox`
  - Code Block: `https://vercel.com/geist/code-block`
  - Collapse: `https://vercel.com/geist/collapse`
  - Combobox: `https://vercel.com/geist/combobox`
  - Command Menu: `https://vercel.com/geist/command-menu`
  - Context Card: `https://vercel.com/geist/context-card`
  - Context Menu: `https://vercel.com/geist/context-menu`
  - Description: `https://vercel.com/geist/description`
  - Destructive Action Modal: `https://vercel.com/geist/destructive-action-modal`
  - Drawer: `https://vercel.com/geist/drawer`
  - Empty State: `https://vercel.com/geist/empty-state`
  - Entity: `https://vercel.com/geist/entity`
  - Error: `https://vercel.com/geist/error`
  - Feedback: `https://vercel.com/geist/feedback`
  - Gauge: `https://vercel.com/geist/gauge`
  - Grid: `https://vercel.com/geist/grid`
  - Input: `https://vercel.com/geist/input`
  - Keyboard Input: `https://vercel.com/geist/keyboard-input`
  - Loading Dots: `https://vercel.com/geist/loading-dots`
  - Material: `https://vercel.com/geist/material`
  - Menu: `https://vercel.com/geist/menu`
  - MiddleTruncate: `https://vercel.com/geist/middle-truncate`
  - Modal: `https://vercel.com/geist/modal`
  - Multi Select: `https://vercel.com/geist/multi-select`
  - Note: `https://vercel.com/geist/note`
  - Pagination: `https://vercel.com/geist/pagination`
  - Phone: `https://vercel.com/geist/phone`
  - Pill: `https://vercel.com/geist/badge#pill`
  - Progress: `https://vercel.com/geist/progress`
  - Project Banner: `https://vercel.com/geist/project-banner`
  - Radio: `https://vercel.com/geist/radio`
  - Relative Time Card: `https://vercel.com/geist/relative-time-card`
  - Scroller: `https://vercel.com/geist/scroller`
  - Select: `https://vercel.com/geist/select`
  - Sheet: `https://vercel.com/geist/sheet`
  - Show More: `https://vercel.com/geist/show-more`
  - Skeleton: `https://vercel.com/geist/skeleton`
  - Slider: `https://vercel.com/geist/slider`
  - Snippet: `https://vercel.com/geist/snippet`
  - Spinner: `https://vercel.com/geist/spinner`
  - Split Button: `https://vercel.com/geist/split-button`
  - Status Dot: `https://vercel.com/geist/status-dot`
  - Switch: `https://vercel.com/geist/switch`
  - Table: `https://vercel.com/geist/table`
  - Tabs: `https://vercel.com/geist/tabs`
  - Textarea: `https://vercel.com/geist/textarea`
  - Theme Switcher: `https://vercel.com/geist/theme-switcher`
  - Toast: `https://vercel.com/geist/toast`
  - Toggle: `https://vercel.com/geist/toggle`
  - Tooltip: `https://vercel.com/geist/tooltip`
- Components: open the concrete matching component URL from the map below, for example `https://vercel.com/geist/button`; never use a placeholder URL. Prefer the reference map or live nav URL for anchor/subcomponent entries such as Pill.

## Layout Rules

- Product apps should open directly into the usable workspace, not a marketing landing page.
- Dashboards should favor a clear primary workflow, quiet secondary controls, and compact information density.
- Use full-width page bands or unframed layouts for sections. Do not put page sections inside decorative cards.
- Cards are for repeated items, modals, individual panels, and genuine framed tools. Do not nest cards inside cards.
- Use a predictable grid and stable dimensions for toolbars, boards, tables, counters, and repeated tiles.
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
- Use tabular numeric treatment for numeric label styles. If the project lacks it, add a named tabular utility to the relevant Geist label/copy utility; use Geist Mono only for official mono classes or technical/code-like content.

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
- Use `tabular-nums` for metrics, timestamps, table numbers, and counters.

## App-Wide Setup

This section is an implementation checklist for the mandatory Foundation Gate; it cannot narrow, delay, or exempt any Foundation Gate requirement.

For any task that creates or materially changes rendered UI, create or verify the shared Geist foundation before styling individual screens, routes, pages, or feature components.

- Fonts: use Geist Sans and Geist Mono through the host project's font setup. In Next.js, prefer the `geist` package with `geist/font/sans` and `geist/font/mono`; add `geist/font/pixel` only when a constrained display/brand accent is actually used.
- Root layout: apply Geist Sans as the default UI font, expose Geist Mono for code, command text, shortcuts, technical identifiers, versions, environment variables, commit hashes, terminal/log output, and official mono classes, and expose Geist Pixel variables only for constrained display accents. Numeric product data should stay in Sans label/copy utilities with tabular numeric treatment unless the consulted Typography page or an existing Geist-mapped primitive maps that context to Mono.
- Typography: define or map the official `text-heading-*`, `text-button-*`, `text-label-*`, and `text-copy-*` classes. New components and screens must use these classes or mapped equivalents; raw `text-sm`, `font-bold`, arbitrary line-height, and arbitrary tracking are allowed only inside shared token/utility definitions or inside third-party/generated code that cannot consume project utilities. The final response must name the file, constraint, and why a mapped utility was impossible.
- Colors: define semantic tokens for `background`, `foreground`, `muted-foreground`, `border`, `ring`, `accent`, `link`, `info`, `destructive`, `success`, and `warning`, mapped to Background 1/2, component backgrounds 1-3, borders 4-6, high-contrast backgrounds 7-8, and text/icons 9-10. Components should consume semantic tokens, not hard-coded grays.
- Materials: define or map `material-base`, `material-small`, `material-medium`, `material-large`, `material-tooltip`, `material-menu`, `material-modal`, and `material-fullscreen` when the project does not already have them. Also define radius tokens/utilities for 6px, 12px, and 16px, and require screen files to consume those tokens rather than one-off `rounded-*` classes.
- Primitives: create or adapt shared primitives for Button/IconButton, Input/Textarea, Select/Combobox when needed, Checkbox/Radio/Switch, Tabs, Modal/Sheet/Drawer, Menu/Tooltip, Toast/Feedback, Table/List, Empty/Error/Loading/Skeleton states, Surface/Material, and AppShell before composing multiple screens. App shells, panels, and surfaces use CSS grid/flex plus Geist tokens/materials by default; consult Geist Grid only when a visible guide/cell layout is intentionally part of the design. Panels/surfaces still inherit Context Card, Relative Time Card, Project Banner, Entity, Description, or Table Best Practices as applicable to the content.
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
- Current component-index reconciliation: open `https://vercel.com/geist/introduction`, compare every Components nav item against the body reference map, frontmatter source list, and mapping buckets; if a live component is missing locally, use the official nav URL, map it to the closest bucket, and mention the skill drift in the final response.

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

- Use official logos only for truthful brand references after consulting Geist Brands. Do not imply Vercel, Next.js, Turbo, or v0 endorsement.
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

## Anti-Patterns And Failure Modes

Geist is a restraint-first production style. When this skill conflicts with generic `frontend-design` guidance, this section wins. Do not apply instructions to be bold, unforgettable, maximal, experimental, surprising, ornamental, or visually striking unless the user explicitly asks for that and confirms it should override Geist. For Vercel/Geist work, differentiation comes from product clarity, precise typography, consistent tokens, and real workflow polish.

This section separates official-source checks from local Vercel/Geist taste heuristics. Official-source checks are enforceable only through the cited Geist foundation/component/brand pages or Web Interface Guidelines and can support `Docs Evidence`. Local taste heuristics are red flags for generic SaaS or template output; they do not satisfy `Docs Evidence` by themselves and must lead back to official docs before making strict Geist claims.

Reject or revise these failure modes before finishing:

- Local heuristic: generic AI SaaS visual language such as giant "accelerate/build/automate" heroes, gradient headlines, glowing blobs/orbs, glass panels, noise overlays, floating feature pills, and fake customer/logo bands.
- Local heuristic: decorative gradients, purple-blue sweeps, rainbow meshes, radial glow backgrounds, bokeh, aurora effects, spotlight blobs, or background effects that are not required by product meaning. Official check: any retained color/motion/material treatment must be justified by Colors, Materials, Animations, or Content evidence.
- Official-source check: arbitrary accent colors, multi-hue dashboards, invented dark-mode palettes, or colors chosen for mood rather than official color roles and semantic product meaning violate the consulted Colors evidence.
- Local restraint, not `Docs Evidence`: non-Geist typography such as expressive display fonts, font pairing experiments, Inter/Roboto/Space Grotesk swaps, global system-font fallbacks used as a design choice, or Geist Pixel outside a constrained display accent.
- Official-source check: reject radii that violate the consulted Materials or component page. Component-specific rounded/pill variants are allowed only when the relevant official component page documents them and the usage matches that context.
- Official-source check: composition fails only when page sections, cards inside cards, metric/list/form blocks, or app shell panels violate consulted Material, component, layout, or guideline evidence. Local heuristic: card-first or card-in-card template composition is a red flag unless tied back to official docs and user scope before strict claims.
- Local heuristic: fake product substance such as mock/sample data, fake charts, fake users, fake notifications, imaginary integrations, placeholder metrics, or seeded examples used to make the UI look busy. Use the real data path, honest empty/loading/error states, or clearly user-provided content.
- Local heuristic: marketing instead of workflow, including landing pages where an app should start, oversized hero before the usable surface, vague value props in operational screens, or "AI-powered" copy that does not describe a concrete capability. Confirm through the user's scope and Content evidence before treating it as a strict failure.
- Official-source check: animation must clarify cause/effect or add deliberate delight, respect reduced motion, avoid `transition: all`, stay interruptible/input-driven, and use CSS/compositor-friendly properties when possible. Local heuristic: avoid scroll reveals, parallax, bounce, animated gradients, cursor effects, celebratory effects, or hover surprises in ordinary product surfaces unless the user explicitly asks and official motion checks still pass.
- Local heuristic: layout spectacle such as asymmetry, overlap, diagonals, broken grids, oversized negative space, or edge-to-edge compositions that reduce scan speed in product UI.
- Local heuristic: control overload where toolbars and sidebars expose many actions before the primary workflow is obvious; group or defer advanced controls and verify with interaction/content evidence.
- Official-source check: low-contrast softness such as gray-on-gray text, subtle borders that disappear, muted controls without visible affordance, or hierarchy that relies on opacity alone violates Colors, Design, or Accessibility evidence.
- Official-source check: inconsistent primitives such as one-off colors, radii, typography classes, shadows, button sizes, focus rings, or state styles fail when they bypass consulted Geist foundations/components.
- Official-source check: brand misuse, including Vercel/Next/Turbo/v0 logos or wording that implies endorsement, affiliation, or product identity when the app is not actually that brand, violates Geist Brands evidence.

Failure handling:

- If a design starts to look like a generic AI startup template, stop and simplify: remove decorative background effects, collapse competing CTAs, reduce color to neutral plus semantic status, and put the real workflow in the first viewport.
- If the result depends on fake data to look complete, do not ship it. Wire real data, show an honest empty state, or ask the user for real content.
- If the existing project has a different visual system and the user has not made it the final visual authority, migrate or adapt the whole touched app or requested surface to Geist through shared tokens and primitives. State a blocker only when an explicit non-Geist authority or hard scope constraint makes coherent whole-surface Geist migration impossible.
- If the user asks for "more creative" without explicitly overriding Geist, increase polish through alignment, density, copy, state coverage, and interaction clarity, not through gradients, ornamental assets, or random colors.

## Vercel Taste Gate

This is a mandatory visual quality gate for any frontend task using this skill. The work is not done until evidence shows the app or verified scope passes a Vercel/Geist audit. Do not finish from code inspection alone when a local app can run.

Required audit loop when the app/code can be exercised; capture screenshots whenever a local page can run:

1. Run the local app or page through the project's normal development command and record the command plus URL.
2. Perform Scope Discovery before screenshots: inspect framework route files/config, navigation/link usage, sitemap or build route output when available, and real app entrypoints. Include Storybook/examples only when they are real app surfaces. Record inaccessible, auth-gated, environment-gated, or dynamic routes with concrete blocker reasons. Create a route/surface/state inventory before screenshots: `route/surface | discovery source | required states | mobile screenshot | laptop screenshot | desktop screenshot | ultra-wide screenshot | interaction audit | status`. For greenfield/full redesign/broad polish work, every discovered routable surface and required shared state must appear in the inventory; whole-app claims fail if any row is missing or incomplete.
3. If the app runs, attempt Browser or Playwright mobile, laptop, desktop, and ultra-wide screenshots for each inventory row. Include the first viewport and any changed states such as menus, dialogs, empty states, loading states, errors, or dense data views. Record the command, URL, viewport sizes, screenshot paths, and state. Valid screenshot blockers are limited to app cannot build/run, missing auth or environment values, browser/screenshot tool unavailable after a named attempt, or route unreachable after the discovery source was checked. If screenshots are possible and not captured, do not claim the Vercel Taste Gate passed.
4. Run an interaction audit for every changed flow using an applicability matrix: `check | pass/fail/N/A | reason/evidence`. Cover keyboard-only operation, visible `:focus-visible`/`:focus-within`, overlay initial/trapped/restored focus, Escape/Enter/Cmd/Ctrl+Enter behavior, label activation, desktop >=24px and mobile >=44px targets, URL state plus Back/Forward/refresh/scroll restoration, optimistic update rollback/Undo, tooltip timing, intentional `overscroll-behavior`, clean drag behavior, locale-aware shortcuts, browser `theme-color`/`color-scheme`, and accessibility tree names/states/hidden decoration. Applicability triggers are mandatory: overlays require focus checks; mutations require optimistic/rollback or explicit non-applicability; tooltips require timing checks when present; filters, tabs, search, pagination, expanded panels, selected views, and any visible workflow state require URL-state checks; drag/reorder features require drag checks; icon-only controls require accessibility-tree verification. Conditional checks may be `N/A` only with a specific reason tied to absent UI/behavior. Revise failures before judging screenshots.
5. Compare the rendered UI against Geist foundations and relevant Geist components from the official reference map.
6. Deterministically check for the official Web Interface Guidelines review path. In Codex, use an installed repo command or slash command only if the current agent actually supports it and a concrete command, file, or documented invocation is present. Otherwise, if network access allows, fetch and use the raw command prompt from `https://raw.githubusercontent.com/vercel-labs/web-interface-guidelines/main/command.md` for a manual audit. Record the exact command/file/path or raw URL used. Run the installer only with explicit user or project opt-in and record the reason. Skills.sh and raw GitHub prompts may only route or run an audit helper; they cannot supply design-system authority, cannot satisfy `Docs Evidence`, and cannot replace reading `https://vercel.com/design/guidelines` in the current turn. If none can be run, record the exact blocker and continue with the manual guidelines audit.
7. Identify every place where the UI fails the evidence-backed pass criteria or trips local generic-SaaS heuristics.
8. Revise the implementation, then inspect fresh screenshots and rerun the interaction audit.
9. Repeat until the screenshots and interaction audit pass every rule below.

Pass criteria:

- Route/surface/state inventory is complete for the verified scope, with discovery source plus mobile, laptop, desktop, and ultra-wide screenshot evidence or valid recorded blockers for every row.
- Foundation evidence is visible in implementation: Geist Sans/Mono usage, Geist Pixel only when a constrained display accent is intentionally used and otherwise verified absent, Colors roles, Typography utilities, Materials/radii, focus rings, app shell, and shared state primitives are mapped in real files and used by changed screens.
- Component evidence is visible in implementation: every UI pattern that maps to Geist has a matching component page, exact section/quote evidence, applicable Best Practices when present, and changed code that follows the documented behavior/content/accessibility rule.
- Web Interface Guidelines evidence is complete: interaction applicability matrix has pass/fail/N/A plus reasons, and failures were revised or explicitly blocked.
- Screenshots show the real product/workflow in the first viewport for every verified route/surface, not a generic landing page unless the user explicitly requested marketing.
- Screenshots and code show one coherent system: shared tokens/classes/materials/primitives are reused, and there are no isolated Geist-looking components inside unrelated styling.
- Typography uses the mapped Geist categories/utilities and does not rely on giant generic headlines, all-bold headings, or default `text-base` everywhere.
- Color uses official roles or mapped project tokens; accents appear only for brand, links, selection, status, or focus.
- Materials and radii follow consulted Materials/component evidence; depth is structural and does not rely on loud shadows, glass panels, or decorative background effects.
- Mobile, laptop, desktop, and ultra-wide screenshots preserve layout integrity: no clipped text, overlapping controls, broken grids, unwanted scrollbars, or oversized card stacks.
- Generic SaaS heuristic diff is recorded: any template-like, ornamental, overly soft, overly colorful, or disconnected areas were identified and revised, or explicitly tied to both official docs and user scope before any strict/Vercel Taste Gate claim.

Official claim blockers:

- Final answer lacks page-specific `Docs Evidence` for every official Geist/Vercel page required for the task, or cites only memory, class names, token names, screenshots, or generic Geist adjectives.
- A final answer claims visual polish or Vercel Taste Gate passage without screenshot inspection and interaction audit when those checks were possible.
- Any required applied foundation, guideline, component, or brand row is missing, blocked, lacks an exact section/anchor, or lacks a page-specific short quote that affected a concrete decision.
- Any Web Interface Guidelines interaction failure remains unrevised without a concrete blocker.

Local anti-template heuristics:

These require revision or explicit user-scope plus official-doc justification before strict claims, but they are not official Geist violations by themselves and do not satisfy `Docs Evidence`.

- Purple-blue gradient SaaS aesthetic.
- Decorative orbs, bokeh blobs, aurora backgrounds, or ornamental SVG filler.
- Oversized rounded cards used as page sections.
- Card-in-card layouts.
- Heavy drop shadows or glassy panels.
- Fake sample data added only to make the UI look populated.
- Marketing copy inside product workflows.
- Dozens of visible controls before the primary task is clear.
- Mixed visual systems where only isolated buttons or cards look Geist-like.

If the app cannot be run, screenshots cannot be captured, or interaction checks cannot be performed, say that explicitly in the final response and do not claim the Vercel Taste Gate passed. If screenshots and interaction checks are possible, the final response must include the audit evidence: dev command, URL, mobile/laptop/desktop/ultra-wide viewport sizes, screenshot paths, changed states inspected, interaction applicability matrix summary, blockers, and revision decisions made because of the audits. Use an inspection method instead of screenshot paths only when screenshot capture is blocked, and then do not claim the Vercel Taste Gate passed.

Failure response:

- If any pass criterion fails and the file is editable, make another revision.
- If the failure cannot be fixed without user input or external access, explain the exact blocker and the closest safe fallback.
- In the final response, briefly state which checks ran and whether any visual verification was blocked.

## Final Verification Checklist

Before finishing any task using this skill that creates, changes, critiques, specifies, or materially directs rendered UI, verify:

- The first viewport shows the real product/workflow, not a generic landing page unless explicitly requested.
- Verification scope is explicit: greenfield/full redesign/broad polish covers all routable app surfaces; narrow existing-project work covers the requested workflow and touched shared primitives, and the final response says `whole app not verified` unless every route/surface was audited.
- The Geist foundation gate was completed before screen design: fonts, tokens, typography utilities, material/radius utilities, focus rings, app shell, required component primitives, shared state system, and screen composition rules are wired through real app entrypoints, theme/Tailwind/CSS files, shared primitives, and app shell, and consumed by changed screens.
- Screen-level styles compose shared Geist foundations, primitives, and state APIs/classes; they do not introduce one-off colors, font stacks, radii, focus rings, shadows, state styles, or component behavior.
- Strict Geist work uses local Geist Sans and Geist Mono. Non-Geist font replacements are allowed only after an explicit non-Geist visual-system override, and those surfaces cannot be claimed as strict/docs-verified Geist. Geist Pixel is installed/loaded only if a display accent uses it, and it is absent from ordinary product UI text.
- Typography uses official Geist classes or mapped equivalents for headings, buttons, labels, copy, mono, and tabular numeric text.
- Color roles use official Geist/Core tokens or custom raw Geist scale variables before semantic aliases such as `background`, `foreground`, `muted-foreground`, `border`, `ring`, `link`, `info`, `destructive`, `success`, and `warning`. Any `accent` alias resolves to a specific official Geist role/scale for focus, selection, link, or status; default/primary actions follow the consulted Button/component page.
- Chart/status palettes use redundant cues and color-blind-friendly choices, APCA contrast is checked where available, and hover/active/focus states increase contrast over rest state.
- Materials use the official 6px, 12px, and 16px radius scale or mapped project tokens.
- Every UI pattern that exists in Geist was checked against its Geist reference before custom implementation.
- Official Geist/Vercel pages required for the task are listed in a page-specific `Docs Evidence` table in the final response in all cases: consulted rows when read, blocked rows with exact tool failures when docs access fails, and the fallback label `local Geist fallback, not docs-verified` for affected surfaces.
- Relevant component pages' Best Practices were followed, not just visual styling.
- Vercel Web Interface Guidelines were applied for keyboard behavior, focus, hit targets, URL state, optimistic updates, tooltip timing, overscroll containment, clean drag behavior, locale-aware shortcuts, mobile inputs, states, copy, numerals/units, performance-relevant UI, `theme-color`, and `color-scheme`.
- The app shell, navigation, forms, tables/lists, dialogs, menus, toasts, loading, empty, error, and no-dead-end recovery paths all share the same audited Geist tokens, typography utilities, materials, primitives, state rules, root background, gutters, header/sidebar/nav structure, dividers, max-width behavior, mobile behavior, one primary action zone, skip-to-content, valid heading hierarchy, and context-specific `<title>`.
- Interactive controls have hover, active/pressed, selected/current, disabled, loading, validation, error, focus-visible, and reduced-motion states as relevant.
- Tables, lists, forms, and screens have loading, empty, error, no-results, validation, and recovery states as relevant.
- Desktop, mobile, laptop, and ultra-wide views were inspected when a local app can run; layouts do not overlap, clip text, shift unpredictably, create unwanted scrollbars, or break safe-area insets.
- Local anti-template heuristics such as generic SaaS gradients, decorative orbs, card-in-card sections, fake sample data, and unrelated visual styles are absent or revised; retained exceptions are tied to both explicit user scope and official docs, otherwise no strict/Vercel Taste Gate claim is made.
