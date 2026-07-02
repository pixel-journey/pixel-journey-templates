# Design System Knowledge Bank

**Pre-filled Knowledge Bank for Design System Integration & Pixel UI Work**

Use this alongside `design-system-integrator.md` (and `educational-documenter.md` when creating UI documentation).

## Core Principles
- All UI work should start from `pixel-journey-design-system` tokens and components
- Default to glassmorphic dark theme with neon accents
- Offer optional retro-pixel / CRT scanline skin toggle
- Use Framer Motion for motion (target fluid 120Hz feel)
- Maintain excellent accessibility (contrast, keyboard navigation, reduced motion)

## Key Tokens & Patterns
- Use design system spacing, typography, colors, and elevation consistently
- Glassmorphic cards and surfaces with subtle borders
- Clear hover/active/focus states on all interactive elements
- Modal and drilldown patterns follow design system guidelines
- Theme switching is instant and persisted

## Common Decisions
- Start with design system primitives before creating custom styles
- Extend the system cleanly when truly needed, and document the extension
- Keep retro-pixel skin as an optional, non-breaking enhancement
- Prioritize mobile experience (bottom sheet patterns on small screens)

## Accessibility Priorities
- Strong contrast ratios
- Full keyboard navigation support
- Proper focus management in modals and overlays
- Reduced motion support

## References
- `PATTERNS.md` → Glassmorphic + Retro-Pixel UI Shell, Modal/Drilldown patterns
- `ai-prompts/design-system-integrator.md`
- `pixel-journey-design-system` repository (tokens and component specs)

## Benefits
- More consistent UI implementation across Px surfaces
- Better adherence to the official design language
- Faster iteration on frontend work

Create similar focused knowledge banks for other high-priority areas as needed.