# Analytical Design

Use this reference for denser explanatory graphics, sparklines, and layered displays.

## Six Principles

1. Show comparisons and differences.
2. Show causality, mechanism, or explanation when relevant.
3. Keep multivariate structure visible instead of over-reducing it.
4. Integrate words, numbers, images, and diagrams in one composition. Default override: inside a figure, words are limited to axis labels, direct series labels, and panel letters. Titles, captions, and findings text stay out unless the user asks (`figure-design-practice.md` section 0.1).
5. Document the evidence with sources, scales, authorship, and provenance.
6. Treat content quality as the deciding factor.

## Sparklines

Use sparklines when a trend matters more than a precise reading.

- Keep them word-sized and inline with text or tables.
- Remove axes and nonessential labels.
- Use endpoints or a highlighted point when needed.
- Pair them with the current value or delta.

## Layering and Separation

Place multiple elements in the same space when they can be separated by weight, hue, or transparency.

- Let primary data carry the darkest weight.
- Push secondary data, grids, and notes into the background.
- Use color to separate overlapping or adjacent structures, not to decorate them.
- Check the graphic by squinting; the key information should still stand out.

## Micro and Macro

Design for both quick scanning and close reading.

- Macro view: overall pattern, trend, or structure.
- Micro view: exact values, exceptions, and labels.
- Use layering or compact annotation so both scales stay visible at once.

## Range-Frames and Dot-Dash Plots

Rework standard chart scaffolding when the default axis is not carrying its weight.

- Use a range-frame when the scale should stop at the observed data range instead of arbitrary outer limits.
- Use dot-dash or rug-like encodings when the marginal distribution matters.
- Make every axis element earn its space.

## Confections and Narrative Graphics

Use a confection when multiple visual elements must work together to explain one story.

- Combine maps, diagrams, and charts when each contributes evidence. Add explanatory prose only when the user asks; the visual encoding carries the message.
- Keep the pieces aligned to one argument.
- Use repeated structure for before/after or side-by-side comparison.

## Causality

Show mechanism, not just correlation.

- Put intervention and response in the same frame.
- Annotate the causal path directly on the display.
- Use small multiples over time when sequence clarifies mechanism.
- Add a process diagram when the causal story is otherwise invisible.

## Extended Checklist

- Does the display answer "compared to what?"
- Is the mechanism visible?
- Are multiple variables shown without over-simplifying the story?
- Are words, numbers, and graphics integrated?
- Is the evidence documented?
- Do primary elements dominate while secondary elements recede?
- Does the graphic reward both a glance and a careful read?
