# pixel-journey-templates

**The Official Standards, Patterns, Ecosystem Handbook & AI Collaboration Templates for Pixel Journey (Px)**

[![WAX](https://img.shields.io/badge/WAX-Antelope-blue?logo=ethereum)](https://wax.io) [![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178c6?logo=typescript)](https://www.typescriptlang.org/) [![Next.js](https://img.shields.io/badge/Next.js-15+-000000?logo=nextdotjs)](https://nextjs.org/) [![WharfKit](https://img.shields.io/badge/WharfKit-Session%20Kit-orange)](https://wharfkit.com) [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> This is the single source of truth for **how we build** in the Pixel Journey organization — including how we collaborate with specialized AI agents.
> It defines the standards, recommended patterns, architectural principles, ecosystem overview, and AI prompt templates that keep every Px project consistent, high-quality, educational, and fast to develop.

**This repo contains the instructions, standards, pattern overviews, expected shapes, and AI collaboration templates** that all other repos in the `pixel-journey` organization follow (or are actively aligning to).

It works alongside:
- `pixel-journey-design-system`
- `pixel-journey-standards`
- All individual Px repos (PxWallet, Hot or Not, PxPackages, docs, etc.)

---

## Core Purpose

Pixel Journey is a complex, multi-disciplinary ecosystem. To maintain velocity and consistency while onboarding both human developers and AI collaborators, we maintain one authoritative handbook covering principles, patterns, ecosystem mapping, and specialized AI prompt templates.

---

## What You Will Find Here

| Section                  | Purpose                                                                 | Best For |
|--------------------------|-------------------------------------------------------------------------|----------|
| **STANDARDS.md**         | Rules, checklists, expected shapes                                      | All contributors & AI agents |
| **PATTERNS.md**          | Pattern overviews + requirements + best usage                           | Feature development |
| **ECOSYSTEM.md**         | Org map and relationships                                               | Onboarding & planning |
| **GLOSSARY.md**          | Key Px terms and concepts                                               | Quick reference |
| **AI_PROMPTS.md**        | Specialized prompt templates for AI agents focused on Px/WAX/Web3       | Creating consistent AI collaborators |
| **CONTRIBUTING.md**      | How to contribute                                                       | New and returning contributors |
| **docs/**                | Deep educational guides                                                 | Learning core topics deeply |
| **.github/**             | Org-wide templates                                                      | Hygiene |

---

## Foundational Principles

Every project and contribution in Pixel Journey is expected to follow the 7 non-negotiable principles (detailed in `STANDARDS.md`):

1. ZERO Custom Contract Overhead
2. Client-Side Sovereignty
3. On-Chain Entropy for Randomness
4. WharfKit First
5. Design System Alignment
6. Educational Excellence
7. Config-Driven & Composable

---

## AI Collaboration Layer

We heavily use specialized AI agents. This repo includes high-quality prompt templates (`ai-prompts/`) so custom agents can be instantiated with deep alignment to Px architecture, patterns, and educational standards.

**Available Specializations**:
- `px-core-architect.md` — Overall Px architecture, principles, patterns, roadmap
- `wax-client-specialist.md` — WAX client-side (AtomicAssets, Hyperion, pagination, caching, GitOps)
- `game-systems-designer.md` — Verifiable mechanics, on-chain entropy, Hot or Not, leaderboards, XP
- `educational-documenter.md` — High-quality layered documentation
- `design-system-integrator.md` — Glassmorphic + pixel UI, design tokens, theming

See `AI_PROMPTS.md` for usage instructions and how to create new specializations.

---

## How to Use This Handbook

- **New to Px?** Start with `ECOSYSTEM.md` + `GLOSSARY.md` + `AI_PROMPTS.md`.
- **Building features?** Check `PATTERNS.md` + relevant AI prompt.
- **Starting new work?** Follow `STANDARDS.md`.
- **Reviewing PRs?** Use checklists in `STANDARDS.md`.

---

## Living Document

This handbook is designed to evolve with the ecosystem. New patterns, guides, or AI specializations will be added as they prove valuable through real work in PxWallet, Hot or Not, PxPackages, and community contributions.

We prioritize quality and usefulness over completeness. The goal is to have a focused, high-signal reference that accelerates consistent, educational Px development.

---

**Built for the long-term health, consistency, and velocity of the Pixel Journey ecosystem.**

*PxWallet • Px Hot or Not • Pixal PFPs • YEET • PxPackages • GitBook Knowledge Bank*