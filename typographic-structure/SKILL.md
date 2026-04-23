---
name: typographic-structure
description: Use typography as a structural and aesthetic element in information design — hierarchy, annotations, labels, callouts, and the integration of text with visual data. Use when designing or reviewing text within data visualizations, infographics, or editorial data pieces. Triggers on "font choice", "label placement", "annotation", "text in chart", "typography for data", or any request involving text in an information design context.
license: MIT
metadata:
  author: information-designer
  version: "1.0.0"
---

Typography in information design is not a caption system — it is an equal participant in meaning-making. The type carries the argument; the visuals carry the evidence.

## Typographic Hierarchy in Information Design

Establish exactly four typographic levels and use them consistently:

| Level | Role | Typical size relationship |
|-------|------|--------------------------|
| **Display** | Headline insight — the one truth | 3–5× base |
| **Subhead** | Section labels, category names | 1.5–2× base |
| **Body** | Explanatory text, context | 1× base |
| **Caption** | Source, methodology, small labels | 0.75× base |

Never introduce a fifth level. If you need more distinction, use weight, case, or color — not size.

## Type Choices for Information Design

### Pairing logic
- One typeface for data/numbers (tabular figures, monospaced if needed), one for prose
- Or: one typeface across all levels, distinguished by weight and style alone

### Typefaces with editorial credibility
- **GT America / Aktiv Grotesk** — contemporary, neutral sans for data labels
- **Styrene A / B** — geometric with warmth for headlines
- **Freight Text / Tiempos** — humanist serifs for body context
- **Roboto Condensed / Barlow Condensed** — space-efficient for dense data labels
- **Libre Franklin / Inter** — open-source options with full weight range

### Number formatting
- Use **tabular (lining) figures** for data labels — they align vertically
- Avoid old-style figures in data contexts
- Format consistently: either all abbreviated (K, M, B) or all spelled out

## Label Placement Principles

Labels that require a legend have already failed. Aim for **direct labeling**:

1. Label the data directly at its visual location
2. Align label to the nearest visual anchor (end of bar, top of arc, center of circle)
3. Use short leaders (thin lines) only when direct placement is impossible
4. Never rotate text more than 30° from horizontal — vertical labels reduce reading speed by ~40%
5. Use contrast (white text on dark fill, or dark text on light fill) rather than leader boxes

### Annotation vs. label
- **Label**: identifies a data element (country name, year, category)
- **Annotation**: interprets a data element ("peak emissions year", "policy change")

Annotations earn more visual weight than labels — slightly larger, often set apart with a thin rule or bracket, and written in full sentences.

## Integrating Type with Geometry

When text lives inside or alongside complex geometry:

- **Radial layouts**: set labels tangent to the arc, or rotate to match the angle — but only if the arc span is ≥ 30°
- **Small multiples**: use consistent label positions across all facets; the reader's eye should never hunt
- **Dense data**: reduce label count — label every 5th item, or use interactive hover in digital contexts
- **Negative space**: reserve a column or quadrant of the layout for explanatory text; never fight the data for space

## Editorial Voice in Annotations

The best information designers write annotations like editors, not statisticians:

- "More than 40 countries reported no data" — not "n/a: 40+"
- "A sharp fall begins here" — not "local minimum at year X"
- Use the second person sparingly but powerfully: "You are here" on a scale puts the reader in the data

Write annotations in the present tense, active voice, and at the reading level of the target publication.
