# ECOSYSTEM.md

**Pixel Journey Ecosystem Overview**

This document provides a high-level map of the major repositories and how they relate to each other within the Pixel Journey organization.

## Core Repos

| Repo | Purpose | Relationship to This Handbook |
|------|---------|-------------------------------|
| `pixel-journey-templates` (this repo) | Central standards, patterns, educational guides, and AI collaboration tools | Single source of truth for how we build |
| `pixel-journey-design-system` | Visual language, design tokens, components, and style guide | Referenced heavily in UI-related patterns and the `design-system-integrator.md` prompt |
| `pixel-journey-standards` | Foundational engineering rules and Web3 best practices | Builds on top with Px-specific enforcement and patterns |
| `wax-ecosystem-blueprint-catalog` | Planning and indexing catalog for individual WAX public infrastructure blueprint repositories | Shares strong alignment on educational quality; we have cross-referenced standards |

## Major Project Repos (Examples)

- **PxWallet** — God-mode self-custody wallet with cross-chain derivation
- **Hot or Not (Px Hot or Not)** — Verifiable voting/pairing with leaderboards and progression
- **PxPackages** — Monorepo of reusable shared packages under `@pxjourney/*`
- Individual blueprint repos (under the catalog) — Focused, high-quality examples of public WAX infrastructure usage

## How This Handbook Fits In

This `pixel-journey-templates` repo acts as the **central reference layer**:
- It defines the standards and patterns that all other repos should follow
- It provides reusable AI personas and knowledge banks to accelerate development
- It maintains the educational quality bar across the ecosystem

Individual project repos and blueprint repos are expected to align with the patterns and quality standards defined here, while contributing new reusable patterns back when discovered.

## Contribution Flow

1. Work happens in project-specific or blueprint repos
2. Reusable patterns and lessons are extracted into this handbook
3. The handbook is updated and referenced by future work
4. AI personas and knowledge banks are improved based on real usage

This creates a virtuous cycle of continuous improvement across the entire Pixel Journey ecosystem.