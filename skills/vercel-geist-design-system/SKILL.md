---
name: vercel-geist-design-system
description: >-
  Community skill for applying the Geist design system to Vercel-inspired
  rendered frontend UI across React/Next.js/Vite/Astro/Svelte/Vue/HTML/CSS,
  Tailwind, shadcn, and Radix. Use for typography, spacing, color, materials,
  components, app shells, dashboards, forms, tables, dialogs, states, responsive
  layout, and UI polish. Community-authored, not official Vercel. Trigger for
  Geist, Vercel-style UI, or generic clean/modern/premium/polished
  SaaS/developer-product visuals when no other final visual system is requested.
  Skip non-visual work unless it materially changes rendered UI.
metadata:
  author:
    github: joe-simo
    x: "@joesimo"
    website: https://joesimo.com
  community: true
  official: false
  short-description: Unofficial Vercel Geist visual system for clean, polished SaaS/developer-product UI; skip non-visual work and explicit alternate visual systems
  sources:
    - https://vercel.com/font
    - https://vercel.com/design/guidelines
    - https://vercel.com/geist/introduction
    - https://vercel.com/geist/colors
    - https://vercel.com/geist/typography
    - https://vercel.com/geist/materials
    - https://vercel.com/geist/brands
---

# Vercel Geist Design System

Use this community skill to make interfaces feel like they belong in Vercel's
Geist design system: precise, calm, high-contrast, developer-focused, and
production-ready. Official Vercel pages are the source of truth. This is not
official Vercel guidance and is not permission to copy Vercel product screens.

## Reference Loading Contract

This compact file is the operating contract. Detailed rules live in
`references/`; load only what the task needs, but never skip a required
reference because this summary seems sufficient.

- Always load `references/source-of-truth-gate.md` for triggered visual work
  before claiming Geist, strict Geist, docs-aligned Geist, source-of-truth
  alignment, or Vercel Taste Gate passage.
- Load `references/foundation-and-style-rules.md` before creating, restyling,
  redesigning, reviewing, or materially changing rendered UI.
- Load `references/official-reference-map.md` when mapping foundations,
  brand/assets, or components to official Vercel URLs.
- Load `references/component-system.md` before components/primitives/states,
  custom compositions, UI copy, performance-relevant UI, icon/brand, motion, or
  Web Interface Guidelines overlay work.
- Load `references/companion-routing.md` only when another Skills.sh entry,
  framework helper, verification helper, tool, or conditional surface could be
  relevant.
- Load `references/taste-and-verification.md` before final audit, screenshots,
  interaction checks, or final response for triggered visual work.

## Trigger Policy

Trigger this skill when a task creates, changes, critiques, specifies, or
materially directs rendered frontend UI and the user asks for Geist,
Vercel-style UI, or generic clean, modern, premium, beautiful, polished
SaaS/developer-product visual design with no competing visual authority.

Do not trigger for TypeScript fixes, data wiring, API/state changes, analytics,
tests, build tooling, dependency work, or behavior-only accessibility fixes
unless rendered UI is created or materially changed.

An explicit non-Geist final visual system, brand style, supplied final non-Geist
design artifact, game style, or illustrative art direction overrides this skill.
Domain, industry, product, API, integration, content subject, Tailwind, shadcn,
Radix, or component-library mentions are not visual-system overrides or trigger
signals by themselves.

When triggered, Geist owns the visual system. Ignore generic frontend-design
pushes toward bold, unforgettable, maximal, ornamental, or surprising visuals
unless the user explicitly overrides Geist.

## Operating Loop

1. Identify the UI surface and scope: greenfield app, full redesign, narrow
   workflow, marketing page, dashboard, settings, table/list, command workflow,
   docs, or component library.
2. Inspect the project before designing: framework, Tailwind version, component
   library, icon library, font setup, theme tokens, existing primitives, routing,
   package manager, and validation commands.
3. Load the required references above.
4. Open current official Vercel pages for every required foundation, guideline,
   brand/assets, and mapped component before implementation or strict claims.
5. Complete the Foundation Gate before screen work: fonts, semantic color
   tokens, typography utilities, material/radius utilities, focus rings, app
   shell, primitives, shared states, and screen composition rules.
6. Map every UI requirement to an official Geist foundation/component,
   official composition, or constrained custom composition before inventing
   patterns.
7. Implement through shared tokens and primitives. Use Radix/shadcn only as
   behavior/accessibility infrastructure after Geist mapping; their visual
   defaults are not design authority.
8. Verify with the Taste Gate, revise failures, then report evidence and
   blockers honestly.

## Non-Negotiables

Official docs are binding design input, not optional inspiration. Required
foundation pages are `https://vercel.com/font`,
`https://vercel.com/geist/introduction`, `/colors`, `/typography`,
`/materials`, and `https://vercel.com/design/guidelines`. Brand/logo work also
requires `https://vercel.com/geist/brands`. Component work requires every
matching official component page from `references/official-reference-map.md` or
the live Geist component navigation.

If required official docs cannot be loaded after every available browsing/docs
tool is attempted in the current turn, state attempted URLs, tools, and exact
failures. Local rules then become advisory only, cannot satisfy
`Docs Evidence`, and cannot support strict/docs-verified claims. Label affected
work `local Geist fallback, not docs-verified`.

Final responses for triggered visual work must include the page-specific
`Docs Evidence` table defined in `references/source-of-truth-gate.md`. Do not
claim strict Geist, docs-aligned Geist, official Geist compliance,
source-of-truth alignment, or Vercel Taste Gate passage if any required applied
row is missing, blocked, lacks an exact section/anchor, or lacks a short
page-specific quote that affected a concrete decision. Strict claims also
require screenshot and interaction checks when those checks are possible.

Geist must own the relevant visual system. Do not create isolated
Vercel-looking widgets inside unrelated UI. Broad work covers app shell,
navigation, pages, forms, data views, dialogs, toasts, command menus, marketing
sections, and empty/loading/error states across all routable surfaces and shared
states. Narrow work covers the requested workflow plus touched primitives; say
`whole app not verified` unless every route/surface was audited.

Use Geist Sans globally, Geist Mono for code/technical identifiers, and Geist
Pixel only for a constrained display/brand accent when justified. Keep ordinary
product UI neutral-first, high-contrast, compact, semantic, accessible, and
state-driven. Typography and spacing should carry hierarchy; color should be
functional; borders should structure the UI; motion should be subtle and tied
to state.

Skills.sh companions are routing helpers only. They never replace official
Geist docs, never define Geist visuals, and never satisfy `Docs Evidence`.

## Verification Contract

Before final response for triggered visual work, run the Vercel Taste Gate in
`references/taste-and-verification.md`: route inventory, current official docs,
Foundation Gate, component mapping, Web Interface Guidelines audit, screenshots,
interaction checks, responsive checks, anti-pattern scan, and revision loop.

If a local app can run, inspect mobile, laptop, desktop, and ultra-wide
viewports plus changed states such as menus, dialogs, empty states, loading
states, errors, and dense data views. If screenshots or interaction checks are
possible and not captured, do not claim the Taste Gate passed. If the app
cannot run or verification is blocked, state the exact blocker and use only the
allowed limited claim.

Final responses must report the important evidence concisely: commands, URL,
viewport sizes, screenshot paths or blocker, changed states inspected,
interaction summary, Docs Evidence, revisions made because of the audit, and
any `whole app not verified` scope limit.
