# templates/

**The home of Design Templates, Feature Pattern Templates, and Scaffolding that make consistent, fast Px development possible.**

This directory contains everything that helps the Pixel Journey team and future contributors build UIs and features that feel native to Px — quickly, correctly, and with shared understanding.

## Philosophy

- **Design consistency first** — Leverage and extend `pixel-journey-design-system`
- **Implementation patterns** — Solve common Px problems once (session, assets, verifiable actions, modals, leaderboards, entropy) with excellent docs
- **Speed with quality** — New features and mini-dApps can be assembled from these building blocks instead of starting from zero every time
- **Educational** — Every template teaches *why* we do things the Px way (client-side, WharfKit, on-chain entropy, glassmorphic + pixel aesthetic)

The documentation quality bar is inspired by excellent examples like the gkniftyheads-tracker we explored — layered, scannable, decision matrices, full context.

## Current Categories

| Folder                  | Purpose                                                                 | Priority |
|-------------------------|-------------------------------------------------------------------------|----------|
| `design-ui/`            | Reusable UI shells, components, and visual patterns (cards, modals, galleries, leaderboards, theme toggles) | P0 |
| `feature-patterns/`     | Modular implementation patterns (WharfKit session, verifiable randomness, asset caching, on-chain action UX, voting shells) | P0 |
| `nextjs-dapp/`          | Full Next.js 15 + WharfKit dApp starter shell                           | P1 |
| `monorepo-pkg/`         | Starter for future @pxjourney/* packages (aligned with PxPackages)      | P1 |
| `github-org/`           | GitHub repo bootstrap helpers                                           | P0 |
| `documentation/`        | Templates for GitBook, README standards, interactive docs               | P2 |

## How to Use

1. Browse the category that matches what you need to build.
2. Copy the template folder or specific files into your project.
3. Follow the template's README for integration with Design System + Px principles.
4. Customize via config or extension points.

New templates must include their own deep README with usage, architecture decisions, and Px alignment notes.

See root `CONTRIBUTING.md` for the full quality checklist.