# analytics-tracker/

**Advanced Reference: Generalized WAX Collection Tracker + Rarity Engine Patterns (GitOps)**

> **Future / Advanced Reference Only** — This folder exists as a high-quality documentation and pattern showcase. We are **not** prioritizing a full port of the gkniftyheads-tracker right now. Instead, we extract reusable patterns (cursor pagination, delta sync logic, client-side rarity/leaderboard calculation, surviving mint rank, trait exposure) into the more fundamental **Feature Pattern Templates** and **Design & UI Templates** categories.

The excellent educational style and file-by-file architecture handbook from the gkniftyheads-tracker source you shared remains our **documentation quality benchmark** for everything we build in this repo.

## When This Might Become Active

Only if/when a specific Px feature (e.g. advanced Pixal PFP trait explorer, Hot or Not historical leaderboards, or holder analytics dashboard) would be dramatically accelerated by having a ready-to-fork GitOps rarity + leaderboard engine. At that point we can revive and generalize it under the Feature Patterns or a dedicated advanced example.

For now, the focus is on **design templates** and **core feature patterns** that give the fastest consistency wins across PxWallet, Hot or Not, PxTicker, and new community contributions.

## Key Patterns We May Extract Later (Educational Value)

- Cursor-based hydration with `lower_bound`
- Delta sync for mints + burns
- Client-side only weighted rarity + surviving_mint_rank calculation
- Split trait exposure (rarity vs variation)
- Beautiful, self-contained demo dashboard pattern
- Zero-cost GitHub Actions + static JSON + CDN delivery

These patterns can inform smaller, more focused templates in `feature-patterns/` (e.g. a "Leaderboard with surviving ranks UI + logic shell" or "Trait exposure visualization component").

## Current Status

**On hold / Reference only**. The folder and this README are kept for context and future use. The real work is happening in `design-ui/` and `feature-patterns/` to deliver immediate value for consistent Px development speed.