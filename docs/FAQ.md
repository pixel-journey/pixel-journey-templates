# FAQ

**Frequently Asked Questions about Pixel Journey Development**

## General

**Q: What is this handbook for?**
A: This is the single source of truth for how we build in the Pixel Journey organization. It defines standards, recommended patterns, architectural principles, and specialized AI prompt templates to keep every Px project consistent, high-quality, educational, and fast to develop.

**Q: Do I need to read everything before contributing?**
A: No. Start with `GETTING_STARTED.md` + `ECOSYSTEM.md` + `GLOSSARY.md`. Then dive into `STANDARDS.md` and the relevant patterns in `PATTERNS.md` as you work.

**Q: How does this relate to `pixel-journey-design-system` and `pixel-journey-standards`?**
A: `pixel-journey-design-system` is the source of truth for visual language and components. `pixel-journey-standards` contains foundational engineering rules. This handbook builds on both with Px-specific patterns, enforcement, and educational guidance.

## AI Collaboration

**Q: How do I use the AI prompt templates?**
A: Copy the content of a prompt file from `ai-prompts/` and paste it as the system prompt in your AI tool (Grok, Claude, Cursor, etc.). You can combine multiple prompts and optionally attach a knowledge bank.

**Q: Can I create new AI personas?**
A: Yes. Follow the quality bar in `AI_PROMPTS.md`, add the new prompt to `ai-prompts/`, and update `AI_PROMPTS.md` and `ai-prompts/README.md`.

**Q: What is a knowledge bank?**
A: A pre-filled structured document with key concepts, patterns, and references for a specific domain. Pairing it with a persona improves consistency and reduces hallucination on Px-specific topics. See `knowledge-bank-example.md`.

## Patterns & Development

**Q: Why are there no project-specific deep dives here (e.g., full PxWallet or Hot or Not architecture)?**
A: This handbook focuses on generalizable standards and patterns. Project-specific details belong in their respective repos. We extract reusable patterns from active development into this handbook.

**Q: How do I propose a new pattern?**
A: Open a PR with a clear description of the problem, the proposed solution, requirements, and best expected usage. Follow the style in `PATTERNS.md`.

**Q: Do I have to use WharfKit / on-chain entropy / the design system?**
A: Yes for most cases. These are part of the non-negotiable 7 Foundational Principles. Exceptions require strong justification and review.

## Contributing

**Q: How do I contribute?**
A: Follow the process in `CONTRIBUTING.md` and always check `STANDARDS.md` first. Use the PR template.

**Q: Where should I ask questions?**
A: For general questions, start in the relevant GitHub discussion or reach out to the core team. For AI-assisted work, the `educational-support-bot.md` persona can help.

This FAQ will grow over time as new questions arise from real usage.