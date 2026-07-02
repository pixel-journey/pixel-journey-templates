# Getting Started with Pixel Journey Development

**A Practical Guide for Humans and AI Agents**

This guide helps you quickly get oriented and start contributing effectively to the Pixel Journey ecosystem, whether you're a human developer or using specialized AI agents.

## 1. Understand the Big Picture

Start here:
- Read the root `README.md` for the overall vision and philosophy.
- Review `ECOSYSTEM.md` to see how the major Px repos relate to each other.
- Skim `GLOSSARY.md` for key terms used across the ecosystem.

## 2. Learn the Rules (Non-Negotiable)

Before writing any code or making contributions:
- Read `STANDARDS.md` thoroughly. These are the rules and expected shapes for all Px work.
- Understand the 7 Foundational Principles (ZERO custom contracts, client-side first, on-chain entropy, WharfKit only, design system alignment, educational excellence, config-driven).

These principles govern everything we build.

## 3. Learn the Recommended Patterns

- Read `PATTERNS.md` to understand the reusable approaches we prefer for common problems (session management, verifiable randomness, asset handling, UI shells, leaderboards, etc.).
- These patterns help keep the ecosystem consistent and high-quality.

## 4. Set Up Your AI Collaboration (Strongly Recommended)

We heavily use specialized AI agents. This dramatically improves speed and consistency:
- Read `AI_PROMPTS.md` and the prompts in `ai-prompts/`.
- Start with `px-core-architect.md` for high-level planning and architecture work.
- Use `educational-documenter.md` when creating or improving documentation.
- Use domain-specific prompts (e.g. `game-systems-designer.md`, `wallet-security-engineer.md`) when working in those areas.

You can combine prompts (e.g. Core Architect + Game Systems) for complex tasks.

## 5. Start Contributing

- Follow the process in `CONTRIBUTING.md`.
- Always check `STANDARDS.md` and relevant patterns before implementing.
- Update documentation and patterns when you discover something reusable.
- Use the PR template — it enforces handbook alignment.

## Recommended First Tasks

Depending on your goal:

- **New to Px overall** — Start by exploring existing repos while referencing the handbook.
- **Want to build a feature** — Use the relevant pattern from `PATTERNS.md` + appropriate AI prompt.
- **Improving documentation** — Use `educational-documenter.md` prompt.
- **Working on PxWallet** — Start with `wallet-security-engineer.md` + relevant patterns.
- **Working on game mechanics / Hot or Not** — Use `game-systems-designer.md`.
- **Working on shared packages** — Use `pxpackages-specialist.md`.

## Quick Reference

| Goal                              | Start Here                              |ecommended AI Prompt              |
|-----------------------------------|-----------------------------------------|------------------------------------|
| High-level planning / architecture | Root README + STANDARDS + PATTERNS     | `px-core-architect.md`            |
| WAX data / queries / GitOps       | `docs/WAX_CLIENT_SIDE_PATTERNS.md`     | `wax-client-specialist.md`        |
| Game mechanics / verifiable randomness | `docs/ONCHAIN_ENTROPY_GUIDE.md`   | `game-systems-designer.md`        |
| Wallet / security / self-custody  | Relevant patterns in `PATTERNS.md`     | `wallet-security-engineer.md`     |
| Documentation / explanations      | This guide + existing docs             | `educational-documenter.md`       |
| UI / theming / design consistency | `pixel-journey-design-system` repo     | `design-system-integrator.md`     |
| Shared packages / monorepo        | Future PxPackages direction            | `pxpackages-specialist.md`        |

Welcome to Pixel Journey. We're building something ambitious, educational, and fun — and this handbook exists to help us do it consistently and at high velocity.