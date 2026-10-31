# Venue Figure Sizes

Use this reference to size a figure for its target venue before plotting. Create the figure at final printed size. Never create it large and shrink it, because text and line weights shrink with it.

## Procedure

1. Identify the venue and year. Templates change; confirm against the current style file.
2. Pick the slot: one column, or full text width (spanning both columns in two-column templates).
3. Set the figure canvas to that width in inches (`figsize=(width_in, height_in)` in Matplotlib) and export without `bbox_inches="tight"` cropping that changes the width.
4. Set font sizes in points for the final size, not relative to the canvas. See "Text and line floors" below.
5. Include the figure at `width=\columnwidth` (or `\textwidth` for `figure*`) with no scaling.
6. Proof at 100% zoom in the compiled PDF, then at grayscale.

Measure the template instead of trusting a table when the venue or year is uncertain. Put this in the preamble and read the log:

```latex
\typeout{columnwidth=\the\columnwidth textwidth=\the\textwidth columnsep=\the\columnsep}
```

Convert: `inches = pt / 72.27` for TeX points.

## Widths (Verified from Style Files and Author Guides)

| Venue | One column | Full text width | Source |
| --- | --- | --- | --- |
| NeurIPS | single column layout; use 5.5 in | 5.5 in | NeurIPS formatting instructions ("5.5 inches (33 picas) wide") |
| ICLR | single column layout; use 5.5 in | 5.5 in | `iclr2025_conference.sty`: `\textwidth 5.5 true in` |
| ICML | 3.25 in | 6.75 in | ICML example paper ("overall width of 6.75 inches ... 0.25 inches between the columns") |
| CVPR / ICCV | about 3.28 in | 6.875 in | `cvpr.sty`: `\textwidth` 6.875 in, `\columnsep` 0.3125 in; column = (6.875 - 0.3125) / 2 |
| AAAI (2026) | about 3.31 in | 7.0 in | `aaai2026.sty`: `\textwidth` 7.0 in, `\columnsep` 0.375 in |
| ACL / EMNLP / NAACL (`*ACL`) | 7.7 cm (about 3.03 in) | 16.0 cm (about 6.30 in) | ACL `formatting.md`: A4, 2.5 cm margins, column 7.7 cm, gap 0.6 cm |
| Nature | 89 mm | 183 mm | Nature research figure guide; max height 170 mm |
| Science Advances | 3.55 in (9 cm) | 7.25 in (18.4 cm) | Science Advances "Guide to Preparing Figures" |

Notes:
- NeurIPS and ICLR are single-column. A "full width" figure is the whole 5.5 in text block; there is no narrower slot except half-width side-by-side panels (about 2.6 in each with a gap).
- Venues not in the table (ACM `sigconf`, IEEE, workshops, theses, slides): measure with the snippet above. Do not guess.
- Workshop templates often reuse the parent conference style but may change margins. Measure.

## Choosing One Column vs. Full Width

| Figure content | Slot |
| --- | --- |
| One simple chart, 1 to 3 series, short labels | One column (two-column venues) |
| Small multiples of 3 or more panels, or long category labels | Full width |
| Heatmaps with many labeled rows/columns, Sankey, network, teaser/overview | Full width |
| Single-column venues (NeurIPS, ICLR) | Full width; panel count sets height |

Rules of thumb:
- Panels in one row: width per panel = (slot width - gaps) / n. If panel width falls under about 1.6 in, move to two rows or cut panels (one idea per plot).
- Default aspect ratio: 4:3 to 16:10 for single panels (height about 0.65 to 0.75 of width). Use wider for time series with long x ranges; use square for scatter plots where both axes share units, and for heatmaps of square matrices.
- Cap height at about 0.4 of the text block height (about 3.5 in on a 9 in block) so figures do not force page-length gaps. Nature's cap is 170 mm.
- Keep gaps between panels small and equal (see perceptual grouping in `figure-design-practice.md`).

## Text and Line Floors (at Final Printed Size)

Conference body text is typically 10 pt. Figure text should be near body size, never far below.

| Element | Floor | Target |
| --- | --- | --- |
| Axis labels, series labels, legends | 7 pt | 8 to 9 pt |
| Tick labels | 6 pt | 7 to 8 pt |
| Panel labels (a, b, c) | 8 pt bold | 9 pt bold |
| Annotation text | 6 pt | 7 pt |
| Lines (data) | 1.0 pt | 1.5 to 2 pt |
| Axes, ticks | 0.5 pt | 0.6 to 0.8 pt |
| Marker size | 3 pt | 4 to 6 pt |

The Nature requirement is concrete: all text 5 to 7 pt at printed size. For conference papers the 6 to 9 pt targets are this skill's recommendation, not a venue rule. Choose the larger value when space allows.

- Check legibility with the PDF at 100% zoom on a laptop and when printed or shown at 50%.
- Use the same fonts and sizes in every figure of the paper so text does not change scale between figures.

## Slides and Posters

- Not covered by the style files above. Size to the slide or poster grid and set text far larger: at least 18 pt on slides, at least 24 pt on posters.
- Cut series and panels further; one message per slide figure.

## Export

- Vector PDF/SVG with text as text, fonts embedded. Nature rejects JPEG, TIFF and PNG for main figures.
- Export at final size; set `savefig.dpi` to at least 300 only for raster content (images, very large point clouds).
- In Matplotlib set `pdf.fonttype` to 42 so fonts stay editable and embed correctly.
