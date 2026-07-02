# PxWallet Architecture Overview

**High-Level Guide to the God-Mode Self-Custody Wallet**

This document provides a high-level architectural overview of PxWallet — one of the flagship projects in the Pixel Journey ecosystem. It is intended to help developers and AI agents understand the major components and design decisions.

## Core Goals

- Maximum self-custody and security
- Excellent user experience (especially for non-technical users)
- Cross-chain support (WAX → EVM / Solana key derivation)
- Deep integration with the rest of the Px ecosystem (Pixal PFPs, Hot or Not, YEET, etc.)
- Support for both browser extension (Chrome MV3) and Progressive Web App (PWA)

## High-Level Architecture

### 1. Encrypted Local Vault

- Master password / biometric protected seed storage
- Strong encryption at rest (Web Crypto API or equivalent)
- Never exposes raw private keys to the UI layer
- Supports account derivation and multiple accounts

### 2. Key Derivation Layer

- Deterministic hierarchical derivation from master seed
- Support for WAX, EVM-compatible chains, and Solana
- Clean separation between derivation logic and signing
- Future-proof for additional chains

### 3. Signing & Transaction Layer

- WharfKit integration for WAX
- Support for multiple signing methods (software vault + hardware wallets)
- Clear UX for transaction review and confirmation
- Auto-sign with explicit, limited scope (user opt-in)

### 4. Frontend Layers

- **Chrome Extension (MV3)**: Background script, popup, and content scripts
- **PWA**: Full-featured web version with offline capabilities
- Shared state management (Zustand) and UI components (Design System)

### 5. Integration Points

- Deep integration with AtomicAssets (Pixal viewing, management)
- Connection points for Hot or Not and other Px dApps
- Future DeFi features (swaps, limit orders via Alcor)
- Analytics and portfolio tracking

## Key Patterns Used

- Cross-Chain Key Derivation & Vault Patterns (see `PATTERNS.md`)
- WharfKit Session & Authentication pattern
- Glassmorphic + Pixel UI Shell
- Modal / Drilldown patterns for transaction review and asset details

## Security Philosophy

- User is always in control
- Transparency around what is being signed
- Defense in depth (encryption + derivation + UX safeguards)
- Clear recovery and backup flows

## Current Status

PxWallet is under active development following the master 150+ item / 26-phase roadmap. Many core vault and derivation features are prioritized early.

## Related Resources

- `PATTERNS.md` → Cross-Chain Key Derivation & Vault Patterns
- `ai-prompts/wallet-security-engineer.md` (specialized AI prompt)
- Future detailed implementation guides will be linked here as they are created

This overview will be expanded as the wallet architecture matures.