# AI_PROMPTS.md

**Specialized Prompt Templates for AI-Assisted Pixel Journey Development**

This document introduces reusable, high-quality prompt templates for creating specialized AI agents focused on different domains of Px, WAX, and Web3 development — including development, design, documentation, feedback, marketing/content, education, and more.

These templates help us (and future contributors) spin up consistent, aligned AI collaborators quickly.

## Philosophy

Pixel Journey development benefits enormously from specialized AI agents that deeply understand our principles, patterns, codebase style, and educational standards. Rather than using generic models for every task, we maintain a library of focused prompt templates across multiple skill domains. We also support pairing these personas with pre-filled knowledge banks for even higher quality and consistency.

## Quick Start

1. Go to the `ai-prompts/` folder.
2. Open the desired persona `.md` file.
3. Optionally include a knowledge bank from `ai-prompts/knowledge-banks/`.
4. Paste as the system prompt in your AI tool.
5. Add current project context if needed.
6. The agent will now operate with deep alignment to Px standards and patterns.

## How to Combine Prompts + Knowledge Banks

You can combine multiple prompt templates and optionally attach a knowledge bank. Examples:

- **Core Architect + Game Systems Designer** + Game Systems knowledge bank — Planning a new Hot or Not feature.
- **Critical Feedback Tester + any development prompt** — Getting rigorous qualitative feedback.
- **Educational Support Bot** + relevant knowledge bank — Helping new contributors learn the ecosystem.

See `ai-prompts/knowledge-banks/example.md` for an example structure.

## Available Specializations

### Development & Architecture
| Prompt File                        | Focus Area                                          | Recommended Use Cases                              |
|------------------------------------|-----------------------------------------------------|----------------------------------------------------|
| `px-core-architect.md`             | Overall Px architecture, principles, patterns, roadmap | High-level planning, major refactors, new features |
| `wax-client-specialist.md`         | WAX client-side (AtomicAssets, Hyperion, pagination, caching, GitOps) | Data layers, queries, performance, pipelines      |
| `game-systems-designer.md`         | Verifiable mechanics, on-chain entropy, Hot or Not, leaderboards, XP | Game features, randomness, progression systems     |
| `wallet-security-engineer.md`      | Encrypted vaults, key derivation, signing UX, self-custody | PxWallet features, cross-chain, security patterns  |
| `pxpackages-specialist.md`         | Monorepo structure, shared packages (@pxjourney/*), reusability | PxPackages development, extracting shared logic    |

### Design, Documentation & Feedback
| Prompt File                        | Focus Area                                          | Recommended Use Cases                              |
|------------------------------------|-----------------------------------------------------|----------------------------------------------------|
| `design-system-integrator.md`      | Glassmorphic + pixel UI, design tokens, theming     | Frontend components, visual consistency            |
| `educational-documenter.md`        | High-quality layered documentation                  | READMEs, guides, pattern documentation, onboarding |
| `critical-feedback-tester.md`      | Rigorous qualitative feedback and testing           | Code reviews, UI/UX feedback, documentation review |

### Content, Community & Education
| Prompt File                        | Focus Area                                          | Recommended Use Cases                              |
|------------------------------------|-----------------------------------------------------|----------------------------------------------------|
| `marketing-content-creator.md`     | Marketing, X content, educational threads, release notes | Announcements, community content, explainers      |
| `educational-support-bot.md`       | Onboarding help, explaining concepts, getting unstuck | New contributors, learning the ecosystem          |

New specializations and knowledge banks can be added as the ecosystem grows.

## Quality Bar for New Prompts

Any new AI prompt template added to this repo must:
- Explicitly reference the 7 Foundational Principles
- Reference `STANDARDS.md` and `PATTERNS.md`
- Emphasize educational output quality
- Be modular and composable where possible

See the `ai-prompts/` folder for the actual prompt files and knowledge banks.