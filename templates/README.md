# templates/

**The Official Home of Design Templates, Feature Pattern Templates, and Scaffolding for Pixel Journey (Px)**

> **This directory contains everything that helps the Pixel Journey team and future contributors build UIs and features that feel native to Px — quickly, correctly, consistently, and with shared understanding.**

Every template here is designed to accelerate development while enforcing the highest standards of educational quality, client-side sovereignty, beautiful design-system alignment, and production readiness.

This folder is a core part of the `pixel-journey-templates` handbook and directly supports the broader Pixel Journey vision of extraordinary, educational Web3 experiences on WAX.

---

## Important Distinction: Px Templates vs `wax-*` Educational Blueprints

**This templates repository is primarily for Px-internal development patterns** (tight design system alignment, shared components, production PxPortals work).

For the public **WAX Blueprint Catalog** (`wax-*` repos):

- Follow the rules in [pixel-journey-standards/standards/REPO_TYPES_AND_STYLING_GUIDELINES.md](https://github.com/pixel-journey/pixel-journey-standards/blob/main/standards/REPO_TYPES_AND_STYLING_GUIDELINES.md)
- Use **plain Tailwind CSS only** (no Px classes)
- Optimize for maximum educational clarity, accessibility, and copy-paste value for the broader WAX community

This separation keeps community blueprints welcoming and timeless while allowing internal Px work to use the full design system.

---

## Vision & Philosophy

We believe the fastest way to high-quality, consistent Px development is to **solve common problems once** — beautifully, educationally, and reusably — so that every new feature, mini-dApp, or package starts from a strong, aligned foundation instead of from zero.

**Core Principles for All Templates**:
- **Design System First** — Every UI element extends or references `pixel-journey-design-system`
- **Educational by Default** — Every template teaches *why* we do things the Px way (client-side logic, WharfKit, on-chain entropy, glassmorphic + pixel aesthetic, verifiable actions)
- **Config-Driven & Composable** — Flexible extension points, not rigid monoliths
- **Production-Ready Patterns** — Real-world patterns extracted from PxWallet, Hot or Not, PxPackages, and WAX public infrastructure
- **Long-Term Maintainability** — Clear architecture decisions, decision matrices, and upgrade paths

These templates are not just starters — they are **living references** that embody the PX Perfection Standard.

---

## Quick Starts

### For Developers Starting a New Feature or dApp
1. Identify the category you need (design-ui, feature-patterns, or full starter)
2. Copy the relevant template folder into your project
3. Read the template's own README.md for integration steps
4. Customize via config/extension points while preserving Px alignment
5. Run the included examples and verify against `EDUCATIONAL-QUALITY-STANDARD.md`

### For AI Agents Generating Code
- Use the `px-core-architect.md` or `pxpackages-specialist.md` persona
- Reference this `templates/` structure and the specific template READMEs
- Always align generated code to the principles above and `STANDARDS.md`

### For Reviewers & Maintainers
- Verify every new or updated template has a deep, scannable README with usage, architecture decisions, Px alignment, and educational notes
- Ensure no duplication with `pixel-journey-design-system`
- Confirm the template generalizes patterns from real Px work

---

## Recommended Starter for `wax-*` Educational Blueprints

For most new public `wax-*` visualizers, simulators, analyzers, or tool repos (not full Next.js dApps):

**Use this minimal, education-first baseline** (Tailwind via CDN for instant clarity):

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>[Blueprint Name] — WAX Educational Blueprint</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style> /* optional small custom styles for retro-pixel feel */ </style>
</head>
<body class="bg-zinc-950 text-zinc-200">
  <!-- Your content here -->
</body>
</html>
```

**README language to use** (copy and adapt):

> This is a clean, educational reference implementation demonstrating [specific pattern] using public WAX primitives (AtomicAssets / Hyperion / Alcor / WharfKit). Styled with vanilla Tailwind for maximum accessibility and clarity for the broader WAX developer community.

See the full guidelines in `pixel-journey-standards`.

---

## Current Categories & Templates

| Category              | Purpose                                                                 | Status     | Key Examples / Notes |
|-----------------------|-------------------------------------------------------------------------|------------|----------------------|
| `design-ui/`          | Reusable UI shells, components, visual patterns (cards, modals, galleries, leaderboards, theme toggles, glassmorphic effects) | Active    | Extend design-system tokens and components |
| `feature-patterns/`   | Modular implementation patterns (WharfKit session handling, verifiable randomness/entropy, asset caching, on-chain action UX, voting/leaderboard shells, permission flows) | Active    | Extracted from real Px projects |
| `nextjs-dapp/`        | Full Next.js 15 + WharfKit + TypeScript dApp starter shell             | Active    | Production-ready starting point |
| `monorepo-pkg/`       | Starter for future `@pxjourney/*` packages (aligned with PxPackages)   | Planned   | For shared logic and components |
| `github-org/`         | GitHub repo bootstrap helpers and org-level templates                  | Active    | Supports consistent repo hygiene |
| `documentation/`      | Templates for GitBook guides, README standards, interactive docs       | Active    | Supports educational excellence |

**Note**: Individual template folders each contain their own detailed `README.md` with usage instructions, architecture decisions, Px alignment notes, and runnable examples.

---

## How to Use These Templates

1. Browse the category that matches what you need to build.
2. Copy the template folder (or specific files) into your project.
3. Follow the template's own README for integration with the Design System + Px principles.
4. Customize via config or extension points — never break the core Px alignment.
5. Contribute improvements back: generalize patterns, improve educational content, or add new high-value templates.

**New templates must include**:
- Deep, scannable README with usage, architecture decisions, and explicit Px alignment
- runnable examples or clear setup instructions
- References to `pixel-journey-design-system` and relevant standards
- Educational notes explaining the "why"

See root `CONTRIBUTING.md` and `STANDARDS.md` for the full quality checklist.

---

## Relationship to the Broader Ecosystem

These templates are the practical implementation layer of the `pixel-journey-templates` handbook. They are tightly integrated with:
- `pixel-journey-design-system` (visual language & components)
- `pixel-journey-standards` (foundational rules)
- `gitbook-docs` (deeper educational guides)
- `wax-ecosystem-blueprint-catalog` (WAX infrastructure patterns)
- Real Px projects (patterns are extracted from and fed back into PxWallet, Hot or Not, PxPackages, etc.)

---

## Living & Evolving

This `templates/` directory evolves as we discover new high-value patterns through real work. We add new templates only when they solve a recurring need with excellent educational and production quality.

**This section exemplifies the PX Perfection Standard** — comprehensive, educational, well-structured, and designed to accelerate consistent, high-quality Px development on WAX.

---

**Pixel Journey — Perfecting the foundation for an extraordinary Web3 adventure.**