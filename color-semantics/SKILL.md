---
name: color-semantics
description: Design intentional, purposeful color systems for information design — categorical palettes, sequential schemes, diverging scales, and semantic color roles. Use when choosing or auditing color in a data visualization, infographic, or editorial design piece. Triggers on "color palette", "color scheme", "accessible colors", "color for data", or any request for color guidance in information design contexts.
license: MIT
metadata:
  author: information-designer
  version: "1.0.0"
---

Color in information design is not decoration — it is a data channel. Every color decision encodes meaning and must be intentional, consistent, and interpretable without prior explanation.

## Color Roles

Assign each color in a palette a role before use:

| Role | Purpose | Typical count |
|------|---------|---------------|
| **Primary** | The main categorical distinction or key metric | 1–2 |
| **Secondary** | Supporting categories or comparison baseline | 2–4 |
| **Accent** | Highlight, anomaly, or call-to-action | 1 |
| **Neutral** | Background, grid lines, annotations | 2–3 |
| **Absence** | Explicitly encodes "no data" or zero | 1 |

Never use a color without a role. If you cannot name what the color encodes, remove it.

## Palette Archetypes

### Categorical (qualitative)
For unordered groups. Requirements:
- Each hue must be perceptually equidistant
- Works in grayscale (lightness varies)
- Distinguishable for common color vision deficiencies (deuteranopia, protanopia)

Starting palette inspired by editorial restraint:
```
#1a1a2e  (deep navy)      — primary text, dominant category
#e63946  (signal red)     — accent, critical value
#457b9d  (slate blue)     — secondary category A
#a8dadc  (pale teal)      — secondary category B
#f1faee  (off-white)      — background, neutral space
```

### Sequential (quantitative, one direction)
For data that goes from low to high. Build as a 5–7 step ramp:
- Fix hue, vary lightness from ~90% (low) to ~20% (high)
- Or shift hue slightly (yellow → orange → red for "heat")

### Diverging (quantitative, two directions from a center)
For data with a meaningful midpoint (zero, average, target):
- Two hues diverge from a neutral center
- Keep saturation equal on both sides
- Common: blue ←→ red with light gray center

## Accessibility Baseline

Every palette must pass:
- **WCAG AA contrast** (4.5:1) for text on background, (3:1) for large text and UI elements
- **Deuteranopia simulation** — check with a color-blindness simulator; avoid red/green as the *only* distinction
- **Print/grayscale** — if the design might be printed, encodings must survive desaturation

Test tools: Colour Contrast Analyser, Viz Palette, Chroma.js `chroma.deltaE()`.

## Color and Emotion in Editorial Design

For editorial and publication work, color carries cultural and emotional weight beyond encoding:

- **Muted, desaturated palettes** → contemplative, serious, rigorous
- **Warm accent on cool ground** → tension, urgency, attention
- **Monochromatic with one saturated accent** → clarity, sophistication
- **High-contrast black and color** → editorial authority (newspaper aesthetic)

Fragapane's signature approach: a dark or neutral ground, with carefully chosen mid-saturation hues that feel archival and considered — never decorative.

## Applying Color in Practice

1. Start in grayscale — if the layout doesn't work without color, fix the layout
2. Introduce one hue at a time; stop when the piece reads clearly
3. Use color to confirm what shape and position already communicate
4. Reserve high saturation and high contrast for the single most important element
5. When in doubt, less color is always more precise
