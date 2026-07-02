# AI_PROMPTS.md

**Specialized Prompt Templates (Personas) for AI-Assisted Pixel Journey Development**

This document introduces reusable, high-quality prompt templates for creating specialized AI agents focused on different domains of Px, WAX, and Web3 development.

These templates help us spin up consistent, aligned AI collaborators quickly. We also support pairing personas with pre-filled knowledge banks for even higher quality and consistency.

See `EDUCATIONAL-QUALITY-STANDARD.md` for the broader quality expectations around educational output and documentation.

## Recommended Structure

Personas are organized under `ai-prompts/personas/` in categorized subfolders:
- `development-architecture/`
- `design-documentation-feedback/`
- `content-community-education/`

Knowledge banks live in `ai-prompts/knowledge-banks/`.

## Quick Start

1. Go to `ai-prompts/personas/<category>/` and open the desired persona.
2. Optionally include a knowledge bank from `knowledge-banks/`.
3. Paste as the system prompt in your AI tool.
4. Add current project context if needed.

## How to Combine Prompts + Knowledge Banks

You can combine multiple personas and attach knowledge banks. Examples:

- **Core Architect + Game Systems Designer** + Hot or Not knowledge bank — Planning a new Hot or Not feature.
- **Critical Feedback Tester + any development prompt** — Getting rigorous qualitative feedback.
- **Educational Support Bot** + Educational Support or Px Fundamentals knowledge bank — Helping new contributors learn the ecosystem.
- **Technical Writer + any persona** — Generating high-quality layered documentation.

See `ai-prompts/knowledge-banks/` for available knowledge banks.

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
| `technical-writer.md`              | Clear, layered, high-quality documentation          | Educational guides, architecture overviews, specs  |

### Content, Community & Education
| Prompt File                        | Focus Area                                          | Recommended Use Cases                              |
|------------------------------------|-----------------------------------------------------|----------------------------------------------------|
| `marketing-content-creator.md`     | Marketing, X content, educational threads, release notes | Announcements, community content, explainers      |
| `educational-support-bot.md`       | Onboarding help, explaining concepts, getting unstuck | New contributors, learning the ecosystem          |

New specializations and knowledge banks can be added as the ecosystem grows.

## Quality Bar for New Prompts

Any new AI prompt template added to this repo must:
- Explicitly reference the 7 Foundational Principles
- Reference `STANDARDS.md`, `PATTERNS.md`, and `EDUCATIONAL-QUALITY-STANDARD.md`
- Emphasize educational output quality
- Be modular and composable where possible

See `ai-prompts/README.md` for the recommended folder structure.