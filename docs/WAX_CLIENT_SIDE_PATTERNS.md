# WAX Client-Side Patterns

**Educational Guide to Building Production-Grade Experiences on Public WAX Infrastructure**

This guide captures the architectural patterns that power reliable, educational, and performant Px applications without custom backends.

## Core Philosophy

We treat the WAX blockchain (via AtomicAssets, Alcor AMM, Hyperion History, and native RPC) as the source of truth. All public data is fetched and processed client-side. This gives us:

- Zero ongoing server costs for public dashboards and tools
- Full transparency and auditability (every data point traces back to on-chain state)
- Excellent educational value — new developers can follow the exact same queries and logic

## Key Patterns

### 1. Cursor-Based Pagination (The Only Scalable Way)

For any collection with thousands of assets, never use `page=` pagination.

**Correct approach**:
```ts
// lower_bound on asset_id + sort + order
/assets?collection_name=...&limit=500&sort=asset_id&order=asc&lower_bound=${lastAssetId}
```

**Why it wins**:
- Avoids the deep-page performance cliff
- Predictable, linear cost
- Easy to resume after interruption

All Px data-heavy features (asset galleries, trait exposure, leaderboards) use this pattern.

### 2. Delta Sync for Daily / Incremental Updates

Instead of re-hydrating entire collections every time:

- Track `last_sync_timestamp` in manifest or local state
- Fetch new mints: `?after=TIMESTAMP&sort=created&order=asc`
- Fetch recent burns: `?burned=true&after=TIMESTAMP&sort=updated&order=asc`
- Merge into existing local dataset

This is the foundation of zero-cost GitOps data pipelines.

### 3. Client-Side Filtering & Calculation

Never trust server-side aggregates for public rankings when the source data is public.

**Examples**:
- Surviving supply = count of `!burned && owner`
- Surviving mint rank = sort survivors by original `template_mint` within each template
- Weighted rarity / trait exposure = calculated live from current survivors only
- XP, streaks, and badge progress = derived from on-chain action history

All of this runs in the browser (or in GitHub Actions for static JSON generation).

### 4. Multiple Public Endpoints + Fallbacks

Never rely on a single API node.

Maintain a list of healthy public endpoints (Alcor, EOSphere, etc.) and rotate or fallback on failure. This is table stakes for production reliability.

### 5. On-Chain Entropy for Verifiable Randomness

See the dedicated pattern in `PATTERNS.md`. The key is deterministic derivation from TX hash + block header — this is what makes Hot or Not and future mini-games trustless and educational.

## Recommended Reading

- [Working with the Atomic API](https://onblock.dev/working-with-the-atomic-api) — excellent practical guide
- Official AtomicAssets Swagger docs
- Hyperion History API documentation

## How This Fits Px

Every major Px surface (PxWallet asset views, Hot or Not leaderboards, Pixal trait explorers, PxTicker grids) follows these patterns. When you see a new feature request, first ask: "Can this be done with public data + client-side logic + the patterns above?"

If the answer is yes, we stay aligned with our principles and keep the ecosystem coherent.