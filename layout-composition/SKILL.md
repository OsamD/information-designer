---
name: layout-composition
description: Apply visual composition principles to information design — grid systems, white space, visual weight, and the orchestration of multiple data elements into a coherent whole. Use when designing the overall layout of an infographic, dashboard, data report, or editorial data page. Triggers on "layout", "composition", "white space", "grid", "page design", "information hierarchy", or "how to arrange" in a data visualization or design context.
license: MIT
metadata:
  author: information-designer
  version: "1.0.0"
---

Composition is the argument made visible before the reader reads a single word. A well-composed information design piece communicates its hierarchy in under three seconds.

## The Three-Second Test

Hold the piece at arm's length. In three seconds, the reader must grasp:
1. What is this about? (Headline / dominant visual)
2. What is the main finding? (Primary data element)
3. Where do I start reading? (Entry point)

If any of these fails, fix the composition before touching the data.

## Grid Systems for Information Design

### Column grid (editorial / print)
Use a 12-column grid for maximum flexibility:
- Headlines: span all 12 columns
- Primary visualization: 8–12 columns
- Supporting charts or text: 4–6 columns
- Caption / source: 4–6 columns, bottom-right

### Modular grid (dashboard / multi-panel)
For pieces with several distinct visualizations:
- Define a base module (e.g., 200×200px)
- Allow visualizations to span 1×1, 2×1, 2×2, or 3×2 modules
- Maintain consistent gutter width (typically 16–24px for screen, 6–8mm for print)

### Radial / freeform composition
When the central visualization is circular or radial:
- Center the visualization on the horizontal axis (not geometrically centered — place it slightly above center, as the eye reads the upper half first)
- Use the surrounding rectangular space for title, annotations, and legend
- Never let explanatory text compete with the data for the visual center

## Visual Weight and Hierarchy

Visual weight is determined by size, contrast, and density. Manage it deliberately:

| High visual weight | Low visual weight |
|-------------------|------------------|
| Large, filled shapes | Small, outlined shapes |
| Dark on light (or light on dark) | Mid-tone on mid-tone |
| Saturated color | Desaturated / neutral color |
| Complex, dense elements | Simple, sparse elements |

**Rule**: one element per composition should have maximum visual weight — the primary data visualization or headline. Everything else must yield.

## White Space as an Active Element

White space is not wasted space — it is the breath between arguments.

- **Macro white space**: margins, the space between major sections. Signals importance and allows the eye to rest before the next idea.
- **Micro white space**: padding within text blocks, gaps between data elements. Prevents visual crowding and improves legibility.

Minimum comfortable margins:
- Screen: 40–60px from edge to any content
- Print (A4): 15–20mm all sides
- Never place text within 8px/4mm of a border or edge

## Composition Patterns for Information Design

### Anchored-center
Single large visualization in the center, supporting elements arranged symmetrically around it. Works for standalone pieces with a single dominant dataset.

### Editorial split
Left: visualization(s). Right: explanatory text and annotations. Reads left-to-right. Works for print and editorial.

### Progressive disclosure
Top: headline + single key number. Middle: primary visualization. Bottom: supporting detail and source. Works for vertical scrolling digital formats.

### Small multiples
Repeated layout of the same visualization type across categories or time periods. Powerful for comparison. Keep each panel minimal — all labeling on the first panel only, subsequent panels show data only.

## Composition Checklist

- [ ] Three-second test passes: hierarchy is immediately legible
- [ ] One dominant visual element; everything else supports it
- [ ] Margins are consistent and generous
- [ ] No elements touch the edge of the canvas
- [ ] Text blocks have a clear reading direction (avoid two columns that compete)
- [ ] The title and primary visualization are in the upper half of the canvas
- [ ] Source / caption is bottom-right (last thing read, not forgotten)
- [ ] The piece reads coherently in grayscale

## Responsive and Multi-Format Considerations

| Format | Priority adjustment |
|--------|-------------------|
| **Instagram square** (1:1) | Drop all secondary charts; headline + one visualization only |
| **Story / vertical** (9:16) | Stack elements vertically; increase type size 20% |
| **A4 print** | Full composition; body text minimum 9pt |
| **Wide-screen / 16:9** | Use horizontal split or centered with large margins |

Design for the primary format first, then adapt. Never design a compromise that works poorly in all formats.
