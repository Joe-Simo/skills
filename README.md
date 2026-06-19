# Skills

[![skills.sh](https://skills.sh/b/joe-simo/skills)](https://skills.sh/joe-simo/skills)

Community Agent Skills by `joe-simo`.

## Apple Design System

`apple-design-system` is a community Agent Skill for designing, redesigning, reviewing, and polishing Apple-style interfaces using official Apple Human Interface Guidelines and Apple Developer design resources only. It helps agents apply platform-native typography, semantic colors, layout, materials, Liquid Glass, SF Symbols, app icons, navigation, controls, component behavior, accessibility, motion, platform adaptation, responsive behavior, asset/licensing boundaries, screenshots, and UI polish across iOS, iPadOS, macOS, watchOS, tvOS, visionOS, SwiftUI/UIKit/AppKit-style UI, and Cupertino-style web UI.

The skill treats official Apple Developer sources as the design authority: current HIG index pages, applied foundation pages, platform pages, component/pattern/input/technology pages, Apple Design Resources, Apple Fonts, and Apple developer terms. Broad Apple-quality claims require a live index sweep so current pages such as Dark Mode, Privacy, Images, newer inputs, and branded technologies are not skipped. It does not use third-party summaries, UI kits, templates, copied Apple screenshots, extracted private assets, or unofficial HIG mirrors as design authority.

The skill includes the same kind of enforcement structure as the Geist skill: a source-of-truth gate, official reference map, foundation gate, platform/pattern map, component documentation contract, component/interaction coverage map, asset/licensing gate, privacy/data-use gate, Apple interface craft checks, accessibility verification, and an Apple Taste Gate for screenshots, interaction checks, and final evidence.

The main `SKILL.md` stays compact for lower initial context use. Detailed source gates, foundations, platform mapping, component rules, interaction coverage, interface craft, asset/licensing checks, privacy/data-use checks, accessibility, and verification checks live in `skills/apple-design-system/references/` and are loaded only when relevant.

This is community-authored by `joe-simo`. It is not an official Apple skill and is not permission to copy Apple apps, Apple marketing, Apple icons, Apple trademarks, or private system UI.

## Awwwards-Style Web Design

`awwwards-style-web-design` is a community Agent Skill for designing and reviewing original Awwwards-style, award-caliber experiential websites. It helps agents create high-craft portfolios, agency sites, editorial microsites, campaign pages, product launches, cinematic landing pages, scroll narratives, WebGL/Three.js/R3F scenes, GSAP/Motion-style interactions, tactile transitions, typography, composition, art direction, audio/video/media, responsive layouts, accessibility, performance, and UI polish. Ordinary portfolio, campaign, launch, luxury, fashion, music, or editorial work should only use it when the request also asks for high-craft, immersive, motion-led, WebGL-heavy, award-caliber, or experiential treatment.

The skill is not a template and does not promise awards. When a user asks for a winning-level site, it interprets that as the strongest honest award-caliber candidate possible inside the project's constraints. It teaches agents to synthesize patterns from award-caliber web work into original concepts: benchmark calibration, multiple concept directions, creative-director selection, clear experience thesis, content-native interaction, bespoke art direction, motion discipline, real content, proper assets, reduced-motion fallbacks, official docs evidence, browser verification, measurable accessibility/performance checks, and production-grade implementation.

The skill includes strict originality and safety guardrails. It must not be used to clone, recreate, or closely imitate any Awwwards winner, nominee, layout, art direction, animation sequence, copy, code, brand system, logo, screenshot, video, or protected campaign concept.

This is a skill, not a plugin or template installer. It should guide original work inside the user's actual project, not clone templates, starters, boilerplates, demo apps, unofficial source code, or generated template code. Implementation guidance should come from the project itself and official library documentation.

The main `SKILL.md` stays compact for lower initial context use. Detailed originality gates, experiential foundations, craft patterns, visual/layout rules, motion/3D guidance, implementation constraints, tool/stack routing, and award-readiness verification live in `skills/awwwards-style-web-design/references/` and are loaded only when relevant.

This is community-authored by `joe-simo`. It is not affiliated with, endorsed by, sponsored by, or authorized by Awwwards.

## Vercel Geist Design System

`vercel-geist-design-system` is a community Agent Skill for designing and reviewing Vercel-inspired interfaces with the Geist design system. It helps agents apply Geist typography, spacing, colors, materials, component styling, app shells, interaction states, screenshot audits, and UI polish across React, Next.js, Tailwind, shadcn, Radix, and other frontend surfaces.

The skill treats official Vercel sources as the design authority. `https://vercel.com/design.md` is now the primary foundation source for Geist tokens, typography, spacing, radii, component defaults, layout rhythm, elevation, motion, focus, and voice; `https://vercel.com/design.dark.md` covers the dark theme. Geist Font, component pages, Brands, Web Interface Guidelines, and conditional foundation pages are used when their specific domains are touched. Skills.sh companions are routing helpers only; they do not replace official Geist docs or prove Geist compliance by themselves.

The skill bundles current local snapshots at `skills/vercel-geist-design-system/references/vercel-design.md` and `skills/vercel-geist-design-system/references/vercel-design-dark.md` so agents can inspect exact token tables and defaults without bloating `SKILL.md`. Because Vercel marks those documents alpha, strict/docs-verified claims still require opening the current live official pages in the current turn.

The skill now asks agents to select the right Vercel/Geist reference archetype before designing. The Vercel homepage is a good reference for homepage, hero, launch, and broad marketing composition, but it is not the universal target. For dashboards, docs, settings, forms, tables, pricing, portfolios, app shells, and component libraries, agents should inspect comparable Vercel/Geist surfaces and mapped components, then measure composition details such as container width, section rhythm, density, typography scale, grid spans, interactions, and responsive behavior.

For existing products, the skill now includes a preservation gate: agents should restyle intentional content, routes, CTAs, brand-defining effects, credential displays, navigation, contact paths, and footer ownership before replacing or inventing alternatives. This is public guidance for any project using the skill, not a project-specific rule.

For Vercel-style grids, the skill now separates grid layout from grid backgrounds. Agents should use CSS grid/flex, columns, rows, gutters, cells, spacing, borders, and stable responsive spans for normal Geist layout. They should not add decorative grid backgrounds, graph-paper lines, blueprint lines, guide lines behind content, or page-wide repeating gradients just because the task says Vercel style, grid layout, dashboard grid, or feature grid. Visible guide/cell/grid background art is opt-in only when the user explicitly asks for it, a user-supplied design clearly shows it, or the requested surface is the official Geist Grid component; otherwise the page should use solid Geist backgrounds and functional grid structure.

The main `SKILL.md` stays compact for lower initial context use. Detailed source gates, component mappings, trust/brand/asset rules, motion/performance/copy rules, style rules, companion routing, and verification checks live in `skills/vercel-geist-design-system/references/` and are loaded only when relevant.

The current companion routing covers:

- Core Geist and guideline helpers: `geist`, `geistdocs`, and `web-design-guidelines`
- Implementation helpers: `building-components`, `shadcn`, React best practices, Next.js guidance, and Vercel composition patterns
- Verification helpers: browser automation, browser verification, full-flow verification, and before/after visual comparison
- Conditional surfaces: AI Elements, Streamdown, `json-render/react-three-fiber`, View Transitions, Geist learning labs, and Remotion Geist video work

The skill intentionally avoids routing Vercel platform/runtime skills for visual design work unless the user explicitly asks for that product capability.

This is community-authored by `joe-simo`. It is not an official Vercel skill.

## License

MIT. See `LICENSE`.

## Install

```bash
npx skills@1.5.9 add joe-simo/skills
npx skills@1.5.9 add joe-simo/skills --skill apple-design-system
npx skills@1.5.9 add joe-simo/skills --skill awwwards-style-web-design
npx skills@1.5.9 add joe-simo/skills --skill vercel-geist-design-system
```

## Local Validation

```bash
npm ci --ignore-scripts --no-audit --no-fund
npx --no-install skills add . --list
for skill in skills/*; do npx --no-install skills-ref validate "$skill"; done
git diff --check
git diff --cached --check
```

Before publishing, also verify internal Markdown reference paths resolve from
`SKILL.md` and `references/`, then run the trusted public-link sweep across
`README.md`, `skills/`, and `skills.sh.json`.

## Example Prompts

```txt
Design an original award-caliber portfolio site with strong art direction, motion, and responsive craft.
```

```txt
Design this iOS app flow using official Apple Human Interface Guidelines.
```

```txt
Review this macOS settings window against Apple HIG typography, layout, materials, controls, and accessibility.
```

```txt
Make this SwiftUI interface feel native to Apple platforms without copying Apple apps.
```

```txt
Design a visionOS settings flow with spatial comfort, indirect input, materials, and accessibility verified against official Apple pages.
```

```txt
Create an Apple-style web translation of this dashboard without using Apple-owned assets or claiming native HIG compliance.
```

```txt
Create a cinematic product launch page with WebGL only if it meaningfully improves the concept.
```

```txt
Review this landing page against a design-award-style usability, creativity, content, performance, and accessibility gate.
```

```txt
Turn this campaign idea into an immersive editorial scroll story without cloning any reference site.
```

```txt
Design this Next.js dashboard with strict Vercel Geist system quality.
```

```txt
Review this React app and make the UI feel like a cohesive Geist-based product.
```

```txt
Refactor these shadcn components so they follow Geist typography, spacing, materials, and interaction patterns.
```

```txt
Audit this landing page and app shell against Vercel Geist design-system expectations.
```

```txt
Create an AI chat surface that uses Vercel-style Geist UI, with AI Elements only as implementation infrastructure.
```

```txt
Render a constrained React Three Fiber scene from json-render inside a Geist-styled product page.
```

## Attribution

GitHub: `joe-simo`

X: `@joesimo`

Website: [joesimo.com](https://joesimo.com)

## Links

- [skills.sh/joe-simo/skills](https://skills.sh/joe-simo/skills)
- [skills.sh/joe-simo/skills/apple-design-system](https://skills.sh/joe-simo/skills/apple-design-system)
- [skills.sh/joe-simo/skills/awwwards-style-web-design](https://skills.sh/joe-simo/skills/awwwards-style-web-design)
- [skills.sh/joe-simo/skills/vercel-geist-design-system](https://skills.sh/joe-simo/skills/vercel-geist-design-system)
