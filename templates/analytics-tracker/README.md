# analytics-tracker/

**Generalized WAX AtomicAssets Collection Tracker + Weighted Rarity + Surviving Mint Rank Engine (GitOps Serverless)**

> **This is the GOLD STANDARD reference template.** Ported and generalized from the complete, excellent gkniftyheads-tracker implementation (full source provided by Pixel Journey team). It will become the canonical pattern for any Px analytics, leaderboards, trait exposure, or on-chain data visualization tool.

## Why This Template Exists

Public dashboards for Pixal PFPs, YEET holders, Hot or Not XP, PxTicker grids, or any future collection need:
- Live surviving supply & burn rates
- Surviving mint ranks (re-ranked after burns using original `template_mint`)
- Weighted rarity scoring (template supply + mint bonuses + rarity name + variation multipliers)
- Live trait exposure % (rarity traits vs variation traits)
- Holder & rarity leaderboards
- **Zero ongoing server cost** via GitHub Actions + static JSON + CDN
- Full Git history of every supply/rarity change (transparent & auditable)

All of this is achieved with **pure client-side + public WAX infra** (AtomicAssets API + Hyperion where needed).

## Quick Start (Demo Mode)

```bash
cd templates/analytics-tracker
# Use provided sample data first
npm run demo          # opens beautiful dashboard with mock survivors

# For real collection (after removing demoLimit in config)
npm run hydrate       # one-time full download (cursor pagination)
npm run calculate     # weighted rarity + ranks + exposure
# Then open demo/index.html or deploy demo/
```

## Core Features (All Educational)

- **Config-driven everything** (`config.json`): collection name, batch sizes, rarity weights, API nodes, demo limit, gzip
- **Cursor pagination hydrate** (best practice for 100k–500k assets)
- **Daily delta sync** (new mints + burns only — cheap & fast)
- **Rarity Calculation Engine**:
  - Only processes surviving (non-burned + has owner) assets
  - Surviving Mint Rank within template (sorted by original `template_mint`)
  - Weighted score = statistical base + template supply weight + mint number bonuses + legendary/1/1 multipliers + variation multiplier
- **Split Trait Exposure** (rarity_traits vs variation_traits with live % of current survivors)
- **Two Leaderboards**: Holder (top by weighted rarity sum) + Rarity (top N with original mint #, surviving rank, scores)
- **Self-updating GitHub Action** (`.github/workflows/daily-sync.yml`)
- **Stunning single-file demo** (Tailwind + modals + search + keyboard shortcuts + tabs)

## File-by-File Architecture (Educational Heart)

See the original gkniftyheads-tracker `README.md` (included in full context) for the complete handbook. This template will maintain that level of clarity:

- `config.json` — Single control panel
- `scripts/hydrate.js` — Cursor-based bulk ingest (educational comments on pagination, rate limits, template extraction)
- `scripts/delta-sync.js` — Incremental mint/burn logic (placeholder → full impl in port)
- `scripts/calculate-rarity.js` — The brain (trait frequency, grouping by template, rank assignment, full weighted formula — all tunable)
- `data/` — All generated JSONs (manifest, templates, schemas/<collection>.json, template_stats, trait_exposure, leaderboard)
- `demo/index.html` — Self-contained interactive dashboard (dynamic JSON loader, asset modal with original mint + surviving rank + weighted score)
- `.github/workflows/daily-sync.yml` — Zero-cost nightly automation

## Px-Specific Customization (Planned in Port)

- Default to a Pixal PFP collection example (or mock data styled as Pixal tiers: Holder/Stacker/Whale/Kraken)
- Easy toggle between "demo mode" (instant) and "live WAX mode"
- Integration hooks for Px design tokens (glassmorphic + neon + CRT optional)
- Exportable components for embedding leaderboards into Px Hot or Not or PxWallet "Community" tab

## WAX Best Practices Embedded

- Cursor pagination with `lower_bound`
- Multiple public Atomic API nodes with fallback
- `template_mint` preservation for surviving rank feature
- Only survivors counted in all rankings/exposure (burned assets filtered)
- Full reference to https://onblock.dev/working-with-the-atomic-api

## Status in Master Plan

**Phase 2 Priority**. Full port of the provided gkniftyheads-tracker source will happen in the next slice of this conversation. It will be generalized, Px-branded, and kept at the same (or higher) educational standard.

Once complete, this single template will accelerate *every* future Px data-heavy feature.