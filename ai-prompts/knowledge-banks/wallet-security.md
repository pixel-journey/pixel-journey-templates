# Wallet Security Knowledge Bank

**Pre-filled Knowledge Bank for Wallet Security & Self-Custody Work**

Use this alongside `wallet-security-engineer.md` (or `px-core-architect.md` when working on PxWallet features).

See `PATTERNS.md` → Cross-Chain Key Derivation & Vault Patterns, and `EDUCATIONAL-QUALITY-STANDARD.md` for quality expectations.

## Core Principles
- Never expose or transmit raw private keys
- Use deterministic, hierarchical derivation from a user-protected master seed
- Strong encryption at rest for sensitive material
- Clear separation between key management, signing, and UI layers
- All sensitive operations require explicit user consent and clear feedback
- Auto-sign is always opt-in with explicit, limited scope

## Key Architecture Decisions
- Master password / biometric protected seed storage
- Deterministic derivation for WAX, EVM-compatible chains, and Solana
- Encrypted local vault (Web Crypto API or equivalent)
- Support for both software vault and hardware wallet paths
- Chrome MV3 extension (background + popup + content scripts) + PWA

## Common Patterns
- Vault logic is isolated and auditable
- Derivation happens client-side with strong encryption at rest
- Users see derived addresses without ever seeing seed material
- Transaction review modals with clear signing intent
- Recovery and backup flows must be first-class

## Security Priorities
- Defense in depth (encryption + derivation + UX safeguards)
- Transparency around what is being signed
- User is always in control
- Clear error states and recovery paths

## References
- `PATTERNS.md` → Cross-Chain Key Derivation & Vault Patterns
- `ai-prompts/wallet-security-engineer.md`
- `docs/PXWALLET_ARCHITECTURE_OVERVIEW.md`
- `knowledge-banks/cross-chain.md`

## Benefits
- More accurate and consistent advice on wallet features
- Better security reasoning in generated code and designs
- Faster iteration on PxWallet work

Create similar focused knowledge banks for other high-priority areas as needed.