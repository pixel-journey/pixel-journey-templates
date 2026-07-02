# templates/

**The living library of Pixel Journey reference implementations and starters.**

Each sub-directory is a complete, educational, runnable template that can be used directly as a GitHub repository template or copied into new projects.

## How to Use

1. **GitHub Template Button** (best for new repos): When creating a new repo, choose "pixel-journey/pixel-journey-templates" then select the sub-folder you want (GitHub supports template repos with sub-paths in some flows, or simply copy the folder).
2. **Local Development**: `cd templates/<category>` then follow its README.
3. **AI-Assisted**: These are designed to be dropped into Claude / Grok / Cursor with full context — the layered docs make it trivial for agents to extend correctly.

## Categories (Status)

| Folder                    | Purpose                                      | Status          | Key Educational Content                     |
|---------------------------|----------------------------------------------|-----------------|---------------------------------------------|
| `github-org/`             | Org-wide GitHub configs & new repo bootstrap | Phase 1         | Semantic PRs, issue templates, CI patterns  |
| `nextjs-dapp/`            | Production Next.js 15 + WharfKit dApp shell  | Phase 2 start   | Session management, asset queries, Px UI    |
| `analytics-tracker/`      | GitOps rarity/leaderboard/data pipeline      | **Priority Port** | Full gkniftyheads generalization + formulas |
| `game-verifiable/`        | On-chain entropy + voting/hot-or-not arena   | Phase 3         | TX hash seed parsing, verifiable pairing    |
| `wallet-primitives/`      | Encrypted vaults, cross-chain derivation, MV3 ext | Phase 4     | Key mgmt security patterns, no privkey leak |

## Contribution Rule
Any new template **must** include:
- Its own exhaustive `README.md` (big picture + file inventory + formulas + WAX best practices)
- Working demo (even with mock data)
- `config.json` or clear env controls
- Strict TypeScript
- Clear "Px Principles" section

See root `CONTRIBUTING.md` for the full quality bar.