# The Information Designer

A skill set for Claude Code that encodes the practice of information design — transforming data into intentional, beautiful, argued visual communication.

Inspired by the work of [Federica Fragapane](https://www.behance.net/FedericaFragapane), whose information design practice demonstrates that data visualization is a form of authorship: rigorous, geometric, and deeply human.

---

## Install

```bash
npx skills add YOUR_GITHUB_USERNAME/information-designer
```

Install all skills at once:

```bash
npx skills add YOUR_GITHUB_USERNAME/information-designer --all
```

Install specific skills only:

```bash
npx skills add YOUR_GITHUB_USERNAME/information-designer --skill data-narrative,color-semantics
```

Restore from lock file (for teams sharing the same skill set):

```bash
npx skills experimental_install
```

---

## Skills

### `data-narrative`
Structure raw data as a visual story with a three-beat arc: context, revelation, implication. Defines the information hierarchy before any visual decision is made.

**Use when**: turning a dataset into an infographic, editorial piece, or visual essay.

---

### `geometric-encoding`
Map data dimensions to geometric primitives — circles, arcs, radii, angles, organic forms. Covers radial layouts, SVG path construction, and perceptual accuracy of visual encodings.

**Use when**: designing a custom, non-standard visualization or choosing how to visually represent a dataset.

---

### `color-semantics`
Design intentional color systems: categorical palettes, sequential/diverging scales, semantic color roles. Includes accessibility requirements and editorial color philosophy.

**Use when**: choosing or auditing color in a data visualization or infographic.

---

### `typographic-structure`
Typography as a structural element: four-level hierarchy, direct labeling, annotation writing, typeface selection, and number formatting for data contexts.

**Use when**: placing text within or alongside data visualizations.

---

### `custom-svg-viz`
Build bespoke SVG data visualizations with complete layout control — coordinate systems, computed geometry, layer architecture, and print-export standards.

**Use when**: standard chart libraries cannot achieve the required visual form, or when print-quality SVG output is needed.

---

### `data-annotation`
Write and place strategic annotations that guide interpretation — distinguishing labels from annotations from titles, writing with editorial voice, and sequencing for visual flow.

**Use when**: a visualization needs to move from descriptive to interpretive.

---

### `layout-composition`
Visual composition principles: grid systems, white space, visual weight hierarchy, and multi-format adaptation (editorial, social, print, screen).

**Use when**: designing the overall layout of an infographic, data report, or multi-panel dashboard.

---

## Philosophy

> "Information design is not charting data — it is authoring a point of view with data."

These skills encode a specific practice of information design:
- **Form follows data nature**, not convention
- **Restraint is a decision**, not a limitation
- **Every element encodes meaning** or is removed
- **Typography and geometry are equal partners**
- **The reader's experience is the only measure**

---

## Update

```bash
npx skills update
```

---

## License

MIT
