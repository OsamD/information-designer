---
name: information-designer
description: Master orchestrator for the full information design workflow. Chains data-narrative → geometric-encoding → color-semantics → typographic-structure → custom-svg-viz → data-annotation → layout-composition in sequence to produce a complete, publication-ready information design piece. Use when asked to design a complete infographic, data visualization, or editorial data piece from scratch. Triggers on "design this", "create an infographic", "full information design", "make a data piece", or any end-to-end design request involving data.
license: MIT
metadata:
  author: information-designer
  version: "1.0.0"
---

This skill orchestrates the full information design pipeline. Each phase must complete before the next begins. Do not skip phases, do not reorder them — the output of each phase is the input to the next.

## Pipeline

```
data-narrative
      ↓
geometric-encoding
      ↓
color-semantics
      ↓
typographic-structure
      ↓
custom-svg-viz
      ↓
data-annotation
      ↓
layout-composition
      ↓
  DELIVERABLE
```

---

## Phase 1 — `data-narrative`

**Goal**: establish the argument before any visual decision.

Apply the `data-narrative` skill in full:

1. Write the headline insight (7 words or fewer — the one truth this piece must communicate)
2. List the 3–5 data points that prove the headline
3. Assign each data point to a narrative beat: Context / Revelation / Implication
4. Name the data's nature (change over time? part-to-whole? comparison? network?)

**Output required before proceeding**:
- [ ] Headline written
- [ ] Information hierarchy: Tier 1 / Tier 2 / Tier 3 defined
- [ ] Narrative arc mapped to the data

---

## Phase 2 — `geometric-encoding`

**Goal**: choose the visual form that makes the headline feel inevitable.

Apply the `geometric-encoding` skill:

1. Select the form family based on the data's nature (from Phase 1)
2. Map each data variable to a geometric property (radius, angle, area, position, opacity, stroke weight)
3. Confirm: max 3 simultaneous encodings
4. Sketch or describe the dominant geometric motif
5. Verify the headline is visually confirmed by the chosen form — not contradicted

**Output required before proceeding**:
- [ ] Form type selected and justified
- [ ] Data → geometry mapping table complete
- [ ] Dominant geometric motif described

---

## Phase 3 — `color-semantics`

**Goal**: assign a color role to every hue before any color is applied.

Apply the `color-semantics` skill:

1. Define the palette type (categorical / sequential / diverging)
2. Assign a role to each color: Primary / Secondary / Accent / Neutral / Absence
3. Check: does the palette work in grayscale?
4. Check: does the palette pass WCAG AA contrast?
5. Check: is the highest-saturation color reserved for the single most important element?

**Output required before proceeding**:
- [ ] Full palette defined with hex values and roles
- [ ] Grayscale check passed
- [ ] Accessibility check passed

---

## Phase 4 — `typographic-structure`

**Goal**: establish the four-level typographic hierarchy and all label/annotation rules.

Apply the `typographic-structure` skill:

1. Select typeface(s) — one for data/numbers, one for prose (or one across all levels)
2. Define the four typographic levels: Display / Subhead / Body / Caption with size ratios
3. Confirm all data elements use direct labels (no legend if avoidable)
4. Write the Display-level text (headline) in its final form
5. Draft all Subhead-level text (category names, section labels)

**Output required before proceeding**:
- [ ] Typeface(s) chosen
- [ ] Four-level hierarchy defined
- [ ] Headline text finalized
- [ ] Label strategy confirmed (direct / legend / hybrid)

---

## Phase 5 — `custom-svg-viz`

**Goal**: construct the visualization.

Apply the `custom-svg-viz` skill:

1. Set the canvas: viewBox dimensions, coordinate system, output format (web / print)
2. Define the layer stack: background → grid → data → annotations → labels
3. Compute all geometry programmatically from the data → geometry mapping (Phase 2)
4. Apply colors from the palette (Phase 3) to each layer
5. Place typography at the correct levels (Phase 4)
6. Run the quality checklist: no overlapping labels, no clipped text, no broken paths

**Output required before proceeding**:
- [ ] SVG file or code generated
- [ ] All data elements rendered
- [ ] Colors and typography applied
- [ ] Quality checklist passed

---

## Phase 6 — `data-annotation`

**Goal**: add editorial voice that interprets the data.

Apply the `data-annotation` skill:

1. Identify 1 primary annotation (the key insight — what the geometry cannot say alone)
2. Identify 2–4 secondary annotations (supporting moments)
3. Write each annotation: present tense, active voice, max 12 words, no "this shows..."
4. Place each annotation: as close to its referent as legible whitespace allows
5. Confirm: every annotation adds information the visual cannot convey alone

**Output required before proceeding**:
- [ ] Primary annotation written and placed
- [ ] Secondary annotations written and placed
- [ ] Revision checklist passed: no annotation could be removed without losing meaning

---

## Phase 7 — `layout-composition`

**Goal**: orchestrate all elements into a coherent whole and deliver.

Apply the `layout-composition` skill:

1. Run the three-second test: headline visible, main finding clear, entry point obvious
2. Confirm one dominant visual element — everything else yields
3. Check margins and white space (no element touching canvas edge)
4. Verify reading direction: title → primary visualization → supporting detail → caption
5. Adapt for the target format (print A4, editorial, 1:1 social, 9:16 story, 16:9 screen)
6. Confirm source and methodology are in the caption

**Final deliverable checklist**:
- [ ] Three-second test passes
- [ ] Visual hierarchy is unambiguous
- [ ] Margins are consistent and generous
- [ ] Source cited in caption
- [ ] SVG/PDF/PNG exported at correct resolution
- [ ] Piece reads in grayscale

---

## On Feedback and Iteration

After delivering the piece, offer exactly three options to the reader:

1. **Revise the argument** — go back to Phase 1 (data-narrative)
2. **Change the form** — go back to Phase 2 (geometric-encoding)
3. **Refine the surface** — adjust color, type, or annotation in Phases 3–6

Never revise all phases simultaneously. Identify the earliest phase where the issue originates and rerun the pipeline from there.
