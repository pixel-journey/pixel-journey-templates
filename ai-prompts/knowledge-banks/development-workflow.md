# Px Development Workflow Knowledge Bank

**Pre-filled Knowledge Bank for General Pixel Journey Development Workflow**

Use this alongside `px-core-architect.md`, `educational-support-bot.md`, or any persona when you need context on how we typically work.

## Typical Development Flow

1. **Understand the problem** — Read relevant handbook sections (`STANDARDS.md`, `PATTERNS.md`, `EDUCATIONAL-QUALITY-STANDARD.md`)
2. **Check existing patterns** — Look in `PATTERNS.md` first before inventing new approaches
3. **Use AI personas + knowledge banks** — Pair the right persona with relevant knowledge banks for higher quality output
4. **Build iteratively** — Focus on core logic + one major interactive component first
5. **Document as you go** — Layered documentation (why → how → examples)
6. **Polish & test** — Code quality, accessibility, DX, and educational clarity
7. **Review against standards** — Use the contribution checklist

## Recommended Tools & Practices

- **AI Collaboration**: Use personas from `ai-prompts/personas/` + knowledge banks from `knowledge-banks/`
- **State Management**: Zustand for client state, TanStack Query for server/async state
- **Styling**: Tailwind + `pixel-journey-design-system` tokens/components + Framer Motion
- **Testing**: Vitest for logic, Playwright for critical flows
- **Documentation**: Layered explanations with clear "Why" sections

## Common Pitfalls to Avoid

- Building custom solutions when good patterns already exist in `PATTERNS.md`
- Skipping documentation until the end
- Ignoring the 7 Foundational Principles
- Creating one-off UI components instead of using/extending the design system
- Not pairing AI personas with relevant knowledge banks

## References
- `STANDARDS.md`
- `PATTERNS.md`
- `EDUCATIONAL-QUALITY-STANDARD.md`
- `ai-prompts/` + `knowledge-banks/`

## Benefits
- More consistent development process across the team
- Higher quality output with less rework
- Better onboarding for new contributors (human or AI)

Create similar focused knowledge banks for other high-priority areas as needed.