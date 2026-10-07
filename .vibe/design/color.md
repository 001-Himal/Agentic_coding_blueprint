# color.md

Use existing tokens. Do not invent new colors unless added to the design system.

## Contrast (non-negotiable)
- Text on background must meet WCAG AA: ≥ 4.5:1 for normal text, ≥ 3:1 for large text and UI components.
- Check EVERY text/background pairing: headings, body, captions, buttons, links, badges, placeholders, disabled states, toasts, badges on images.
- Verify both states of component that flip bg/text (hover, active, selected, focus) — a good default state can hide a broken hover state.
- Check dark mode AND light mode separately; a token pair that passes in one can fail in the other.
- Do not rely on color alone to convey meaning — pair it with text/icon (red text on red-tinted bg still counts as "low contrast + color-only").

## AI-slop-proof color rules
- Never hardcode raw hex in components; always reference design tokens.
- Never put light text on light bg or dark text on dark bg — AI "aesthetic" output loves washed-out pastels; reject them.
- Backgrounds and text must come from the SAME token family (e.g., `bg-surface` + `text-on-surface`), never mixed from unrelated palettes.
- No low-contrast "ghost" text, no white text on saturated brand colors without measuring, no gray-on-gray stacks.
- Accent/brand colors must pass contrast on BOTH primary and secondary surfaces; if a brand color fails, use a dedicated darker/lighter token for text usage.
- Placeholder text, captions, and disabled text still need readable contrast (≥ 3:1 minimum); "it's intentionally faded" is not an excuse.
- Overlays, modals, and images behind text need a scrim/backdrop that guarantees contrast — never text directly over a busy screenshot/photo.
- One accent color per surface; multiple clashing accent hues on one screen = slop.
- Shadows, borders, and dividers must be visible enough to separate layers but never compete with text.

## Verification
- Run a contrast checker on the final values, not on "what the CSS looks like".
- Any color change re-runs: visual check at all breakpoints + both themes + hover/focus states.
