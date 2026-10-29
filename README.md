# Night Bridge Design System

**Dark boutique bridge** — a token-driven design system for calm, data-forward UIs. Built with Astro 6, Tailwind 4, and an agent-publish layer for LLM workflows.

Live showcase: run locally at [http://localhost:4321](http://localhost:4321). Example product landing: [/coaching](/coaching) (Harbor Chapter).

## Quick start

```sh
npm install
npm run dev
```

| Command | Action |
| --- | --- |
| `npm run dev` | Dev server + regenerates `/tokens.json`, `/system.md`, `/llms.txt` |
| `npm run build` | Production build to `./dist/` |
| `npm run preview` | Preview production build |

**Node.js 22+** required.

## What's included

- **Tokens** — `src/styles/global.css` (`@theme` + `:root`): abyss background, warm primary, cool accent, IBM Plex Serif/Sans, `type-*` typography utilities
- **Showcase** — `src/pages/index.astro`: color, type, and component galleries
- **Components** — `src/components/ds/*` (Button, Card, Input, Badge, Section, …)
- **Shell** — `src/components/shell/*` (header, footer, route viz)
- **Agent layer** — generated on dev/build (not committed): `tokens.json`, `system.md`, `llms.txt`, versioned `/v1/`
- **Impeccable** — vendored in `.cursor/skills/impeccable` and `.claude/skills/impeccable` for `/impeccable` design commands
- **Personal context** — `PRODUCT.md` and `DESIGN.md` are gitignored; run `/impeccable init` locally if you fork this repo

## Stack

| Piece | Version |
| --- | --- |
| [Astro](https://astro.build/) | 6.x |
| [Tailwind CSS](https://tailwindcss.com/) | 4.x |
| daisyUI | registered, themes off — custom tokens only |

Deploy: static output (`wrangler.jsonc` for Cloudflare Pages).

## Origin

Evolved from the [DataCamp Summer Vibes](https://github.com/lucas-datacamp/vibe-design-system) session scaffold; customized for Night Bridge / Harbor Chapter.
