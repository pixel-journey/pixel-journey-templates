# nextjs-dapp/

**Production-Grade Next.js 15 + WharfKit dApp Shell for Pixel Journey Features**

> The default starting point for any new Px frontend: PxWallet, Px Hot or Not, PxTicker, community portals, etc.

## Stack (Locked & Aligned with Px Standards)

- **Framework**: Next.js 15 (App Router, React Server Components where beneficial, Turbopack)
- **Auth/Session**: WharfKit Session Kit + Account Kit + Contract Kit (strictly no legacy UAL/eosjs/Anchor)
- **State**: Zustand (sessions, assets, UI) + TanStack Query (server state, caching)
- **Styling**: Tailwind CSS + Shadcn UI primitives + Radix + Framer Motion (animations, modals, haptics-ready)
- **i18n**: next-intl or i18next with 8+ Px locales pre-configured
- **Theme**: Deep hooks for pixel-journey-design-system (glassmorphic dark + optional retro CRT/Pixel skin toggle)
- **TypeScript**: Strict, comprehensive interfaces for all WAX responses and Px domain types

## Quick Start

```bash
cd templates/nextjs-dapp
npm install
npm run dev
# Connect WharfKit session (Testnet by default)
# See live sample AtomicAssets query for demo Pixal-style assets
```

## What You Get Out of the Box (Educational + Production)

- Full WharfKit session management (login/logout, active account, sign arbitrary actions)
- Example AtomicAssets query (fetch assets by owner or collection) with proper cursor handling pattern
- Px-branded UI shell (header with wallet status, tab navigation, glassmorphic cards)
- Zustand stores for `useSession`, `useAssets`, `useUI`
- Demo mode toggle (mock data when no wallet connected — perfect for screenshots/docs)
- Responsive + keyboard accessible
- Ready for i18n, error boundaries, loading skeletons
- `.env.example` + config for collection names, RPC endpoints

## Architectural Decisions Documented

(See inline comments and future deep README sections)
- Why WharfKit over legacy libs
- Client-side caching strategy (TanStack + localStorage)
- How to add new Px features without breaking session
- On-chain entropy hook location (for future game features)

## Integration Points

- Consumes tokens/components from `pixel-journey-design-system` (when mature)
- Follows patterns from `pixel-journey-standards`
- Will be the base for real PxWallet and Px Hot or Not frontends (bidirectional improvement flow)

## Status

Phase 2 scaffolding. Full implementation with working WharfKit + sample Px data in next iteration.