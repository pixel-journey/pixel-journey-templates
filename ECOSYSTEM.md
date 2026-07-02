# ECOSYSTEM.md

**Pixel Journey Organization Ecosystem Overview**

This document maps the major repositories and projects in the Pixel Journey GitHub Organization and how they relate to each other.

## Core Repositories

| Repo                              | Purpose                                                                 | Maturity | Key Patterns / Focus Areas                     |
|-----------------------------------|-------------------------------------------------------------------------|----------|------------------------------------------------|
| `pixel-journey` (org)             | Organization root & high-level coordination                             | Active   | Governance, visibility                         |
| `pixel-journey-templates` (this)  | Standards, patterns, and ecosystem handbook                             | Active   | This repo — instructions & target state        |
| `pixel-journey-design-system`     | Visual language, tokens, components, theming                            | Active   | Glassmorphic + pixel aesthetic, Figma sync     |
| `pixel-journey-standards`         | Foundational engineering rules and Web3 best practices                  | Active   | Coding standards, security, contribution rules |
| `PxWallet`                        | God-mode self-custody wallet (vault, cross-chain, Chrome ext, PWA)      | In Progress | Encrypted vault, key derivation, auto-sign, DeFi |
| `PxHotOrNot` / Hot or Not         | Verifiable voting arena with PXJ mechanics, leaderboards, XP            | Alpha    | On-chain entropy, verifiable pairing, rewards  |
| `PxPackages`                      | Monorepo for published `@pxjourney/*` packages                          | Planned  | Unified wiring, shared utils, SDK hooks        |
| `docs.pixeljourney.xyz` / GitBook | Knowledge bank, WAX/EVM guides, ecosystem documentation                 | Active   | Educational content, navigation, onboarding    |

## Supporting & Community Repos

- Collection-specific tools and trackers (e.g. Pixal PFP analytics, trait exposure)
- Meme coin tooling around YEET (airdrops, staking, PFPs, burns)
- Mini-game experiments and visualizers
- Community contribution repos

All of these are expected to align with the standards and patterns documented in this handbook.

## How the Pieces Fit Together

- **Design System** provides the visual foundation.
- **Standards + this Templates/Handbook repo** provide the architectural and documentation rules.
- **PxWallet** and **Hot or Not** are flagship consumer experiences that stress-test the patterns.
- **PxPackages** will extract the best reusable pieces into published, versioned packages.
- **Docs** captures the educational output and makes the ecosystem approachable.

## Contribution Flow

1. New idea or feature → Check this handbook (Patterns + Standards)
2. Align with Design System
3. Implement in the appropriate repo (or propose new one)
4. Document decisions back into this handbook if the pattern is reusable
5. Improve educational clarity for future contributors

This creates a virtuous cycle of consistency and velocity.