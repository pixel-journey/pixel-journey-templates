# ai-prompts/

**Specialized Prompt Templates for AI-Assisted Pixel Journey Development**

This folder contains high-quality, reusable system prompt templates designed to create focused AI agents aligned with Pixel Journey principles, patterns, and standards.

## Purpose

These prompts allow us to quickly instantiate specialized AI collaborators for different domains of Px development. Instead of starting from a generic model every time, we use these templates to ensure consistency, depth, and adherence to our architectural and educational standards.

## How to Use

1. Open the desired `.md` file.
2. Copy its entire content.
3. Paste it as the system prompt (or starting context) in your AI tool (Grok, Claude, Cursor, etc.).
4. Optionally add current project-specific context on top.

## Available Templates

### Development & Architecture
- `px-core-architect.md` — Overall Px architecture, principles, patterns, and high-level planning
- `wax-client-specialist.md` — WAX client-side development (AtomicAssets, Hyperion, pagination, caching, GitOps)
- `game-systems-designer.md` — Verifiable game mechanics, on-chain entropy, Hot or Not, leaderboards, progression
- `wallet-security-engineer.md` — Encrypted vaults, key derivation, signing UX, self-custody
- `pxpackages-specialist.md` — Monorepo structure, shared packages (@pxjourney/*), reusability

### Design, Documentation & Feedback
- `design-system-integrator.md` — Glassmorphic + pixel UI, design tokens, theming
- `educational-documenter.md` — High-quality layered documentation and explanations
- `critical-feedback-tester.md` — Rigorous qualitative feedback and testing

## Contributing New Templates

We welcome expansion into new domains (marketing/content creation, educational support bots, knowledge-bank templates, etc.). When adding one:
- Follow the existing style and quality bar
- Update `AI_PROMPTS.md` and this file
- Reference the 7 Foundational Principles and relevant handbook sections

See `AI_PROMPTS.md` (in the repo root) for the full index, usage guidance, and how to combine prompts.