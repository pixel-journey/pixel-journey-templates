# pixel-journey-templates

**The Official Standards, Patterns & Ecosystem Handbook for Pixel Journey (Px)**

[![WAX](https://img.shields.io/badge/WAX-Antelope-blue?logo=ethereum)](https://wax.io) [![TypeScript](https://img.shields.io/badge/TypeScript-Strict-3178c6?logo=typescript)](https://www.typescriptlang.org/) [![Next.js](https://img.shields.io/badge/Next.js-15+-000000?logo=nextdotjs)](https://nextjs.org/) [![WharfKit](https://img.shields.io/badge/WharfKit-Session%20Kit-orange)](https://wharfkit.com) [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> This is the single source of truth for **how we build** in the Pixel Journey organization.
> It defines the standards, recommended patterns, architectural principles, and ecosystem overview that keep every Px project consistent, high-quality, educational, and fast to develop — for the core team and every future contributor.

**This repo does not contain hundreds of cloneable boilerplates.** It contains the **instructions, standards, pattern overviews, and expected shapes** that all other repos in the `pixel-journey` organization follow (or are in the process of fully aligning to).

It works alongside:
- `pixel-journey-design-system` — The visual language, tokens, and components
- `pixel-journey-standards` — Foundational engineering & Web3 rules
- All the individual Px repos (PxWallet, Hot or Not, PxPackages, docs, etc.)

---

## Core Purpose

As the Pixel Journey ecosystem grows (PxWallet, Px Hot or Not, Pixal PFPs, YEET, PxTicker, PxPackages, GitBook knowledge bank, and many community contributions), we need one place that answers:

- What are the non-negotiable principles every Px project must follow?
- What are the recommended patterns for common tasks (session management, on-chain actions, UI shells, verifiable mechanics, data handling)?
- What does a "well-formed" Px repo or package look like?
- How do all the pieces of the ecosystem fit together?
- How do we maintain pixel-perfect consistency and educational excellence at scale?

This handbook is the answer.

---

## What You Will Find Here

| Section                  | Purpose                                                                 | Best For |
|--------------------------|-------------------------------------------------------------------------|----------|
| **STANDARDS.md**         | The rules, checklists, and expected shapes for Px work                 | Contributors, maintainers, AI agents |
| **PATTERNS.md**          | Overviews + requirements of recommended implementation approaches      | Feature development, consistency reviews |
| **ECOSYSTEM.md**         | Map of all major Px repos, how they relate, and their current maturity | Onboarding, planning, discovering where to contribute |
| **GLOSSARY.md**          | Definitions of key Px terms and concepts                               | New contributors and quick reference |
| **CONTRIBUTING.md**      | How to contribute to this handbook and the wider ecosystem             | New and returning contributors |
| **docs/**                | Deeper educational guides (WAX client-side, on-chain entropy, etc.)    | Learning the "Px way" deeply |
| **.github/**             | Org-wide issue, PR, workflow, and repo templates                       | New repos and contribution hygiene |

---

## Foundational Principles (Non-Negotiable)

Every project, package, and contribution in the Pixel Journey org is expected to embody these:

1. **ZERO Custom Contract Overhead** — We maximize existing public WAX/Antelope primitives (`atomicassets`, `alcorammswap`, `eosio.msig`, `eosio.token`, Hyperion, etc.). Custom contracts are a last resort only.
2. **Client-Side Sovereignty** — Public indexing APIs + local state + intelligent caching. No unnecessary centralized backends for public data.
3. **On-Chain Entropy for Randomness** — All game mechanics and randomness use deterministic, client-side parsing of transaction hashes + block headers (provably fair, zero RAM/oracle cost).
4. **WharfKit First** — Session Kit, Contract Kit, and Account Kit. No legacy UAL, eosjs, or deprecated Anchor patterns.
5. **Design System Alignment** — All UI work consumes and extends the patterns from `pixel-journey-design-system` (glassmorphic + optional retro-pixel/CRT aesthetic).
6. **Educational Excellence** — Every repo, major file, and pattern includes layered, scannable documentation. New developers (human or AI) should be able to understand *why* decisions were made.
7. **Config-Driven & Composable** — Features are tunable via config where possible. Patterns are modular and reusable across Px projects.

These principles are not suggestions. They are the foundation that makes the entire ecosystem coherent and trustworthy.

---

## How to Use This Handbook

- **New to Px?** Start with `ECOSYSTEM.md` + `GLOSSARY.md` + Foundational Principles.
- **Building a feature?** Check the relevant section in `PATTERNS.md` first.
- **Starting a new repo or package?** Follow `STANDARDS.md` + expected shape.
- **Reviewing code or PRs?** Use the checklists in `STANDARDS.md`.
- **Want to contribute?** See `CONTRIBUTING.md`.

---

## Current Status & Philosophy

The Pixel Journey organization currently contains many active repositories at various stages of maturity. This handbook documents the **target state** — the standards and patterns we are aligning everything toward.

We document patterns at the level of "requirements + best expected usage + key decisions" rather than shipping hundreds of full boilerplates here. The actual production implementations live in their respective repos and are expected to embody (or be actively migrating toward) the guidance in this handbook.

This approach keeps the handbook focused, maintainable, and authoritative.

---

## Next Steps for This Repo

This handbook is a living document. As the ecosystem matures, we will:
- Expand `PATTERNS.md` with additional high-value patterns as they emerge from real development
- Add more educational guides under `docs/` when topics warrant deeper treatment
- Keep `GLOSSARY.md`, `STANDARDS.md`, and `ECOSYSTEM.md` updated
- Maintain extremely high documentation quality across the org

---

**Built for the long-term health, consistency, and velocity of the Pixel Journey ecosystem.**

*PxWallet • Px Hot or Not • Pixal PFPs • YEET • PxPackages • GitBook Knowledge Bank*