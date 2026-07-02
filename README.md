# pixel-journey-templates

**The Official Standards, Patterns, Ecosystem Handbook & AI Collaboration Templates for Pixel Journey (Px)**

[![WAX](https://img.shields.io/badge/WAX-Antelope-blue?logo=ethereum)](https://wax.io) [![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178c6?logo=typescript)](https://www.typescriptlang.org/) [![Next.js](https://img.shields.io/badge/Next.js-15+-000000?logo=nextdotjs)](https://nextjs.org/) [![WharfKit](https://img.shields.io/badge/WharfKit-Session%20Kit-orange)](https://wharfkit.com) [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> This is the single source of truth for **how we build** in the Pixel Journey organization — including how we collaborate with specialized AI agents.
> It defines the standards, recommended patterns, architectural principles, ecosystem overview, and AI prompt templates that keep every Px project consistent, high-quality, educational, and fast to develop.

**This repo contains the instructions, standards, pattern overviews, expected shapes, and AI collaboration templates** that all other repos in the `pixel-journey` organization follow (or are actively aligning to).

It works alongside:
- `pixel-journey-design-system` — The visual language, tokens, components, and detailed style guide
- `pixel-journey-standards` — Foundational engineering rules and Web3 best practices
- All individual Px repos (PxWallet, Hot or Not, PxPackages, docs, etc.)

---

## Relationship with Related Repos

- **`pixel-journey-design-system`**: Contains the detailed visual language, design tokens, component specifications, and style guide. This handbook references it heavily (especially in UI-related patterns and the `design-system-integrator.md` prompt) but does not duplicate its content.
- **`pixel-journey-standards`**: Contains foundational engineering and Web3 rules. This handbook builds on top of it with Px-specific enforcement, patterns, and educational guidance.
- **Individual Px Repos** (PxWallet, Hot or Not, etc.): These are the living implementations. We extract generalizable patterns and principles from them into this handbook, but we do not create project-specific deep summaries here.
- **`wax-ecosystem-blueprint-catalog`**: Planning and indexing catalog for individual WAX public infrastructure blueprint repositories. We share strong alignment on educational quality and have cross-referenced standards.

---

## Core Purpose

Pixel Journey is a complex, multi-disciplinary ecosystem. To maintain velocity and consistency while onboarding both human developers and AI collaborators, we maintain one authoritative handbook covering principles, patterns, ecosystem mapping, and specialized AI prompt templates.

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
| **.github/**                     | Org-wide templates                                                      | Hygiene |

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

---

## Living Document & Future Expansion

This handbook is designed to evolve with the ecosystem. New patterns, guides, or AI specializations will be added as they prove valuable through real work in PxWallet, Hot or Not, PxPackages, and community contributions.

We prioritize quality and usefulness over trying to predict every possible need in advance. The goal is to have a focused, high-signal reference that accelerates consistent, educational Px development.

---

**Built for the long-term health, consistency, and velocity of the Pixel Journey ecosystem.**

*PxWallet • Px Hot or Not • Pixal PFPs • YEET • PxPackages • GitBook Knowledge Bank*