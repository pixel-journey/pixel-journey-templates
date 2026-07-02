# AI_PROMPTS.md

**Specialized Prompt Templates for AI-Assisted Pixel Journey Development**

This document introduces reusable, high-quality prompt templates for creating specialized AI agents focused on different domains of Px, WAX, and Web3 development.

These templates help us (and future contributors) spin up consistent, aligned AI collaborators quickly.

## Philosophy

Pixel Journey development benefits enormously from specialized AI agents that deeply understand our principles, patterns, codebase style, and educational standards. Rather than using generic models for every task, we maintain a library of focused prompt templates.

## Quick Start

1. Go to the `ai-prompts/` folder.
2. Open the `.md` file for the specialization you need.
3. Copy the entire content.
4. Paste it as the system prompt (or initial context) in your AI tool (Grok, Claude, Cursor, etc.).
5. Optionally add current project-specific context on top (e.g. "We're currently working on the encrypted vault feature in PxWallet").
6. The agent will now operate with deep alignment to Px standards and patterns.

## Available Specializations

| Prompt File                        | Focus Area                                          | Recommended Use Cases                              |
|------------------------------------|-----------------------------------------------------|----------------------------------------------------|
| `px-core-architect.md`             | Overall Px architecture, principles, patterns, roadmap | High-level planning, major refactors, new features |
| `wax-client-specialist.md`         | WAX client-side (AtomicAssets, Hyperion, pagination, caching, GitOps) | Data layers, queries, performance, pipelines      |
| `game-systems-designer.md`         | Verifiable mechanics, on-chain entropy, Hot or Not, leaderboards, XP | Game features, randomness, progression systems     |
| `wallet-security-engineer.md`      | Encrypted vaults, key derivation, signing UX, self-custody | PxWallet features, cross-chain, security patterns  |
| `pxpackages-specialist.md`         | Monorepo structure, shared packages (@pxjourney/*), reusability | PxPackages development, extracting shared logic    |
| `educational-documenter.md`        | High-quality layered documentation                  | READMEs, guides, pattern documentation, onboarding |
| `design-system-integrator.md`      | Glassmorphic + pixel UI, design tokens, theming     | Frontend components, visual consistency            |

New specializations can be added as the ecosystem grows.

## Quality Bar for New Prompts

Any new AI prompt template added to this repo must:
- Explicitly reference the 7 Foundational Principles
- Reference `STANDARDS.md` and `PATTERNS.md`
- Emphasize educational output quality
- Be modular and composable where possible

See the `ai-prompts/` folder for the actual prompt files.