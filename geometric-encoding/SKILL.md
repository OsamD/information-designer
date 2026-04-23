---
name: geometric-encoding
description: Map data dimensions to geometric primitives — circles, arcs, radii, angles, lines, and organic forms — to create bespoke, non-standard visualizations. Use when asked to design custom, hand-crafted data visualizations that go beyond bar/line/pie charts. Triggers on "custom visualization", "unique chart", "geometric data art", "radial chart", "circular layout", or any request for visually distinctive information design.
license: MIT
metadata:
  author: information-designer
  version: "1.0.0"
---

Geometry is the grammar of data. Every dimension of data can be encoded in a geometric property. The goal is to choose encodings that feel *inevitable* — where the shape reveals the data's nature rather than imposing structure on it.

## The Encoding Vocabulary

Map data variables to geometric properties with intention:

| Data type | Geometric encoding |
|-----------|-------------------|
| Magnitude / quantity | Radius, area, length |
| Category | Shape family, fill pattern |
| Time / sequence | Angular position (radial), horizontal position (linear) |
| Proportion | Arc angle, filled sector |
| Intensity / density | Opacity, stroke weight |
| Relationship | Connecting line, chord |
| Hierarchy | Concentric rings, nested areas |

**Rule**: use at most 3 encodings simultaneously. Beyond 3, the reader decodes, not sees.

## Radial Layouts

Radial forms are powerful for cyclic data (time, seasons, weekly patterns) and for giving each data point equal visual status — unlike bar charts which privilege leftmost items.

Building a radial layout:
1. Map the cyclic variable to angle (0–360°)
2. Map the quantitative variable to radius (inward = low, outward = high, or inverted)
3. Use concentric rings for multiple series
4. Anchor labels at the perimeter, never inside dense geometry

## Organic and Irregular Forms

Not all data encodes naturally into regular grids or circles. Use organic forms when:
- Data has biological, geographic, or human-body subject matter
- The irregularity is itself the message (inequality, disorder)
- You want to evoke feeling, not just convey fact

Construct organic forms as SVG paths with controlled irregularity: Bézier curves with slight randomness, or D3 `curveBasis` / `curveCardinal` interpolation.

## Constructing Custom Forms in SVG

Core SVG elements for information design:

```svg
<!-- Arc / sector -->
<path d="M cx cy L x1 y1 A rx ry 0 large-arc sweep x2 y2 Z" />

<!-- Radial segment with varying thickness -->
<path d="M x1 y1 A r1 r1 0 0 1 x2 y2 L x3 y3 A r2 r2 0 0 0 x4 y4 Z" />

<!-- Connecting chord -->
<path d="M x1 y1 Q mx my x2 y2" stroke-width="..." opacity="..." />
```

Always compute coordinates programmatically — define the data → geometry mapping as a pure function, then render.

## Principles of Geometric Restraint

- **Perceptual accuracy**: area is harder to read than length; angle is harder than position. Use the most perceptually precise encoding your design permits.
- **Negative space**: the space between geometric elements carries meaning. Let data breathe.
- **Alignment as meaning**: if two elements share an edge, the reader assumes a relationship. Be deliberate.
- **One dominant form**: choose one geometric motif and repeat it at multiple scales (fractal logic). Mixing circles, bars, and lines in one piece without hierarchy creates noise.

## Sketching Protocol

Before coding, sketch with compass and ruler:
1. Draw the bounding area (circle, rectangle, or freeform)
2. Mark the data extremes at their encoded positions
3. Trace the visual path a reader's eye follows
4. Verify the headline insight is visually obvious at arm's length
