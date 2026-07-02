## Description
Please include a summary of the changes and which issue is fixed. Please also include relevant motivation and context.

Fixes # (issue)

## Type of change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature or pattern (non-breaking)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation / Handbook improvement
- [ ] Refactor / code quality

## Alignment with Px Handbook (required)
Before submitting, confirm you have reviewed the relevant sections:
- [ ] I have read `STANDARDS.md` and this change follows the expected shape and principles
- [ ] I have checked `PATTERNS.md` — this work either follows an existing pattern or introduces a new reusable one documented here
- [ ] Educational value and documentation have been considered

## Px Quality Checklist (required)
- [ ] All new code is strictly TypeScript with full interfaces
- [ ] Follows ZERO CUSTOM CONTRACT OVERHEAD principle
- [ ] Client-side state & public infra only (Hyperion/AtomicAssets/Alcor)
- [ ] On-chain entropy used for any randomness (if applicable)
- [ ] Educational READMEs / inline comments updated or added
- [ ] Demo / example mode works (mock or live data)
- [ ] Config-driven where possible
- [ ] Pixel / glassmorphic theme hooks present (or documented why not)
- [ ] No legacy libs (no UAL, no eosjs, no AnchorLink)
- [ ] Aligns with `pixel-journey-design-system` for all UI work

## How Has This Been Tested?
Please describe the tests that you ran.

## Screenshots (if UI change)

## Checklist
- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works