# Cross-Chain / Multi-Chain Development Knowledge Bank

**Pre-filled Knowledge Bank for Cross-Chain Key Derivation and Multi-Chain Work**

Use this alongside `wallet-security-engineer.md` and `px-core-architect.md` when working on multi-chain features.

## Core Principles
- Never expose or transmit raw private keys
- Use deterministic, hierarchical derivation from a user-protected master seed
- Clear separation between key management, signing, and UI layers
- Support for WAX, EVM-compatible chains, and Solana (expandable to others)
- Encrypted local vault with strong security at rest

## Key Architecture Decisions
- Master password / biometric protected seed storage
- Deterministic derivation for multiple chains from a single master seed
- Users see derived addresses without ever seeing seed material
- Support for both software vault and hardware wallet paths
- Clear UX for viewing and managing derived accounts across chains

## Common Patterns
- Vault logic is isolated and auditable
- Derivation happens client-side with strong encryption
- Transaction review modals clearly show chain and intent
- Recovery and backup flows must be first-class and chain-aware

## Security Priorities
- Defense in depth (encryption + derivation + UX safeguards)
- Transparency around what is being signed and on which chain
- User is always in control
- Clear error states and recovery paths per chain

## References
- `PATTERNS.md` → Cross-Chain Key Derivation & Vault Patterns
- `ai-prompts/wallet-security-engineer.md`
- `docs/PXWALLET_ARCHITECTURE_OVERVIEW.md`

## Benefits
- More consistent and secure multi-chain implementations
- Better reasoning on cross-chain UX and security trade-offs
- Faster iteration on PxWallet multi-chain features

Create similar focused knowledge banks for other high-priority areas as needed.