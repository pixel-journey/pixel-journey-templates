# GLOSSARY.md

**Key Terms in the Pixel Journey Ecosystem**

This glossary helps new contributors and developers quickly understand the language we use across Px projects.

## Core Concepts

**Pixal** — The flagship NFT collection / PFP series in the Pixel Journey ecosystem. Supports tiered ownership (Holder, Stacker, Whale, Kraken) with burns, airdrops, and progression mechanics.

**PxWallet** — The god-mode self-custody wallet being built for Pixel Journey. Features encrypted local vault, cross-chain key derivation (WAX → EVM / Solana), Chrome MV3 extension + PWA support, auto-sign (opt-in), and deep DeFi integration.

**Px Hot or Not** — The verifiable voting / matchmaking arena. Uses on-chain entropy for fair pairing, PXJ transfers for votes, and 50% reward splits. Leaderboards combine surviving mint rank, weighted scores, XP, and streaks.

**YEET** — The community meme coin of Pixel Journey. Fair launch with airdrops, PURR rewards, staking, and integration with Pixal PFPs and burns. No team allocation or taxes.

**PxPackages** — The upcoming monorepo and published package scope (`@pxjourney/*`). Will contain shared utilities, UI primitives, game SDK hooks, and WAX client helpers extracted from real Px development.

**Surviving Mint Rank** — When assets are burned, the remaining assets in a template are re-ranked by their original `template_mint` number. Rank 1 = the lowest original mint still alive.

**On-Chain Entropy** — The deterministic, client-side randomness technique used for fair game mechanics. Derived from transaction hash + recent block header data. Provably fair, zero cost, fully verifiable.

**Glassmorphic + Pixel Aesthetic** — The signature Px visual language: modern glassmorphism with optional retro-pixel / CRT scanline skin. Built on top of the `pixel-journey-design-system`.

## Technical Terms

**WharfKit** — The modern WAX authentication and contract interaction library (Session Kit, Contract Kit, Account Kit). The only supported auth solution in Px projects.

**AtomicAssets** — The public NFT standard and API on WAX. All Pixal and collection data comes from here.

**template_mint** — The original sequential mint number assigned to an asset at creation time. Critical for surviving mint rank and early supporter recognition.

**Cursor Pagination** — The recommended way to fetch large collections on AtomicAssets using `lower_bound` + `sort=asset_id`. Avoids deep page performance problems.

**GitOps Data Pipeline** — The zero-server-cost pattern of using GitHub Actions to periodically fetch on-chain data, calculate derived values (rarity, exposure, leaderboards), and commit static JSON files that are served via CDN.

## Related Repos

See `ECOSYSTEM.md` for the current mapping of repositories in the Pixel Journey GitHub Organization.