# knowledge-bank-example.md

**Example: Pre-filled Knowledge Bank Template**

This is an example of how a specialized AI persona can be paired with a pre-filled knowledge bank. The idea is to give the agent rich, structured context about a specific domain so it can provide more accurate and helpful responses without needing to re-explain fundamentals every time.

## How to Use

1. Create a knowledge bank file (Markdown or structured text) with key concepts, patterns, decisions, and references.
2. Include it in the system prompt or as additional context when starting a conversation with a specialized persona.
3. The agent can then reference this knowledge directly, leading to higher-quality, more consistent outputs.

## Example Structure (for a Game Systems persona)

```markdown
# Pixel Journey Game Systems Knowledge Bank

## Core Principles
- All randomness uses on-chain entropy (TX hash + block header)
- Prefer client-side state and public data
- Every mechanic must be verifiable by users

## Key Patterns
- Verifiable pairing via memos + entropy
- Surviving mint rank + weighted rarity for leaderboards
- XP, streaks, and badge progression tied to on-chain actions

## Common Decisions
- Reward splits: Usually 50/50 for Hot or Not style mechanics
- Transparency: Always show source TX and derivation method in UI

## References
- `PATTERNS.md` → Verifiable On-Chain Entropy
- `docs/ONCHAIN_ENTROPY_GUIDE.md`
- `ai-prompts/game-systems-designer.md`
```

## Benefits
- Faster, higher-quality responses
- Better consistency across conversations
- Easier onboarding for new AI collaborators
- Reduces hallucination on Px-specific concepts

You can create similar knowledge banks for any persona (Wallet Security, Design System, Educational Support, etc.). This approach scales well as the ecosystem grows.