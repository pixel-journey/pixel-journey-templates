# On-Chain Entropy Guide

**How Pixel Journey Implements Provably Fair Randomness Without Oracles or RAM Cost**

This guide explains the pattern we use for all randomness-dependent features (Hot or Not pairings, future mini-games, procedural elements, etc.). It is one of the most important technical differentiators of the Px approach.

## The Problem

Traditional on-chain games either:
- Use centralized oracles (cost + trust issues)
- Store randomness on-chain (RAM bloat + fees)
- Use weak client-side `Math.random()` (not verifiable or fair)

Px rejects all three.

## The Solution: Deterministic Client-Side Derivation

We derive entropy **after** a user action is broadcast, using only public on-chain data:

1. The transaction hash of the action that triggered the random event
2. Recent block header data (available via public RPC or History API)

Because the TX hash is only known *after* the transaction is included in a block, and block headers are deterministic, the resulting seed is:
- Provably fair (anyone can recompute it)
- Impossible to predict or manipulate in advance
- Completely free (no oracle calls, no RAM allocation)

## Implementation Requirements

Every Px feature using randomness **must**:

- Use a pure, deterministic function: `deriveEntropy(txId: string, blockHeader: any) => Uint8Array | string`
- Document the exact derivation steps in the code and UI
- Surface the source TX and seed in the interface so users can verify independently
- Never fall back to insecure randomness for anything that affects outcomes or rewards

## Example High-Level Flow (Hot or Not Style)

1. User initiates a vote / match request → signs and broadcasts TX
2. Client waits for TX confirmation
3. Client fetches recent block header(s)
4. Client computes entropy from `txId + block data`
5. Client uses entropy to determine pairing, outcome, or reward tier
6. UI shows: "Pairing derived from TX abc123... + Block 12345678 — verifiable by anyone"

## Why This Matters for Px

- Aligns with our "trustless verifiable mechanics" ethos
- Enables fun, meme-worthy features (Hot or Not, future games) without compromising on decentralization
- Creates strong educational moments — users literally see how fairness is enforced
- Scales infinitely at zero marginal cost

## Related Patterns

See `PATTERNS.md` → "Verifiable On-Chain Entropy" for the concise version of this pattern.

This approach will be reused across Px Hot or Not alpha, future mini-games, and any procedural content in the ecosystem.