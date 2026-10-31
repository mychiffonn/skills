# LaTeX, templates, and layout review

Read this reference for LaTeX authoring, format conversion, or PDF review. Keep
formatting work subordinate to the argument and the venue's actual instructions.

## Choose the venue format

Preserve a project's working build and existing conventions. For a new paper,
verify the official format and author instructions for the target venue, year,
track, and submission stage. Use
[checklists.md](checklists.md) to find official venue sources; do not rely on
archived copies as evidence of current requirements.

Copy the complete required files from the official source, including style and
bibliography files, into an appropriate new manuscript directory. Avoid
overwriting an existing manuscript. Build the unmodified files to distinguish
environment problems from later edits.

For a venue conversion, start with the target format and migrate content,
figures, tables, and bibliography entries. Do not merge old preambles or retain
old conference headers. Adapt macros and packages only when needed. Preserve
valid self-citations and follow the venue's anonymization instructions.


## Build and inspect

Before compilation, regenerate analysis-derived macros and `.tex` tables using
[generated-results.md](generated-results.md). Preserve the dependency from the
intended analysis inputs through the exporter to the manuscript.

Use the project's prescribed build command. A common fallback is:

```bash
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

Replace `main.tex` with the actual entry file. Check the log for unresolved
citations, cross-references, missing files, and overfull boxes. A build failure
requires diagnosis, not a claim that the PDF was verified.

Inspect the rendered PDF after substantive edits. Review changed pages and their
neighbors because float placement can cascade; for a full manuscript revision,
review the main text and all affected supplementary pages. Confirm:

- Page limits and the actual start pages of excluded sections match current
  venue rules. Do not infer compliance from source length.
- Figures and tables appear near their first meaningful discussion and in
  reading order. Float moves do not leave large blank areas.
- Text, tables, equations, captions, and footnotes remain readable at final size.
- Nothing overlaps, clips, or spills into margins; captions stay with objects.
- Paragraphs avoid a lone final word in a column or an awkwardly short final
  line in full-width text when a natural rewrite can fix it.
- Rendered prose satisfies the terminology, compound, and paragraph-ending
  checks in [manuscript-review.md](manuscript-review.md).

Fix page pressure by removing redundancy, selecting evidence, and moving genuine
supporting detail. Do not change margins, shrink fonts, compress spacing against
venue rules, or make figures illegible to meet a limit. If the toolchain is
unavailable, report that compilation or visual inspection remains unverified.

## References, tables, and captions

Follow existing cross-reference conventions. Use `\Cref{}` when the template
supports it and the manuscript already follows that convention; use
`Appendix~\ref{}` where explicit appendix wording is desired. Do not add a
package merely to impose a preference.

Use `booktabs` where compatible, align comparable numbers, keep precision
consistent, and state metric direction. Explain boldface, shading, or other
semantic emphasis. Captions must identify the comparison, necessary units,
aggregation, uncertainty, and takeaway without repeating all visible values.
Refer to series by names as well as colors; never rely on color alone.

For visual design or converting a table or long passage into a figure, read the
[figure-design skill](../../figure-design/SKILL.md) when prompted. Let that skill
choose the display and encodings; keep this skill focused on the surrounding
textual narrative. Vector output is preferable for plots and diagrams, but use
a format appropriate to the actual image and the venue's requirements.
