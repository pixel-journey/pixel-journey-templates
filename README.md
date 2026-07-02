# pixel-journey-templates

**The Official Standards, Patterns, Ecosystem Handbook & AI Collaboration Templates for Pixel Journey (Px)**

[![WAX](https://img.shields.io/badge/WAX-Antelope-blue?logo=ethereum)](https://wax.io) [![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178c6?logo=typescript)](https://www.typescriptlang.org/) [![Next.js](https://img.shields.io/badge/Next.js-15+-000000?logo=nextdotjs)](https://nextjs.org/) [![WharfKit](https://img.shields.io/badge/WharfKit-Session%20Kit-orange)](https://wharfkit.com) [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **This is the single source of truth for *how we build* in the Pixel Journey organization** — including how we collaborate with specialized AI agents.
> It defines the standards, recommended patterns, architectural principles, ecosystem overview, and AI prompt templates that keep every Px project **consistent, high-quality, educational, production-ready, and fast to develop**.

**This repo contains the instructions, standards, pattern overviews, expected shapes, and AI collaboration templates** that all other repos in the `pixel-journey` organization follow (or are actively aligning to).

It works alongside:
- `pixel-journey-standards` — Foundational engineering rules and Web3 best practices
- `pixel-journey-design-system` — The visual language, tokens, components, and detailed style guide
- `wax-ecosystem-blueprint-catalog` — Curated WAX public infrastructure blueprints and guides
- `gitbook-docs` — The living educational knowledge base
- All individual Px repos (PxWallet, Hot or Not, PxPackages, etc.)

---

## Vision & Long-Term Participation Mindset

Pixel Journey exists to create **extraordinary, educational, and empowering Web3 experiences** on WAX and Antelope infrastructure — with a deep commitment to client-side sovereignty, on-chain entropy, beautiful design, and long-term ecosystem health.

We believe the best way to scale quality is to give both humans *and* AI collaborators a single, authoritative, living handbook that encodes our principles, patterns, and educational standards.

This repo is designed for **long-term participants** — people and agents who want to build consistently excellent Px projects over months and years, not just quick prototypes.

---

## Quick Starts (Choose Your Path)

### For New Humans Exploring Px
1. Read `ECOSYSTEM.md` + `GLOSSARY.md`
2. Skim `STANDARDS.md` (focus on the 7 foundational principles)
3. Explore `AI_PROMPTS.md` to understand how we collaborate with AI
4. Start building with one of the templates in `templates/`

### For Developers Starting New Work
1. Read `STANDARDS.md` fully
2. Review `PATTERNS.md` for the pattern you need
3. Use the relevant AI prompt from `ai-prompts/personas/`
4. Follow `EDUCATIONAL-QUALITY-STANDARD.md` when writing docs or blueprints

### For AI Agents & Power Users
1. Load the appropriate persona prompt from `ai-prompts/personas/`
2. Combine with knowledge banks in `ai-prompts/knowledge-banks/`
3. Reference `STANDARDS.md` and `PATTERNS.md` as grounding context
4. Always align output to `EDUCATIONAL-QUALITY-STANDARD.md`

### For Reviewers & Maintainers
- Use the checklists in `STANDARDS.md`
- Verify alignment with `pixel-journey-design-system` and `EDUCATIONAL-QUALITY-STANDARD.md`
- Check that new patterns are generalized back into this handbook

---

## What You Will Find Here

| Section                          | Purpose                                                                 | Best For |
|----------------------------------|-------------------------------------------------------------------------|----------|
| **STANDARDS.md**                 | Rules, checklists, expected shapes                                      | All contributors & AI agents |
| **PATTERNS.md**                  | Pattern overviews + requirements + best usage                           | Feature development |
| **EDUCATIONAL-QUALITY-STANDARD.md** | What high-quality, reference-grade educational output looks like     | Documentation, blueprints, guides |
| **ECOSYSTEM.md**                 | Org map and relationships                                               | Onboarding & planning |
| **GLOSSARY.md**                  | Key Px terms and concepts                                               | Quick reference |
| **AI_PROMPTS.md**                | Specialized prompt templates for AI agents focused on Px/WAX/Web3       | Creating consistent AI collaborators |
| **CONTRIBUTING.md**              | How to contribute                                                       | New and returning contributors |
| **docs/**                        | Deep educational guides                                                 | Learning core topics deeply |
| **templates/**                   | Ready-to-use project scaffolds (Next.js dapp, analytics, etc.)         | Starting new Px projects |
| **.github/**                     | Org-wide templates                                                      | Hygiene |

---

## Core Architecture & Relationships

This handbook is the **central coordination layer** for the entire Pixel Journey ecosystem:

- It extracts generalizable patterns from real Px projects (PxWallet, Hot or Not, PxPackages...)
- It enforces consistency via `STANDARDS.md` and `PATTERNS.md`
- It enables high-quality AI collaboration via the `ai-prompts/` system
- It points to deeper educational content in `gitbook-docs` and `wax-ecosystem-blueprint-catalog`

**Key Related Repos** (all cross-linked):
- `pixel-journey-standards` — Foundational rules
- `pixel-journey-design-system` — Visual language & components
- `wax-ecosystem-blueprint-catalog` — WAX infrastructure blueprints
- `gitbook-docs` — Living knowledge base (this handbook feeds into it)

---

## Foundational Principles

Every project and contribution in Pixel Journey follows these **7 non-negotiable principles** (detailed in `STANDARDS.md`):

1. **ZERO Custom Contract Overhead** — Prefer client-side and existing on-chain primitives
2. **Client-Side Sovereignty** — Users control their experience and keys
3. **On-Chain Entropy for Randomness** — Fair, verifiable randomness
4. **WharfKit First** — Session Kit for seamless wallet integration
5. **Design System Alignment** — Consistent beautiful UI/UX
6. **Educational Excellence** — Every artifact teaches and empowers
7. **Config-Driven & Composable** — Flexible, maintainable architectures

---

## AI Collaboration Layer

We heavily use specialized AI agents. This repo includes high-quality prompt templates so custom agents can be instantiated with deep alignment to Px architecture, patterns, and educational standards.

**Available Specializations** (organized under `personas/`):

**Development & Architecture**
- `px-core-architect.md`
- `wax-client-specialist.md`
- `game-systems-designer.md`
- `wallet-security-engineer.md`
- `pxpackages-specialist.md`

**Design, Documentation & Feedback**
- `design-system-integrator.md`
- `educational-documenter.md`
- `critical-feedback-tester.md`
- `technical-writer.md`

**Content, Community & Education**
- `marketing-content-creator.md`
- `educational-support-bot.md`

See `AI_PROMPTS.md` for usage instructions, how to combine prompts, and the knowledge bank examples.

---

## How to Use This Handbook

- **New to Px?** Start with `ECOSYSTEM.md` + `GLOSSARY.md` + `AI_PROMPTS.md`.
- **Building features?** Check `PATTERNS.md` + relevant AI prompt.
- **Starting new work?** Follow `STANDARDS.md` + `EDUCATIONAL-QUALITY-STANDARD.md`.
- **Reviewing PRs?** Use checklists in `STANDARDS.md`.
- **Contributing improvements?** See `CONTRIBUTING.md` — we welcome pattern generalizations and new AI specializations.

---

## Living Document & Future Expansion

This handbook evolves with the ecosystem. New patterns, guides, or AI specializations are added only when they prove valuable through real work.

We prioritize **quality and usefulness** over trying to predict every possible need. The goal is a focused, high-signal reference that accelerates consistent, educational, production-grade Px development on WAX.

**This repo itself exemplifies the PX Perfection Standard** — comprehensive, educational, well-structured, and designed for long-term participants and AI collaborators.

---

**Built for the long-term health, consistency, velocity, and educational impact of the Pixel Journey ecosystem.**

*PxWallet • Px Hot or Not • Pixal PFPs • YEET • PxPackages • GitBook Knowledge Bank • WAX Public Infrastructure Blueprints*

**Pixel Journey — Perfecting the foundation for an extraordinary Web3 adventure.**