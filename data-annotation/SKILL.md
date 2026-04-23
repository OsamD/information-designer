---
name: data-annotation
description: Write and place strategic text annotations that guide interpretation of data visualizations — turning raw charts into argued, opinionated visual essays. Use when a data visualization needs editorial voice, when key moments or anomalies must be highlighted, or when a piece needs to move from descriptive to interpretive. Triggers on "add annotations", "explain the data", "highlight this point", "editorial callout", or "make the visualization tell a story".
license: MIT
metadata:
  author: information-designer
  version: "1.0.0"
---

An annotation is the designer's voice in the visualization. It says: *here, pay attention here, this is what matters*. Without annotations, a chart presents; with them, it argues.

## Annotation vs. Label vs. Title

| Element | Function | Example |
|---------|----------|---------|
| **Title** | States the conclusion | "Emissions fell 40% after the 2015 agreement" |
| **Label** | Identifies an element | "France", "2019", "42%" |
| **Annotation** | Interprets an element | "Sharpest single-year drop since 1990" |
| **Caption** | Credits and qualifies | "Source: IEA, 2024. Excludes aviation." |

Never confuse these roles. A title that merely describes ("CO₂ emissions by country, 2000–2023") is a wasted opportunity.

## Writing Effective Annotations

### The annotation must add information the geometry cannot
If the chart already shows a line going up, writing "trend increases" adds nothing. Instead:
- Name the cause: "Tax reform takes effect"
- Give the human scale: "Equivalent to removing 2M cars from the road"
- Compare: "Twice the rate of the previous decade"
- Provoke: "The year the target was supposed to be met"

### Annotation voice
- Present tense, active voice
- Max 12 words per annotation; prefer 6–8
- Never start with "This shows..." or "Data indicates..."
- Write as if speaking to an intelligent reader who has 10 seconds

### Annotation hierarchy
A piece should have at most:
- 1 **primary annotation** (the key insight, visually dominant)
- 2–4 **secondary annotations** (supporting moments)
- Any number of **tertiary labels** (identification, not interpretation)

## Placement Principles

**Proximity**: place the annotation as close to its referent as legible whitespace allows. A reader should not have to search for what is being annotated.

**Leader lines**: use when the annotation must be offset from the data point.
- Keep lines thin (0.5–0.75pt), neutral gray
- Use a right angle bend (L-shape) rather than a diagonal for precision
- Terminate with a small dot at the data point, no arrowhead unless directionality matters

**Orientation**: keep annotations horizontal whenever possible. Rotated text slows reading by 30–40%.

**Contrast**: annotation text must contrast with both the background and any overlapping data elements. Use a small white or tinted background rectangle (opacity 0.85) when placing text over complex geometry.

## Positioning Annotations for Visual Flow

The reader's eye enters at the most visually prominent element and moves toward explanatory text. Design for this flow:

1. **Establish the visual anchor** (the most striking data element)
2. **Place the primary annotation** adjacent to or above the anchor
3. **Sequence secondary annotations** in the order the eye naturally moves (left→right, or top→bottom)
4. **Reserve the bottom-left** for source/caption — the last thing read

In radial layouts, place annotations in the outer ring or in a dedicated rectangular panel alongside the circle — never inside dense geometry.

## Annotation for Digital vs. Print

| Medium | Approach |
|--------|----------|
| **Print / static** | All annotations visible at once; must not overlap; designed for a single reading distance |
| **Digital / interactive** | Use hover tooltips for secondary annotations; show only primary annotations by default |
| **Scrollytelling** | Annotations appear sequentially as the reader scrolls; each triggers a visual state change |

## Revision Checklist

Before finalizing annotations:
- [ ] Every annotation adds information the visual cannot convey alone
- [ ] No annotation could be removed without losing meaning
- [ ] Primary annotation states the conclusion, not the observation
- [ ] All annotations are horizontally set (or justified rotations < 30°)
- [ ] Source and methodology are in the caption, not the annotations
- [ ] Read all annotations aloud — if they sound like a report, rewrite them
