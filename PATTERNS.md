# PATTERNS.md

**Recommended Patterns & Best Expected Usage in Pixel Journey**

This document provides overviews of the patterns we use repeatedly across Px projects. It focuses on **requirements + key decisions + best expected usage** rather than full implementations (those live in the individual repos).

## WharfKit Session & Authentication Pattern

**Purpose**: Consistent wallet connection, session management, and signing across all Px frontends.

**Key Requirements**:
- Use WharfKit Session Kit + Account Kit exclusively
- Support both Anchor and WalletConnect where possible via WharfKit
- Clear visual state for connected / disconnected / wrong network
- Expose clean hooks/stores (`useSession`, `useAccount`)
- Auto-reconnect on return visits (with user consent)

**Best Expected Usage**:
- Session provider wraps the entire app
- Components react to session changes via Zustand or context
- Signing actions are wrapped with loading/error/success UI
- Testnet/Mainnet switching is explicit and safe

## Verifiable On-Chain Entropy (for Games & Random Mechanics)

**Purpose**: Provably fair randomness without oracles or RAM cost.

**Key Requirements**:
- Derive seed deterministically from a recent transaction hash + block header data
- Never rely on client-side `Math.random()` for anything that affects on-chain outcomes or fairness
- Document the exact derivation method so others can verify

**Best Expected Usage**:
- Create a small pure utility (`deriveEntropyFromTx(txId, blockNum) => seed`)
- Use the seed for game logic (pairing in Hot or Not, loot tables, etc.)
- Expose the seed and derivation in UI for transparency ("Verifiable via TX ...")

## Asset Query + Caching Pattern

**Purpose**: Efficiently fetch and display AtomicAssets data (Pixals, other collections) with good UX.

**Key Requirements**:
- Use cursor-based pagination (`lower_bound` + `sort=asset_id`)
- Cache responses intelligently (TanStack Query + localStorage where appropriate)
- Always filter burned assets when showing "active" supply or rankings
- Preserve `template_mint` for any ranking or "early supporter" features

**Best Expected Usage**:
- Centralize query logic in a small set of hooks or query keys
- Show skeleton/loading states that match final layout
- Support search/filter client-side on already-fetched data when possible

## Glassmorphic + Pixel UI Shell Pattern

**Purpose**: Consistent visual identity across Px surfaces.

**Key Requirements**:
- Base on tokens and components from `pixel-journey-design-system`
- Support glassmorphic dark mode as default
- Offer optional retro-pixel / CRT skin toggle for signature Px flavor
- Use Framer Motion for all motion (120Hz feel where hardware allows)
- Maintain accessibility (contrast, keyboard nav, reduced motion)

**Best Expected Usage**:
- Start every new screen or major component from approved shell templates
- Theme switching should be instant and persist
- All cards, modals, and data displays follow the same spacing, border, and shadow language

## Leaderboard / Ranking UI + Logic Shell

**Purpose**: Reusable way to display ranked lists (rarity, XP, holdings, Hot or Not results, etc.).

**Key Requirements**:
- Support multiple ranking modes (global, per-template, by tier, etc.)
- Show original mint number + surviving rank where relevant
- Clear visual distinction for top tiers (Legendary, Whale, etc.)
- Loading, empty, and error states
- Optional "Your rank" highlighting when user is connected

**Best Expected Usage**:
- Separate data fetching/logic from presentation
- Use the same table/card patterns as the Design System
- Make ranking criteria transparent to the user

These patterns will be expanded over time as we extract more reusable approaches from active Px development.