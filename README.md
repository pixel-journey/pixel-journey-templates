# pixel-journey-templates

**The Canonical Educational Boilerplate & Reference Implementation Arsenal for Pixel Journey (Px) on WAX / Antelope**

[![WAX](https://img.shields.io/badge/WAX-Antelope-blue?logo=ethereum)](https://wax.io) [![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178c6?logo=typescript)](https://www.typescriptlang.org/) [![Next.js](https://img.shields.io/badge/Next.js-15+-000000?logo=nextdotjs)](https://nextjs.org/) [![WharfKit](https://img.shields.io/badge/WharfKit-Session%20Kit-orange)](https://wharfkit.com) [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Mission**: Equip every builder — human or AI — with pixel-perfect, production-grade starting points that embody the Px ethos: **trustless verifiable mechanics**, **client-side sovereignty**, **zero custom contract overhead**, **retro-pixel joy + serious engineering**, and **unparalleled educational clarity**.

Every template is a self-contained learning resource + runnable foundation. Clone one, understand *why* every architectural decision was made, customize via config, and ship.

**This repo is the long-term foundation layer for the entire Pixel Journey GitHub Organization.** It will evolve alongside `pixel-journey-design-system` (theming & primitives) and `pixel-journey-standards` (engineering & Web3 rules), and feed into the upcoming `PxPackages` monorepo (@pxjourney/* scope).

---

## Quick Start (Pick Your Template)

```bash
# 1. Use GitHub template (recommended for new repos)
gh repo create my-px-dapp --template pixel-journey/pixel-journey-templates --public

# 2. Or clone a specific template locally
git clone https://github.com/pixel-journey/pixel-journey-templates.git
cd pixel-journey-templates/templates/nextjs-dapp
npm install && npm run dev

# 3. For the full Analytics/GitOps Tracker template (gold standard reference)
cd templates/analytics-tracker
git clone ... # (or copy from this repo)
npm run hydrate   # one-time (or use demo data)
npm run calculate # rarity + leaderboards
# Then open demo/index.html
```

All templates include:
- Strict TypeScript + comprehensive interfaces
- WharfKit (Session Kit, Contract Kit) — never legacy UAL/eosjs
- Tailwind + Shadcn/Radix + Framer Motion (glassmorphic + optional CRT/Pixel skin)
- Full educational READMEs at every layer (root → category → template → inline comments)
- Working demo with mock or live public data
- .github/workflows CI ready to enable
- Config-driven everything (weights, endpoints, theme, collection)

---

## Vision & Alignment with Pixel Journey Ecosystem

Pixel Journey (Px) is building a community-driven, verifiable, meme-infused Web3 ecosystem on WAX:
- **Pixal PFPs** (Holder / Stacker / Whale / Kraken tiers + WaxRock, burns/airdrop mechanics)
- **YEET** meme coin (fair launch, airdrops, PURR rewards, staking, no team allocation)
- **PxWallet** (god-mode self-custody vault, cross-chain derivation WAX→EVM/Solana, Chrome MV3 + PWA, auto-sign, DeFi)
- **Px Hot or Not** alpha (verifiable voting arena with PXJ transfers, leaderboards, XP/streaks, on-chain entropy)
- **PxTicker** & analytics grids (Alcor AMM, trait exposure, whale tiering)
- **PxPackages** monorepo standardization (@pxjourney/core, @pxjourney/ui, @pxjourney/game, etc.)
- **GitBook Knowledge Bank** (WAX/EVM guides, docs.pixeljourney.xyz)

This templates repo exists so that every future piece of that vision (and community forks) can be built **fast, correctly, and educationally**.

We follow the sacred principles from the Lead Architect mandate:

### Core Architectural Principles (Non-Negotiable in Every Template)

1. **ZERO CUSTOM CONTRACT OVERHEAD** — Maximize existing public primitives: `atomicassets`, `atomicmarket`, `alcorammswap` (Concentrated Liquidity v2), `eosio.msig`, `eosio.token`. No new smart contracts unless absolutely unavoidable for core protocol.
2. **STATE PATTERNS & CLIENT-SIDE RENDERING** — No centralized backend DBs. Everything via public indexing (Hyperion History API, Light-API, native RPC tables), localStorage caching, and client-side processing. GitOps for data pipelines.
3. **ON-CHAIN ENTROPY** — All randomized game mechanics use deterministic client-side parsing of WharfKit-broadcast transaction hashes + block headers. Provably fair, zero RAM/oracle cost.
4. **EDUCATIONAL SUPREMACY** — Every template must be the best possible teacher. Layered READMEs (big-picture handbook → file-by-file guides → decision matrices → inline annotations). A new dev or AI must be able to understand the *entire system* without external hand-holding.
5. **PIXEL-PERFECT + RETRO-FUTURE UX** — Optional CRT scanlines, Press Start 2P typography, 120Hz fluid haptics-ready interactions, glassmorphic dark theme with neon Px accents. Luxury feel on modern hardware.
6. **COMPOSABLE & CONFIG-DRIVEN** — One `config.json` (or env) controls collection names, rarity weights, API nodes, feature flags, theme. Easy to fork for new Px sub-projects.

---

## MASTER PLAN: pixel-journey-templates v1.0 — Complete Template Ecosystem

This is the living master plan. We will iterate publicly here. Every phase delivers runnable, documented value.

### Template Taxonomy (What We Will Build)

We organize by **use-case category**, not by tech stack (stack is standardized across all).

| Category                        | Priority | Est. Complexity | Key Deliverables & Educational Value                                                                 | Example Px Use Cases                          | Status      |
|--------------------------------|----------|-----------------|-------------------------------------------------------------------------------------------------------|-----------------------------------------------|-------------|
| **GitHub Org & Repo Scaffolding** | P0      | Low            | .github/ templates (workflows, issue/PR templates, CODEOWNERS, semantic labels), root package.json patterns, CONTRIBUTING.md gold standard | New repo bootstrap for any Px package or dApp | In Progress |
| **Core Next.js dApp Starter**     | P0      | Medium         | Next.js 15 (App Router, Turbopack), WharfKit full integration, Zustand/TanStack Query stores, i18n (8+ locales), asset gallery, session management, Px design system hooks | PxWallet, Px Hot or Not frontend, PxTicker   | Planned     |
| **Analytics / GitOps Tracker**    | P0      | Medium-High    | Generalized version of the excellent gkniftyheads-tracker (full source provided). Config-driven collection, cursor-pagination hydrate, delta-sync (mints+burns), weighted rarity + surviving_mint_rank engine, trait exposure split, beautiful interactive demo dashboard, daily GitHub Action self-updating, full file-by-file architecture handbook | Pixal PFP trait exposure & leaderboards, YEET holder analytics, Hot or Not XP leaderboards, any future collection | **Ready to Port** |
| **Verifiable Game Mechanics**     | P1      | Medium         | On-chain entropy utils (pure TS, no deps) + Hot-or-Not voting arena template (PXJ xfer + 50% reward split, verifiable pairing via memo), XP/streak/badge systems, leaderboards | Px Hot or Not alpha v0.2+, future mini-games | Planned     |
| **Wallet & Security Primitives**  | P1      | High           | Encrypted vault patterns (master pw + derived keys), cross-chain key derivation (WAX → EVM/Solana), Chrome MV3 extension (background/popup/content scripts), PWA + auto-sign opt-in, WharfKit Account Kit examples | PxWallet god-mode (150+ item roadmap)        | Planned     |
| **Monorepo & @pxjourney/* Package** | P2     | Medium         | Turborepo / pnpm workspace template, tsup build, vitest + playwright, changesets, strict exports, alignment with PxPackages unification roadmap | Core utils, UI primitives, game SDK hooks, WAX SDK wrappers | Planned     |
| **Canvas Pixel Mini-Game Base**   | P2      | Medium         | HTML5 Canvas + Web Workers for heavy data, retro pixel rendering, input handling, integration with on-chain entropy & WharfKit signing for on-chain actions | Future Px mini-games, asset visualizers      | Planned     |
| **Documentation & Knowledge Bank**| P2      | Low            | GitBook-compatible MD structure, interactive demo embeds, WAX/EVM guide templates, navigation patterns (as audited in Px docs) | docs.pixeljourney.xyz knowledge bank         | Planned     |
| **DeFi & Alcor Integration**      | P3      | Medium         | alcorammswap concentrated liquidity hooks, quote/routing/swap examples, limit orders, arbitrage detectors, PxTicker grid components | Px DeFi features, token analytics            | Planned     |

### Phased Implementation Roadmap

**Phase 1 — Foundation (Current Sprint)**
- [x] Massive root README upgrade with full vision, principles, taxonomy & this plan
- [ ] Upgrade all .github/ files (production CI matrix with lint/build/test, dependabot, labeler, stale)
- [ ] Create `templates/` directory skeleton with category READMEs
- [ ] Create `shared/` for common types, utils, config schemas (reusable across templates)
- [ ] Update CONTRIBUTING.md, SECURITY.md, LICENSE to Px standards
- [ ] Add root `config.json` example + schema
- **Success Metric**: Any AI or dev can read root README and immediately understand the entire future of Px template strategy.

**Phase 2 — Core dApp & Analytics Gold Standard (Next 1-2 weeks)**
- Port & generalize the complete **gkniftyheads-tracker** (provided in full context) into `templates/analytics-tracker/`
  - Make 100% config-driven (collection name, weights, API fallbacks, demoLimit, gzip)
  - Keep *all* the educational excellence: file-by-file guides, WAX best practices section, decision matrices, formulas
  - Add Px-branded demo data (Pixal PFP style) + live toggle
  - Ensure it becomes the reference implementation for any future Px data/analytics tool
- Scaffold `templates/nextjs-dapp/` with working WharfKit session, sample AtomicAssets query, Px glassmorphic UI shell, i18n stub, Zustand stores
- **Success Metric**: `npm run dev` in analytics-tracker shows beautiful live-updating (demo) leaderboards + trait exposure in < 60s. New collection can be tracked by editing one config value.

**Phase 3 — Game & Verifiable Mechanics (Following)**
- Extract on-chain entropy utility (pure TS, no deps) + Hot-or-Not voting template
- Verifiable seed/pairing via pxhot.pxj TX memos (as in current Px Hot or Not alpha planning)
- Leaderboard + XP system with surviving ranks pattern (reuse from analytics tracker)

**Phase 4 — Wallet, Package & Advanced**
- Chrome ext + PWA wallet primitives
- Monorepo package template aligned with PxPackages 92-point upgrade roadmap
- Full cross-linking and example data from real Px repos (when ready)

**Phase 5 — Polish, CLI & Ecosystem**
- `create-px-app` CLI (or `npx` generator) that scaffolds from these templates
- Storybook / interactive docs site (self-hosted or GitHub Pages)
- Automated contribution checks (template checklist enforcement)
- Public launch announcement on @PxJourney X + integration into Px GitBook

**Long-term (v2+)**: Templates become living references — improvements from real Px dApps (PxWallet, Hot or Not, PxTicker) flow back here. The repo itself becomes a showcase of Px engineering quality.

---

## Why This Architecture Wins for Px & WAXFAMs Community

| Approach                        | Cost | Educational Value | Onboarding Speed | Auditability | Recommendation for Px |
|--------------------------------|------|-------------------|------------------|--------------|-----------------------|
| **This Templates Repo (GitOps + Layered Docs)** | $0  | Excellent (layered + runnable) | Minutes         | Full Git history | **Strongly Recommended** |
| Minimal boilerplate (create-next-app + manual) | $0 | Poor             | Hours            | Low          | Only for throwaway prototypes |
| Custom backend-heavy           | $$  | Medium           | Days             | Medium       | Avoid for public goods   |

**GitOps + Static + Educational** is the Px way: transparent, forkable, zero ongoing cost, perfect for community contributions and AI-assisted development.

---

## WAX AtomicAssets & Public Infra Best Practices (Baked Into Every Template)

All templates that touch chain data will include (and educate on):

- **Cursor-based pagination** (`lower_bound` + `sort=asset_id&order=asc`) — the only sane way for 100k+ collections (avoids deep page cliff). See `hydrate.js` pattern in analytics-tracker.
- **Delta sync patterns** (mints via `after=` + burns via `burned=true` + `sort=updated`)
- **Rate-limit friendly batching** + exponential backoff + multiple public endpoints (alcor, eosphere, etc.)
- **POST for complex queries** when GET URL length limits hit
- **Key fields mastery**: `asset_id`, `template_id`, `template_mint` (critical for surviving mint rank), `owner`, `burned`, `attributes`/`immutable_data`
- **Client-side only processing** for rarity, exposure, leaderboards, XP — no DB needed for public dashboards
- Full reference: https://onblock.dev/working-with-the-atomic-api (highly recommended reading, included in every relevant README)

---

## Current Repository Structure (Evolving)

```
pixel-journey-templates/
├── .github/                    # Org-wide GitHub automation & templates (upgrading now)
│   ├── workflows/
│   │   └── ci.yml              # Multi-job matrix (lint, build, test) — Phase 1
│   ├── ISSUE_TEMPLATE/         # bug_report, feature_request (Px-specific)
│   └── PULL_REQUEST_TEMPLATE.md
├── templates/                  # The actual template library (Phase 1 scaffolding)
│   ├── README.md               # Category overview + how to pick
│   ├── github-org/             # For new org repos
│   ├── nextjs-dapp/            # Core frontend starter
│   ├── analytics-tracker/      # Gold standard — generalized gkniftyheads-tracker
│   ├── game-verifiable/        # Hot-or-Not + entropy
│   ├── wallet-primitives/      # Vault, cross-chain, ext
│   └── ...
├── shared/                     # Reusable TS types, utils, config schemas (reusable across templates)
│   ├── types/
│   ├── utils/
│   └── config.schema.json
├── docs/                       # Master educational guides
│   ├── WAX_CLIENT_PATTERNS.md
│   ├── ONCHAIN_ENTROPY_GUIDE.md
│   └── CONTRIBUTING_TEMPLATES.md
├── scripts/                    # Optional generators / validators
├── README.md                   # You are here — the single source of truth
├── CONTRIBUTING.md             # Detailed contribution checklist (template quality bar)
├── config.example.json
└── LICENSE
```

Every sub-folder will eventually have its own exhaustive README.md (architecture, formulas, file inventory, customization, migration notes) — exactly like the gkniftyheads-tracker root and scripts/ READMEs.

---

## Immediate Next Steps (This Conversation Thread)

1. **Review & Align** on this Master Plan (adjust priorities, add missing categories, confirm Px branding).
2. **Phase 1 Execution Begins Now** — I have already upgraded this root README. Next actions in thread:
   - Push production-grade `.github/workflows/ci.yml` + new issue/PR templates
   - Scaffold `templates/analytics-tracker/` by porting the complete, excellent gkniftyheads-tracker (with generalization layer)
   - Create `templates/nextjs-dapp/` skeleton with WharfKit hello-world + Px UI shell
3. Iterate: You give feedback or new requirements → I refine plan + execute next slice → commit directly to main (or PR if preferred).

We will keep every change **highly educational** and **pixel-perfect**.

---

**Built with ❤️ for the Pixel Journey community, WAXFAMs, and every future builder who wants to understand *why* their dApp works.**

*Part of the Pixel Journey GitHub Organization — PxWallet • Px Hot or Not • Pixal PFPs • YEET • PxPackages*