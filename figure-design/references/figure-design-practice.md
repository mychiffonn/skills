# Figure Design Practice

Use this reference when planning, building, or reviewing figures for papers, reports, and talks. It turns Tufte's principles and current scientific-figure guidance into a production workflow.

Sources:
- Sophie Wang, "behind the scenes of paper writing" (https://www.sophielwang.com/blog/paper-writing). Process and craft: storyboarding, panel logic, color systems, layout, export.
- CASRAI, "Designing Effective Scientific Figures" (https://casrai.org/guides/designing-effective-scientific-figures). Chart-type fit, palettes, pitfalls, checklist.
- Nature research figure guide (https://research-figure-guide.nature.com/figures/building-and-exporting-figure-panels). Sizing, fonts, accessible palette, decorative icons, formats.
- Venue sizes: `venue-figure-sizes.md` (style files and author guides, cited there).

Where these sources conflict with the Tufte defaults, the user's defaults in section 0 win and the reconciliation is stated inline.

## 0. Hard Defaults

Apply these unless the user explicitly overrides them for a specific figure.

### 0.1 The Takeaway Must Be Visible, Not Written

- Do not add a figure title, caption, subtitle, or findings text (e.g., "Method A improves accuracy by 12%", significance prose, "Key insight" boxes) inside the figure. The caption lives in the document.
- The takeaway must be unmistakable from the visual design alone. A reader who glances for three seconds and never reads a caption should be able to say what the figure shows.
- Carry the message with encoding, not words:
  - Order: sort categories by value, or by the argument; put the key comparison adjacent.
  - Emphasis: the focal series gets the strongest weight, saturation, and size; context series recede (lighter, thinner) but stay visible and keep their identity.
  - Reference: show the baseline, control, chance level, or target as a visible reference line or marker so "compared to what?" is answered in the frame.
  - Gap and annotation by geometry: a bracket, dumbbell, or shaded region showing the difference is allowed when it is a data mark, not prose.
  - Panel order and spacing follow the explanation (sections 3 and 9).
- Text that stays in the figure: axis labels with units, tick labels, direct series labels, panel letters, and legend entries when direct labels are impossible. Nothing that states the conclusion.
- If the message is not obvious without a caption, redesign the encoding (fewer series, better order, stronger emphasis). Do not patch it with text.
- Test: cover the caption and the text; state the message in one sentence from the figure alone. If two people state different messages, the hierarchy is wrong.

### 0.2 Redundant Encoding: Every Distinction Gets Multiple Signals

Encode every category or condition with at least two independent visual channels that carry the same mapping. Never rely on a single channel, color above all.

| Channel | Use for |
| --- | --- |
| Color (accessible palette) | Condition identity |
| Marker shape | Condition identity in scatter and line charts (circle, square, triangle, diamond) |
| Line style | Condition identity in line charts (solid, dashed, dotted, dash-dot) |
| Fill pattern / hatch / patches | Condition identity in bars, areas, and boxes |
| Size | Importance or magnitude, only when it is part of the same mapping; never as the only cue |
| Facet / panel | Group identity; position in the grid repeats the mapping |
| Direct label | Condition name placed on or next to the mark, replacing the legend where possible |
| Position / order | The same sequence in legend, bars, and panels |

Rules:
- The same condition keeps the same color, marker, line style, and hatch in every panel and every figure of the paper.
- Redundant channels must agree. Do not give one condition a circle in panel a and a square in panel b.
- Test in grayscale and under a colorblind simulator: every condition must still be identifiable. Fail the figure if it is not.
- Direct labels beat legends. Use a legend only when labels would collide, and then order entries as the marks appear.
- Redundancy is not decoration: use the lightest second channel that disambiguates (marker shape or line style before hatching or size).

### 0.3 Accessible, Colored Palette by Default

- Use color by default. Do not default to grayscale. (This replaces Tufte's "grayscale by default".)
- Choose a colorblind-safe palette matched to the data type (section 7). Never red-green, never rainbow/jet.
- Use gray only for what is not condition identity: axes, reference lines, context or "other" series, and non-focal elements.
- Text color is black or near-black on a high-contrast background. Do not color text, except where color is the legend.

### 0.4 Size to the Venue

- Size the canvas to the target venue's column or text width before plotting; see `venue-figure-sizes.md`.
- Ask for the venue and year if the user has not said. If unknown, use a conservative one-column width (about 3.25 in) and say so.
- Create the figure at final size; set text in points at that size.

### 0.5 No Chartjunk, Ever

Never include any visual element that is not necessary to comprehend the information represented, or that distracts the viewer from it. Cut back on everything unnecessary.

Cut list. Remove by default; restore only when removal loses information:
- Figure titles, subtitles, and captions inside the plot (see 0.1).
- Gridlines. Keep one light axis of gridlines only if readers must read exact values and no direct values are labeled.
- Plot-area backgrounds, panel borders, boxed frames, and the top and right spines.
- Drop shadows, gradients, bevels, textures, glow, 3D, and perspective.
- Decorative icons, clip art, logos, and illustrations. Keep an icon only if it encodes data or supplies context text cannot (Nature: use text labels instead of decorative icons).
- Redundant legends, duplicate axis labels across shared axes, and tick labels on every small multiple when axes are shared.
- Excess ticks, trailing zeros, and over-precise numbers (use the precision the data supports).
- Bold, large, or colored axis lines. Axes are thin and neutral.
- Marks that repeat information without adding a signal (e.g., a data label on every bar when the axis already shows the value). Redundant encoding in 0.2 is the exception: it adds an independent channel, not repeated ink.
- Unused axis range and empty padding.
- Annotations, arrows, and callouts that restate what the geometry already shows.

Test for each non-data element: "If I delete this, does the viewer lose information needed to comprehend the data?" If no, delete it.

## 1. Design Figures Before Results (Storyboarding)

Sketch every planned figure before the data exists.

- Draw each figure by hand: axes, conditions, and the result you expect.
- Write the expected result next to the sketch. A figure that cannot state its expectation is not yet a hypothesis.
- Design the experiment around the figure, not the figure around the experiment. The sketch exposes missing conditions, baselines, and controls early.
- When results contradict the sketch, keep both. The mismatch is a finding, and the final figure may need an extra condition to separate effects (e.g., one data edit that creates a new effect vs. one that redirects an existing effect).
- A vague sketch is acceptable. It can define the measurement you still need to invent (e.g., a "flow" visual that forces you to define how to measure the links).
- Order the sketches as the argument you want the reader to follow: what the reader must see first, second, third.

Revision loop after real results arrive:

1. Compare the final figure to the sketch.
2. Re-ask which comparison matters most; change the encoding if it does not match the sketch (e.g., training curves to grouped bars when the real comparison is between final conditions).
3. Cut any panel or series that answers a different question.

## 2. One Idea per Plot

- Each plot conveys a single message. State it as a sentence before drawing.
- Remove series that answer a different question (e.g., pass@16 in a figure about single-attempt accuracy). Move them to another panel, figure, or supplement.
- Test for splitting: if explaining what is shown takes a paragraph, split or redesign the figure (CASRAI). Do not shrink the problem by adding in-figure text.
- Prefer several focused panels over one dense plot with many colors and mixed chart types.

## 3. Panel Order and Axis of Variation

- Panel order follows the explanation, not the order experiments were run or the order of interest you started with. Reorder when the story changes (e.g., lead with "what changed in the model" before "what that buys you").
- The axis of variation must make the key comparison obvious. Put the compared items adjacent, on a shared scale, in the same encoding.
- Choose the encoding by the comparison: if the question is "which condition wins at the end", grouped bars beat trajectories; if the question is "when does divergence start", lines beat bars.
- Replace a plain bar with a more explanatory form when the mechanism is structural (e.g., a branching diagram of sequences with probabilities instead of bars of next-token probability). This follows Tufte's causality principle.
- Pair conceptual diagrams with the data they explain in one composition (confection).

## 4. Teaser (Figure 1) Figure

- The teaser should carry the paper's takeaway for a reader who reads nothing else.
- Draft it after the main results exist. Picture a chalkboard explanation of the findings, then draw that.
- Show the mechanism or concept on top and the empirical result beneath it, so the reader sees how the concept becomes a measurable effect.
- Merge panels when you have one unified understanding; keep panels separate only when the understanding is separate.
- Restrict the diagram to the part that carries the idea (e.g., first few tokens, not the whole tree).

## 5. Parallel Narratives: Figures and Words

- Figures and text each tell the story and each must stand alone.
- Figures let results speak for themselves. Text explains why the problem matters, why these experiments were chosen, and what the results imply.
- Check: skim only the figures and captions, then only the text. Both should deliver the argument.

## 6. Choosing the Chart Type (Decision Check)

Answer three questions before opening plotting software.

1. What kind of variable is on each axis (categorical, ordered, continuous, time)?
2. What comparison must the reader make (magnitude between categories, trend, relationship, matrix pattern, distribution, composition)?
3. How many series or categories appear at once?

Then look up the purpose in `chart-type-catalog.md`. Core fits:

| Question | Default chart |
| --- | --- |
| Magnitude across a few discrete categories | Bar / dot plot (start bars at zero) |
| Trend over continuous or ordered variable | Line |
| Relationship between two continuous variables | Scatter |
| Pattern across a two-way matrix | Heatmap with perceptually uniform colormap |
| Many trends (more than about five lines) | Small multiples, shared axes |
| One figure answers more than one of the above | Split into panels |

Rules from CASRAI:

- Bars encode length only. Start at zero; stack only when the sum is meaningful, otherwise group.
- A connecting line implies a continuous process between points. Do not connect unordered categories.
- Scatter overplotting: use alpha, smaller points, hexbin, or density contours. Thousands of opaque points hide density.
- Heatmaps ask for magnitude by color, which is the weakest perceptual channel. Colormap choice is critical.

## 7. Color

### Palette type matches data type

| Data | Palette | Safe default |
| --- | --- | --- |
| Unordered categories | Qualitative (distinct hues) | Okabe-Ito (8 colors) |
| Ordered low-to-high | Sequential (lightness ramp) | viridis and similar perceptually uniform maps |
| Meaningful midpoint (zero change, correlation) | Diverging, symmetric about the midpoint | Blue-orange or RdBu-like; avoid red-green |

- Avoid rainbow/jet. Equal data steps must look like equal perceptual steps; otherwise small differences look large.
- Check uniformity so the palette does not exaggerate small numerical differences.

### Consistent color system across the paper

- Give each condition one color and keep it in every figure (e.g., neutral for baseline, amber for the intervention, blue for the trained model).
- Use a structured palette with numbered shades (e.g., Tailwind v4, built on OKLCH) only after checking its chosen hues under a colorblind simulator; Okabe-Ito is already verified. Reuse the same shade level for comparable elements: one level for fills, a darker level for outlines.
- Use a wide range of hues when there are many conditions. A narrow hue range lowers contrast and makes series hard to separate.
- Choose an accessible palette deliberately; do not rely on plotting defaults if you want a distinctive, coherent look.

### Accessibility

- About 1 in 12 men and about 1 in 200 women have a red-green color vision deficiency.
- Never encode a distinction with color alone. Apply redundant encoding (section 0.2): marker shape, line style, hatch, direct label, or position.
- Run the final figure through a colorblind simulator and in grayscale.
- Avoid colored text; use black text with sufficient contrast (ratio above 4.5, per Nature/WCAG 2.1 AA).

### Okabe-Ito Qualitative Palette (Nature's Colorblind-Safe Example)

| Name | Hex |
| --- | --- |
| Black | `#000000` |
| Orange | `#E69F00` |
| Sky blue | `#56B4E9` |
| Bluish green | `#009E73` |
| Yellow | `#F0E442` |
| Blue | `#0072B2` |
| Vermillion | `#D55E00` |
| Reddish purple | `#CC79A7` |

- Yellow `#F0E442` has low contrast on white; use it for large fills only, never for thin lines or text.
- For more than about 5 conditions, color alone fails; split into small multiples or highlight one focal series (section 0.1).

### Reconciliation with the Tufte Default

Tufte's grayscale default is dropped. Color is the default, chosen from an accessible palette, kept consistent across the paper, and always backed by a second channel. Gray is reserved for non-focal context, axes, and reference elements so that colored marks stay dominant.

## 8. Typography

- Use a deliberate sans-serif for plot text so figures read as distinct from body text; vary weight (light/regular/bold) to mark emphasis.
- Use monospace for code, tokens, or literal strings.
- Text must be legible at final print size. Floors and targets per element are in `venue-figure-sizes.md`. Test at final dimensions, not at full-screen zoom.

## 9. Layout and Perceptual Grouping

- Whitespace is a grouping device. Smaller gaps bind panels into a group; larger gaps separate groups.
- Make the same panel grid read as rows or as columns by changing the gaps. Put the smaller gaps along the axis you want compared (e.g., conditions within a model close together; models farther apart).
- Keep panel sizes and axes identical when panels are meant for comparison (small multiples).

## 10. Visual Hierarchy

- Size, color, and line weight decide what the viewer sees first.
- Data gets the highest contrast. Axes, ticks, and gridlines are thin and light.
- Decide the emphasis deliberately: large points emphasize the samples and their departure from a trend; a heavy line emphasizes the fit. Same data, different message.
- Squint test: the intended message must survive blurring.

## 11. Pitfalls (Integrity)

| Pitfall | Problem | Fix |
| --- | --- | --- |
| Truncated bar axis | Length no longer proportional to value | Start at zero; if truncation is unavoidable, use a dot plot or show the break explicitly |
| Non-zero or log axis on a line chart | Reader assumes linear scale | Label explicitly and make the scale visible, not only in tick values |
| 3D bar or pie | Perspective distorts magnitude | Use flat 2D; 3D only for real spatial data |
| Dual y-axes | Independent scaling can fabricate or hide correlation | Anchor both at a meaningful reference (both from zero, or both percent change); prefer two stacked panels with a shared x-axis |
| Overloaded figure | Reader cannot find the point | One message per figure; split or move to supplement |
| Chartjunk (titles, grids, frames, gradients, shadows, icons, 3D) | Competes with data | Apply the cut list in section 0.5; delete anything whose removal loses no information |
| Overplotted scatter | Dense regions saturate | Alpha, hexbin, density contours |
| Rainbow colormap | False perceptual jumps | Perceptually uniform colormap |

## 12. Export and Submission

- Export vector (PDF/SVG) with text preserved as text, not JPEG/PNG for line art. Lines and labels stay sharp on zoom and text stays selectable.
- When compressing the final PDF, use settings that preserve vectors and fonts; otherwise figures get downsampled into blurry rasters.
- Use raster only for genuinely raster content (photographs, dense images, very large point clouds).
- Design first, then check venue requirements: resolution, file format, panel labels, numbering, image integrity, and size (`venue-figure-sizes.md`). CASRAI covers these separately in "Scientific Figure Rules for Journal Submission".
- Tools: scripted plots (e.g., Matplotlib) for data panels; a vector editor (e.g., Figma) for teaser and conceptual diagrams.

## 13. Figure Review Checklist

Message and structure
- [ ] The one-sentence message is stated and the plot shows only that.
- [ ] The message is obvious from the figure alone: no in-figure title, caption, or findings text.
- [ ] The plot answers "compared to what?" (baseline, control, or alternative is in frame).
- [ ] Panel order follows the argument.
- [ ] The axis of variation puts the key comparison side by side.
- [ ] Figure and text can each carry the story alone.

Encoding and honesty
- [ ] Chart type matches the comparison (see `chart-type-catalog.md`).
- [ ] Bars start at zero; non-zero or non-linear axes are explicitly marked.
- [ ] No 3D, no dual-axis tricks, no area or volume encoding for linear quantities.
- [ ] Uncertainty (CI, SD, distribution, n) is shown or stated.

Color and type
- [ ] Palette type matches data type; colorblind-safe; not grayscale by default.
- [ ] Every condition has at least two signals (color plus marker, line style, hatch, size, facet, or direct label), identical in every figure.
- [ ] Still readable in grayscale and under a colorblind simulator.
- [ ] Each condition uses one color across the whole paper.
- [ ] Text is legible at final printed size.
- [ ] Canvas matches the target venue's column or text width.

Hierarchy and ink
- [ ] Data has the highest contrast; axes, ticks, and any retained grid are thin and neutral.
- [ ] Cut list (section 0.5) applied: every non-data element survives the "remove it, lose information?" test.
- [ ] Gaps group panels along the intended axis.

Delivery
- [ ] Vector export with live text.
- [ ] Venue requirements checked after the design is final.
