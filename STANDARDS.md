# STANDARDS.md

**Pixel Journey Development Standards & Expected Shapes**

This document defines the non-negotiable rules and the target shape for all work across the Pixel Journey GitHub Organization.

## 1. Foundational Principles (Must Follow)

See the root `README.md` for the seven core principles. They are repeated here for emphasis because they govern everything:

- ZERO Custom Contract Overhead
- Client-Side Sovereignty
- On-Chain Entropy for Randomness
- WharfKit First (no legacy auth libs)
- Design System Alignment
- Educational Excellence at every layer
- Config-Driven & Composable

Any PR or new repo that violates these will be asked to realign.

## 2. Repository Shape (Target State)

A well-formed Px repository should contain:

- Clear root `README.md` with vision, quickstart, architecture overview, and contribution guide
- `CONTRIBUTING.md` (or link to org standards)
- `.github/` with appropriate issue/PR templates and workflows
- Strict TypeScript (no `any` except in very narrow justified cases)
- Comprehensive interfaces/types for all domain concepts (assets, sessions, on-chain actions, etc.)
- Layered documentation (big picture → specific decisions → inline comments)
- Working demo or example mode where applicable
- Alignment with `pixel-journey-design-system` for all UI work

## 3. Code Quality Bar

- Prefer composition and small, focused modules
- State management: Zustand for client state, TanStack Query for server/async state
- Styling: Tailwind + design-system tokens/components + Framer Motion for motion
- Testing: Vitest for unit/logic, Playwright for critical flows (where relevant)
- No unnecessary dependencies. Every added package must be justified.

## 4. Documentation Standards

Every significant pattern, component, or feature must have:
- A clear "Why" section (architectural rationale)
- Usage example
- Customization / extension points
- Relationship to other Px patterns or repos

The documentation quality target is extremely high — inspired by the best educational examples in the broader WAX ecosystem.

## 5. On-Chain & Web3 Patterns

- Always use public endpoints with fallbacks
- Cursor-based pagination for large collections
- Preserve `template_mint` when working with AtomicAssets (critical for surviving mint rank and early minter recognition)
- All randomness in games/features must be derivable client-side from TX hash + recent block header
- User actions that change chain state must have clear loading, error, and success states

## 6. Contribution & Review Checklist

Before merging, verify:
- [ ] Aligns with Foundational Principles
- [ ] Follows expected repository shape
- [ ] Documentation is layered and educational
- [ ] Design System tokens/components used (or clear justification)
- [ ] No legacy auth libraries
- [ ] Educational value for future Px devs has been considered

This checklist lives in PR templates and is enforced culturally.