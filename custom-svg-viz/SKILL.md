---
name: custom-svg-viz
description: Build bespoke, hand-crafted SVG data visualizations that go beyond standard chart libraries — custom geometry, precise layout control, and export-ready output. Use when asked to create a unique or artisanal data visualization, when standard chart libraries produce insufficient control, or when output must be print-quality SVG. Triggers on "custom chart", "SVG visualization", "hand-crafted viz", "D3 chart", "print-ready infographic", or "unique data design".
license: MIT
metadata:
  author: information-designer
  version: "1.0.0"
---

Custom SVG visualizations give complete control over every pixel. They are appropriate when the visual form is itself part of the message — when standard library output would betray the design intent.

## When to Build Custom vs. Use a Library

| Situation | Approach |
|-----------|----------|
| Standard chart type, standard output | Use Chart.js, Recharts, or Observable Plot |
| Non-standard geometry, standard data | Use D3.js for layout math, custom SVG for rendering |
| Fully bespoke form, print quality | Hand-authored SVG with computed coordinates |
| Interactive + bespoke | D3 + SVG or Canvas |

Custom SVG is the right choice when the visual form has no library equivalent.

## SVG Canvas Setup

Always establish the coordinate system explicitly:

```svg
<svg
  xmlns="http://www.w3.org/2000/svg"
  viewBox="0 0 800 600"
  width="800"
  height="600"
  style="font-family: 'GT America', 'Inter', sans-serif;"
>
  <!-- Define reusable elements -->
  <defs>
    <clipPath id="chart-area">
      <rect x="80" y="40" width="680" height="500" />
    </clipPath>
  </defs>

  <!-- Layers (back to front) -->
  <g class="layer-background" />
  <g class="layer-grid" />
  <g class="layer-data" clip-path="url(#chart-area)" />
  <g class="layer-annotations" />
  <g class="layer-labels" />
</svg>
```

Layer order matters: render backgrounds first, data in the middle, annotations and labels last.

## Computing Geometry Programmatically

Never hardcode coordinates for data-driven elements. Use a mapping function:

```javascript
// Linear scale (D3-style, or manual)
function scale(value, domainMin, domainMax, rangeMin, rangeMax) {
  return rangeMin + ((value - domainMin) / (domainMax - domainMin)) * (rangeMax - rangeMin);
}

// Polar to Cartesian (for radial layouts)
function polarToCartesian(cx, cy, radius, angleDeg) {
  const rad = (angleDeg - 90) * (Math.PI / 180);
  return {
    x: cx + radius * Math.cos(rad),
    y: cy + radius * Math.sin(rad),
  };
}

// SVG arc path
function arcPath(cx, cy, r, startAngle, endAngle) {
  const start = polarToCartesian(cx, cy, r, endAngle);
  const end = polarToCartesian(cx, cy, r, startAngle);
  const largeArc = endAngle - startAngle > 180 ? 1 : 0;
  return `M ${start.x} ${start.y} A ${r} ${r} 0 ${largeArc} 0 ${end.x} ${end.y}`;
}
```

## Typography in SVG

```svg
<!-- Headline -->
<text x="80" y="36" font-size="24" font-weight="700" fill="#1a1a2e">Headline insight</text>

<!-- Data label (right-aligned) -->
<text x="760" y="200" text-anchor="end" font-size="13" fill="#457b9d">Category A</text>

<!-- Annotation with leader -->
<line x1="340" y1="180" x2="380" y2="160" stroke="#999" stroke-width="0.75" />
<text x="385" y="158" font-size="11" fill="#666">Notable spike in 2019</text>
```

Use `text-anchor="middle"` for centered labels (e.g., axis centers), `"start"` for left-aligned, `"end"` for right-aligned.

## Print Export Standards

For editorial / print delivery:
- **ViewBox**: use a 1:1 px-to-pt ratio. A4 portrait at 300dpi = 2480×3508px
- **Fonts**: embed as `<style>@font-face {...}</style>` or convert text to paths (`font-to-path`) for guaranteed fidelity
- **Strokes**: never use `stroke-width` below 0.5pt (≈0.7px at 96dpi) — invisible in print
- **Colors**: use CMYK-safe RGB values; avoid neon or screen-only colors
- **No CSS filters**: Gaussian blur and drop-shadow do not render correctly in all print workflows

Deliver as:
- `.svg` for web and editorial editorial hand-off
- `.pdf` (exported from Illustrator or Inkscape) for print production
- `.png` at 2× or 3× for digital publication

## Quality Checklist Before Delivery

- [ ] Headline insight is legible at 50% zoom
- [ ] No overlapping labels or text clipping
- [ ] All data values are directly labeled or have a clear legend
- [ ] Color passes accessibility check in grayscale
- [ ] SVG validates (no broken paths, no orphaned `<defs>`)
- [ ] File size is reasonable (< 500KB for web, uncompressed SVG)
- [ ] Source data and methodology are cited in the caption
