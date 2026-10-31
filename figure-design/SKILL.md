---
name: "figure-design"
description: "Design and critique scientific and data figures: choose a chart type for a purpose, size the figure to a conference or journal, pick accessible colors, encode every condition redundantly, convey the takeaway visually without captions, and cut chartjunk. Grounded in Edward Tufte's principles plus CASRAI, Nature, and paper-writing practice. Use when Codex needs to create, compare, review, or improve charts, dashboards, paper figures, teaser figures, sparklines, small multiples, or other dense visual displays, or to check graphical integrity, data-ink ratio, lie factor, labeling, scaling, palettes, layout, venue size, or export format."
---

# Figure Design

Design for clarity, density, and truthfulness. Prefer the simplest display that preserves comparison, context, and evidence.

## Hard Defaults

Apply to every figure unless the user overrides one for a specific figure. Details in `references/figure-design-practice.md` section 0.

1. **No chartjunk.** Never include a visual element that is not necessary to comprehend the data or that distracts from it. Cut back on everything unnecessary: in-plot titles, gridlines, backgrounds, borders, top/right spines, shadows, gradients, 3D, decorative icons, redundant legends, excess ticks.
2. **The takeaway is visual, not written.** No figure title, caption, or findings text inside the figure. The message must be unmistakable from order, emphasis, reference marks, and layout alone. Only axis labels, tick labels, direct series labels, and panel letters are text.
3. **Accessible color by default.** Do not default to grayscale. Use a colorblind-safe palette matched to the data type (Okabe-Ito, viridis, symmetric diverging). Never red-green, never rainbow. Reserve gray for axes, references, and non-focal context.
4. **Multiple signals for every distinction.** Encode each condition with at least two independent channels carrying the same mapping: color plus marker shape, line style, hatch/patch, size, facet, or direct label. Keep the mapping identical across all panels and figures. It must survive grayscale and a colorblind simulator.
5. **Size to the venue.** Set the canvas to the conference or journal column/text width before plotting, create it at final size, and set text in points at that size. See `references/venue-figure-sizes.md`. Ask for the venue and year if unknown.

## Workflow

1. Clarify the analytical question.
   - Identify the key comparison, trend, outlier, or mechanism.
   - State the single message of the figure in one sentence. One idea per plot.
   - Identify the target venue and slot (one column or full width).
   - For papers, sketch the figure and its expected result before the data exists; design experiments around the figure.
2. Choose the display that carries the most information with the least noise.
   - Look up the purpose in `references/chart-type-catalog.md`; check the Tufte stance.
   - Use tables, sparklines, or small multiples for dense comparison.
   - Use line charts for time series with minimal scaffolding.
   - Avoid pies, 3D effects, dual-axis tricks, and ornamental chart elements.
   - If one figure must answer more than one question, split it into panels.
3. Encode data directly and keep structure honest.
   - Keep baselines, ranges, and scales explicit. Bars start at zero.
   - Check whether the visual effect is proportional to the data effect.
   - Pick the palette by data type, then add the redundant channels.
   - Show the baseline or control in frame so "compared to what?" is answered visually.
4. Make the takeaway visible.
   - Order categories by value or by the argument; put the key comparison adjacent on a shared scale.
   - Give the focal series the strongest weight and saturation; keep context series lighter but identifiable.
   - Order panels to follow the explanation and use whitespace to group them along the axis of variation.
5. Tighten the graphic.
   - Apply the cut list (`references/figure-design-practice.md` section 0.5). Delete every element whose removal loses no information.
   - Move labels onto the data; prefer direct labels to legends.
   - Check text legibility at final printed size; export vector with live text.
6. Review.
   - Ask whether a reader who covers the caption can state the message in one sentence.
   - Ask whether it answers "compared to what?"
   - Ask whether every condition is identifiable in grayscale.
   - Ask whether the design is doing work the data should be doing.
   - Run the checklist in `references/figure-design-practice.md` section 13.

## Use the References

- Read `references/figure-design-practice.md` when planning, building, or reviewing any figure: hard defaults, storyboarding, one idea per plot, panel order, teaser figures, palettes, typography, layout, hierarchy, pitfalls, export, and the review checklist.
- Read `references/venue-figure-sizes.md` when setting figure dimensions or font sizes for a conference, journal, or slide deck.
- Read `references/chart-type-catalog.md` when choosing or replacing a chart type: question-to-chart table and a purpose-grouped list of the chart types documented at visualizing.org (related variants share rows) across comparison, distribution, correlation, part-to-whole, time series, flow, hierarchy, network, geospatial, statistical, financial, scientific, sets, and multi-dimensional purposes, each with a Prefer/OK/Caution stance.
- Read `references/tufte-principles.md` for the core Tufte test, graphical integrity, chartjunk, lie factor, and small multiples.
- Read `references/analytical-design.md` when the task involves sparklines, layering, micro/macro views, range-frames, confections, or causal explanation.

## Output Expectations

- Give concrete, data-specific recommendations instead of generic style advice.
- State what to remove, what to keep, and what to change.
- Name the chart type from the catalog and say why it fits the comparison.
- If proposing a revision, describe the expected comparison or insight it should improve.
- For paper figures, report the one-sentence message, target venue and canvas size (inches), panel order, and the condition-to-encoding map (color, marker, line style, hatch).
- When writing plotting code, set `figsize` to the venue width, use the chosen palette and redundant channels, omit titles and captions, and export vector PDF.
