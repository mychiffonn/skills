# Tufte Principles

Use this reference when judging whether a visualization is clear, honest, and information-dense.

## Core Tests

- Show the data plainly.
- Favor substance over decoration.
- Preserve truthful proportions and baselines.
- Let viewers compare values quickly.
- Reveal several levels of detail in the same display.
- Provide the context needed to evaluate the data.

## Graphical Integrity

- Keep visual effect proportional to data effect.
- Use precise labels, scales, and baselines.
- Do not distort with 3D, truncated axes, inconsistent intervals, or area/volume encodings for linear quantities.
- Do not quote data out of context.

### Lie Factor

Use this as a distortion check:

`Lie Factor = visual effect / data effect`

- Near `1.0`: faithful.
- Far above or below `1.0`: likely distortion.

## Data-Ink Ratio

Prefer ink that carries information.

- Remove decoration, heavy borders, redundant labels, and excessive ticks.
- Remove ink that can be erased without losing information.
- Iterate until only useful structure remains.

## Chartjunk

Treat chartjunk as any interior decoration that does not carry data.

- Avoid visual noise and moiré patterns.
- Omit grids by default; keep one light axis of gridlines only if exact values must be read (see `figure-design-practice.md` section 0.5).
- Do not add self-advertising design flourishes.
- Do not use clip art, icons, or effects unless they encode information.

## Small Multiples

Use repeated panels when the main task is comparison.

- Keep the design identical across panels.
- Keep scales consistent.
- Minimize spacing and decoration.
- Make the variable that changes obvious.

## Quick Checklist

- Does the graphic show the data clearly?
- Can the viewer compare values quickly?
- Does the design avoid distortion?
- Can anything be removed without losing information?
- Is the context sufficient to judge the evidence?
