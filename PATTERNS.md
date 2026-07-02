# PATTERNS.md

**Recommended Patterns & Best Expected Usage in Pixel Journey**

This document provides overviews of the patterns we use repeatedly across Px projects. Focus is on **requirements + key decisions + best expected usage** so that new work stays consistent and high-quality.

---

## 1. WharfKit Session & Authentication

**Purpose**: Consistent, secure wallet connection and signing across all Px frontends.

**Key Requirements**:
- Use WharfKit (Session Kit + Account Kit + Contract Kit) exclusively
- No legacy UAL, eosjs, or deprecated AnchorLink patterns
- Support explicit network switching (Testnet/Mainnet) with clear feedback
- Persist session with user consent; never auto-sign without explicit opt-in
- Expose clean, typed hooks/stores for session state

**Best Expected Usage**:
- Wrap the app root with a Session Provider
- UI components react to session changes via Zustand or TanStack
- Every on-chain action button shows loading / error / success states
- "Connect Wallet" and account display are standardized across Px surfaces

---

## 2. Verifiable On-Chain Entropy (Games & Random Mechanics)

**Purpose**: Provably fair randomness with zero oracle/RAM cost.

**Key Requirements**:
- Derive entropy deterministically from a recent transaction hash + block header data
- Never use `Math.random()` or client-only randomness for anything affecting outcomes or fairness
- Make the derivation transparent and verifiable in the UI
- Document the exact method so others can independently verify

**Best Expected Usage**:
- Small pure utility function: `deriveEntropy(txId, recentBlockHeader) => seed`
- Use seed for pairing, loot, matchups, or procedural generation in Hot or Not, mini-games, etc.
- Surface the seed and source TX in the interface ("Verifiable via TX 0x...")

---

## 3. Asset Query, Caching & Display

**Purpose**: Efficient, consistent handling of AtomicAssets data (Pixals, collections, trait exposure).

**Key Requirements**:
- Cursor-based pagination (`lower_bound` + `sort=asset_id&order=asc`) for large collections
- Always filter burned assets when showing active supply or rankings
- Preserve `template_mint` — it is essential for surviving mint rank and early supporter recognition
- Use TanStack Query + intelligent local caching
- Support both mock/demo mode and live chain data

**Best Expected Usage**:
- Centralize query logic in typed hooks or query factories
- Show skeleton states that match final card/table layout
- Client-side filtering and sorting on already-fetched data when possible
- Trait exposure and rarity calculations happen client-side on survivors only

---

## 4. Glassmorphic + Retro-Pixel UI Shell

**Purpose**: Cohesive visual identity that feels distinctly Pixel Journey.

**Key Requirements**:
- Base all UI work on tokens and primitives from `pixel-journey-design-system`
- Default to glassmorphic dark theme with neon accents
- Offer optional retro-pixel / CRT scanline skin toggle (signature Px flavor)
- Use Framer Motion for all motion (target 120Hz fluid feel)
- Maintain excellent accessibility (contrast, keyboard navigation, reduced motion support)

**Best Expected Usage**:
- Start new screens or major components from approved shell patterns
- Theme switching is instant and persisted
- Cards, modals, leaderboards, and data displays follow consistent spacing, borders, and elevation language
- Every UI element has clear hover/active/focus states

---

## 5. Leaderboard, Ranking & XP Systems

**Purpose**: Reusable, transparent ranking displays (rarity, XP, holdings, Hot or Not results, tier standings).

**Key Requirements**:
- Support multiple ranking dimensions (global, per-template, by tier, by streak, etc.)
- When relevant, show both original `template_mint` and current surviving rank
- Clear visual treatment for top tiers (Legendary, Whale, Kraken, etc.)
- Loading, empty, and error states
- Optional "Your position" highlighting when a wallet is connected

**Best Expected Usage**:
- Separate data/logic layer from presentation components
- Reuse the same table and card primitives from the Design System
- Make ranking criteria and weighting formulas transparent to users
- Combine with XP/streak/badge visuals where the feature supports progression

---

## 6. Verifiable Voting / Hot-or-Not Arena Mechanics

**Purpose**: Trustless, on-chain voting and pairing with clear reward flows.

**Key Requirements**:
- Pairing/seed must be derivable from on-chain data (TX memos + entropy pattern)
- All votes and transfers use WharfKit signing with proper UX states
- Reward splits (e.g. 50/50) and XP/streak updates are transparent
- Results and leaderboards update from public chain data (no hidden backend state)

**Best Expected Usage**:
- Use the entropy + verifiable pairing pattern for match generation
- Clear "Vote with PXJ" flow with confirmation and result display
- Leaderboards combine surviving rank + weighted score concepts where applicable
- All mechanics remain auditable via transaction history

---

## 7. Cross-Chain Key Derivation & Vault Patterns

**Purpose**: Secure multi-chain support (WAX → EVM / Solana) without exposing private keys.

**Key Requirements**:
- Never expose or transmit raw private keys
- Use deterministic, hierarchical derivation from a master seed protected by user password/encryption
- Clear separation between key management, signing, and UI layers
- Support for encrypted local vault + optional hardware wallet paths

**Best Expected Usage**:
- Vault logic is isolated and auditable
- Derivation happens client-side with strong encryption at rest
- Users see clear "Derived addresses" views without ever seeing seed material
- Auto-sign is always opt-in with explicit scope

These patterns will continue to evolve as we extract more reusable approaches from active development in PxWallet, Hot or Not, PxPackages, and community work.