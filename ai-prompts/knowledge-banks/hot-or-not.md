# Hot or Not / Verifiable Mechanics Knowledge Bank

**Pre-filled Knowledge Bank for Hot or Not and Verifiable Game Mechanics Work**

Use this alongside `game-systems-designer.md` (and `px-core-architect.md` when planning new game features).

## Core Principles
- All randomness uses on-chain entropy (TX hash + block header derivation)
- Every mechanic must be verifiable by users
- Prefer client-side state and public data
- Educational output quality is non-negotiable
- Transparency in UI (show source TX and derivation method)

## Key Hot or Not Mechanics
- Verifiable pairing via memos + entropy
- PXJ voting with reward splits (commonly 50/50)
- Leaderboards combining surviving mint rank + weighted score
- XP, streaks, and badge progression tied to on-chain actions
- Tiered ownership (Holder → Stacker → Whale → Kraken) with surviving mint rank importance

## Common Patterns
- Use entropy + verifiable pairing pattern for match generation
- Clear "Vote with PXJ" flow with confirmation and result display
- Leaderboards combine surviving rank + weighted score concepts
- All mechanics remain auditable via transaction history

## References
- `PATTERNS.md` → Verifiable On-Chain Entropy, Leaderboards, Verifiable Voting
- `docs/ONCHAIN_ENTROPY_GUIDE.md`
- `ai-prompts/game-systems-designer.md`

## Benefits
- More consistent and accurate game mechanics design
- Better verifiable and transparent implementations
- Faster iteration on Hot or Not style features

Create similar focused knowledge banks for other high-priority areas as needed.