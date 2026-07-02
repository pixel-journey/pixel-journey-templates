# pixel-journey-templates

**The Canonical Library of Design Templates, Feature Patterns & Scaffolding for the Pixel Journey (Px) Ecosystem**

[![WAX](https://img.shields.io/badge/WAX-Antelope-blue?logo=ethereum)](https://wax.io) [![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178c6?logo=typescript)](https://www.typescriptlang.org/) [![Next.js](https://img.shields.io/badge/Next.js-15+-000000?logo=nextdotjs)](https://nextjs.org/) [![WharfKit](https://img.shields.io/badge/WharfKit-Session%20Kit-orange)](https://wharfkit.com) [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Mission**: Give the Px team and every future contributor **design templates, feature pattern templates, and project scaffolding** that make consistent, high-quality, pixel-perfect development **fast and joyful** — across PxWallet, Hot or Not, Pixal PFPs, PxPackages, docs, and every new idea.

This is not just boilerplate. It is the shared design language + implementation patterns that keep the entire ecosystem coherent while letting builders move at speed.

**This repo works hand-in-hand with `pixel-journey-design-system` (tokens, components, visual language) and `pixel-journey-standards` (engineering rules, Web3 patterns).** Together they form the foundation layer for PxPackages and all future Px work.

---

## Quick Start

```bash
# Create a new Px project from a template
gh repo create my-new-px-feature --template pixel-journey/pixel-journey-templates

# Or explore locally
cd templates/
# Pick a category: design-ui/, feature-patterns/, nextjs-dapp/, monorepo-pkg/, etc.
```

Every template includes:
- Strict TypeScript + full interfaces
- Deep integration points for the Px Design System
- WharfKit-first (Session + Contract Kit)
- Glassmorphic + optional retro-pixel / CRT theme hooks
- Layered educational READMEs (vision → usage → architecture decisions → customization)
- Working demo or Storybook-ready examples
- Ready-to-extend structure aligned with PxPackages future

---

## Why "Templates" Matter for Pixel Journey

Px is growing fast. To keep quality high and onboarding friction low (for both internal team and new community devs), we need:

- **Design consistency** — Every new screen or component feels like it belongs in the Px universe
- **Implementation consistency** — Common patterns (session management, asset fetching with cache, verifiable on-chain actions, modals, leaderboards, etc.) are solved once, documented excellently, and reused
- **Speed** — A new feature or mini-dApp can be scaffolded in hours, not days, while still following all the right architectural principles
- **Educational onboarding** — New devs (or AI agents) can read a template and understand not just *what* to do, but *why* we do it this way in Px

This repo is the home for all of that.

---

## Core Principles (Inherited from Px Lead Architect Mandate)

1. **ZERO CUSTOM CONTRACT OVERHEAD** — Leverage public WAX primitives (`atomicassets`, `alcorammswap`, `eosio.msig`, etc.).
2. **Client-Side First** — Public indexing APIs + local state + caching. GitOps where data pipelines are needed.
3. **On-Chain Entropy Ready** — All randomness uses deterministic TX hash + block header parsing (provably fair, zero extra cost).
4. **Design System Aligned** — Every UI template consumes tokens/components from `pixel-journey-design-system` (or provides clear extension points).
5. **Educational at Every Layer** — Root READMEs, category guides, per-template deep docs, and generous inline comments. The gkniftyheads-tracker example we explored showed the documentation quality bar we want everywhere.
6. **Composable & Config-Driven** — Easy to customize for new Px sub-projects or community forks.

---

## Template Categories (What Lives Here)

We organize around **what helps builders move fastest with consistency**:

| Category                        | Focus                                      | Priority | Example Contents / Use Cases                                      | Status      |
|--------------------------------|--------------------------------------------|----------|-------------------------------------------------------------------|-------------|
| **Repo & GitHub Scaffolding**   | New project / package bootstrap            | P0       | Full repo templates, .github/ workflows, issue/PR templates, semantic PR config, CONTRIBUTING.md standards | In Progress |
| **Design & UI Templates**       | Visual + component consistency             | P0       | Glassmorphic card templates, Asset Gallery shells, Modal / Drilldown templates, Leaderboard table shells, Tab navigation, CRT/Pixel theme toggles, Figma-to-code mapping guides | Planned     |
| **Feature Pattern Templates**   | Reusable implementation patterns           | P0       | WharfKit Session Provider + hooks, Verifiable Randomness (on-chain entropy) hook, Asset Query + TanStack Cache pattern, On-chain Action Button (loading/error states), Verifiable Voting / Hot-or-Not UI + logic shell, XP/Streak badge system starter | Planned     |
| **Full dApp / Mini-App Starters**| Complete runnable starting points         | P1       | Next.js 15 + WharfKit dApp shell (for PxWallet, Hot or Not frontend, PxTicker, community portals) | Planned     |
| **Monorepo & Package Templates**| Alignment with future PxPackages           | P1       | Turborepo/pnpm workspace starter for @pxjourney/* packages, tsup + vitest setup, export maps, changesets | Planned     |
| **Documentation Templates**     | Knowledge sharing & GitBook consistency    | P2       | GitBook folder structure templates, interactive demo embed patterns, WAX/EVM guide templates, README standards | Planned     |
| **Advanced Reference Examples** | High-quality, fully documented showcases   | P3       | (Optional later) Generalized collection tracker / rarity engine patterns (inspired by excellent external examples like gkniftyheads-tracker) — only when it directly accelerates Px features | Future      |

### Design & UI Templates (Core Focus)

These are the heart of making Px feel cohesive:
- Pre-built, themeable UI shells that match the Px Design System
- Common Web3 UI patterns solved once (asset cards, trait displays, leaderboards with surviving ranks or XP, modals with drilldown)
- Clear mapping from Figma / design-system components to production code
- Optional retro-pixel / CRT skin toggle for that signature Px flavor

### Feature Pattern Templates (The "Secret Sauce")

These are modular, copy-paste or import-friendly implementations of things we do repeatedly in Px:
- Session & wallet connection (WharfKit best practices)
- Fetching & caching on-chain data (AtomicAssets + Hyperion patterns)
- Verifiable on-chain actions with proper UX (signing, loading, error, success states)
- On-chain entropy for games (pure client-side, deterministic from TX + block)
- Leaderboard / ranking UI + logic shells (reusable for Hot or Not, Pixal tiers, holder analytics)

New Px devs can drop these in and immediately have production-grade, consistent behavior.

---

## Revised Master Plan & Roadmap

**Phase 1 — Foundation (Current)**
- [x] Root README realigned to design templates + feature patterns focus
- [x] Production CI + Px-specific issue/PR templates (enforcing design-system alignment & educational docs)
- [x] Initial `templates/` category scaffolding + READMEs
- [ ] Flesh out `templates/design-ui/` and `templates/feature-patterns/` with first concrete templates (e.g. Glassmorphic Card, WharfKit Session Hook, Verifiable Randomness utility)
- [ ] Create `shared/` types & utils that all templates can reference
- **Success**: Any team member or new dev can open this repo and immediately see how to build consistent Px UIs and features quickly.

**Phase 2 — Core Design & Feature Templates (Next priority)**
- High-quality, documented implementations of the most common Px UI patterns and feature primitives
- Tight hooks into `pixel-journey-design-system`
- Working demos / Storybook stories for each
- Full educational documentation (why this pattern, how it fits Px architecture, customization points)

**Phase 3 — Full Starters & Monorepo**
- Polished `nextjs-dapp` starter
- Monorepo package template aligned with PxPackages unification roadmap
- `create-px-app` style generator (optional but powerful for speed)

**Phase 4+ — Polish & Ecosystem**
- Documentation templates
- Advanced reference examples (only if they directly help Px velocity)
- Bidirectional improvement loop with real Px dApps (improvements from PxWallet / Hot or Not flow back into templates)
- Public announcement + integration into Px GitBook onboarding

---

## Current Repository Structure

```
pixel-journey-templates/
├── .github/                      # GitHub scaffolding used by the whole org
├── templates/
│   ├── design-ui/                # Glassmorphic cards, modals, galleries, leaderboards, theme toggles
│   ├── feature-patterns/         # Session management, verifiable entropy, asset queries, on-chain actions
│   ├── nextjs-dapp/              # Full dApp starter shell
│   ├── monorepo-pkg/             # For future @pxjourney/* packages
│   ├── github-org/               # Repo bootstrap helpers
│   └── documentation/            # GitBook + README templates
├── shared/                       # Common TS types, config schemas, small utils
├── docs/                         # Guides on "how to use templates in Px"
├── README.md                     # This file — the living master plan
└── CONTRIBUTING.md               # Quality bar for new templates
```

Every template folder will have its own deep README explaining vision, usage, architecture decisions, and how it supports consistent Px development.

---

## Immediate Next Steps

1. Confirm this revised direction (design templates + feature patterns for speed & consistency) feels right.
2. I will continue Phase 1 by creating concrete first templates in `design-ui/` and `feature-patterns/` (starting with high-impact, frequently used pieces).
3. We keep the educational excellence (layered docs) while focusing content on what accelerates actual Px work.

The gkniftyheads-tracker source you shared remains an outstanding example of **documentation quality** — we will apply that same rigorous, educational style to every template we create here, even if we are not porting its specific analytics engine right now.

Ready for the next slice. What would you like to build first?