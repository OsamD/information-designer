# The Information Designer

Claude Code skills for information design — data narrative, geometry, color, typography, annotation, and composition.

Inspired by the work of [Federica Fragapane](https://www.behance.net/FedericaFragapane).

---

## Install

```bash
npx skills add YOUR_GITHUB_USERNAME/information-designer --all
```

Or pick only what you need:

```bash
npx skills add YOUR_GITHUB_USERNAME/information-designer --skill data-narrative,color-semantics
```

Restore a team's exact skill set from the lock file:

```bash
npx skills experimental_install
```

---

## Skills

| Skill | What it covers |
|-------|---------------|
| [`data-narrative`](#data-narrative) | Story structure, information hierarchy, form selection |
| [`geometric-encoding`](#geometric-encoding) | Mapping data to shape, angle, radius, and area |
| [`color-semantics`](#color-semantics) | Palettes, semantic roles, accessibility |
| [`typographic-structure`](#typographic-structure) | Hierarchy, labels, annotation writing, typeface selection |
| [`custom-svg-viz`](#custom-svg-viz) | Bespoke SVG construction, computed geometry, print export |
| [`data-annotation`](#data-annotation) | Editorial annotations that interpret, not just describe |
| [`layout-composition`](#layout-composition) | Grid systems, visual weight, white space, multi-format |

---

### `data-narrative`

Structure raw data as a visual story with a three-beat arc: context → revelation → implication. Covers information hierarchy, form selection by data nature, and working process from headline to final form.

**Trigger**: "make this data tell a story", "build an infographic", "visualize this dataset"

---

### `geometric-encoding`

Map data dimensions to geometric primitives — circles, arcs, radii, angles, organic forms. Covers radial layout construction, SVG path math, perceptual accuracy of encodings, and the principle of encoding restraint.

**Trigger**: "custom visualization", "radial chart", "geometric data design", "non-standard chart"

---

### `color-semantics`

Design intentional color systems with defined roles for every hue. Covers categorical, sequential, and diverging palettes; WCAG accessibility; grayscale compatibility; and the editorial philosophy behind restrained, purposeful color.

**Trigger**: "color palette", "accessible colors", "color for data", "color scheme"

---

### `typographic-structure`

Typography as a structural and aesthetic element: a four-level hierarchy, direct labeling over legends, annotation voice, typeface selection for data contexts, and tabular number formatting.

**Trigger**: "font choice", "label placement", "text in chart", "typography for data"

---

### `custom-svg-viz`

Build bespoke SVG visualizations with complete control — canvas setup, layer architecture, coordinate computation, polar-to-Cartesian math, and print-quality export standards. Covers when to build custom versus use a library.

**Trigger**: "custom SVG", "hand-crafted viz", "D3 chart", "print-ready infographic"

---

### `data-annotation`

Write and place annotations that guide interpretation rather than repeat what the geometry already shows. Covers the distinction between title, label, annotation, and caption — with editorial voice, placement rules, and a revision checklist.

**Trigger**: "add annotations", "highlight this point", "make the chart argue", "editorial callout"

---

### `layout-composition`

Orchestrate multiple elements into a coherent whole using column and modular grids, visual weight hierarchy, and active white space. Includes the three-second test, composition patterns, and multi-format adaptation (print, editorial, social, screen).

**Trigger**: "layout", "composition", "grid", "how to arrange", "white space"

---

## Philosophy

> Information design is not charting data. It is authoring a point of view with data.

- Form follows the nature of the data, not convention
- Restraint is a design decision, not a limitation
- Every element encodes meaning or is removed
- Typography and geometry are equal partners
- The reader's experience is the only measure of success

---

## Update

```bash
npx skills update
```

---

## License

MIT
