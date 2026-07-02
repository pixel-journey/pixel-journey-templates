# STANDARDS.md

**Standards, Rules, and Expected Repository Shapes for Pixel Journey**

This document defines the non-negotiable rules and expected shapes for all work in the Pixel Journey organization. Every contribution and project should follow these standards.

See `EDUCATIONAL-QUALITY-STANDARD.md` for the broader quality expectations around educational output and documentation.

---

## The 7 Foundational Principles

These principles govern all human and AI-assisted work in Pixel Journey. They are non-negotiable unless there is an extremely strong, documented reason otherwise.

1. **ZERO Custom Contract Overhead** — Maximize existing public primitives (atomicassets, alcorammswap, eosio.msig, Hyperion). Avoid new smart contracts unless absolutely unavoidable.
2. **Client-Side Sovereignty** — Rely entirely on public indexing (Hyperion, AtomicAssets API), local browser storage, and client-side processing. Use GitOps for data pipelines.
3. **On-Chain Entropy for Randomness** — For all randomized game mechanics, use deterministic client-side parsing of WharfKit broadcast transaction hashes combined with block headers.
4. **WharfKit First** — Use WharfKit (Session Kit, Account Kit, Contract Kit) exclusively. No legacy UAL, eosjs, or deprecated libraries.
5. **Design System Alignment** — Base all UI work on tokens and primitives from `pixel-journey-design-system`. Maintain glassmorphic + optional retro-pixel aesthetic.
6. **Educational Excellence** — Every output must be exceptionally clear, layered, and educational. New developers (human or AI) must understand *why* every decision was made.
7. **Config-Driven & Composable** — Everything should be tunable via config where possible. Prefer modular, reusable components.

---

## Expected Repository Shape

All Px repos should generally follow this structure (adjusted for project needs):

- Clear `README.md` with positioning, principles, and how to get started
- `STANDARDS.md` and `PATTERNS.md` references (or direct adoption from this handbook)
- Proper TypeScript strict mode and clean builds
- Use of WharfKit for all on-chain interactions
- Alignment with `pixel-journey-design-system` for UI work
- Educational comments and documentation quality
- Proper `.github/` templates (PR template referencing this handbook)

---

## Contribution Checklist

Before submitting a PR, ensure:

- [ ] Follows the 7 Foundational Principles
- [ ] Uses patterns from `PATTERNS.md` where applicable
- [ ] Aligns with `pixel-journey-design-system` for UI
- [ ] Includes or updates educational documentation where relevant
- [ ] Passes linting, TypeScript checks, and builds cleanly
- [ ] References this handbook where decisions are explained

---

## AI Collaboration Expectations

When working with AI agents:

- Use the specialized prompt templates from `ai-prompts/`
- Pair personas with relevant knowledge banks when available
- Expect outputs to follow the educational and structural standards in this handbook and `EDUCATIONAL-QUALITY-STANDARD.md`
- Review AI-generated work against the 7 Foundational Principles

These standards will evolve as the ecosystem grows. Major changes should be discussed and documented here.