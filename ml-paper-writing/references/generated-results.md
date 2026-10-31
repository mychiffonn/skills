# Generate manuscript numbers and tables from analysis

Read this reference when a manuscript reports quantities derived from code,
experimental outputs, or analysis. Prefer a reproducible path from the finalized
analysis to LaTeX macros and `.tex` tables. Hand-copied results become stale when
the analysis changes, and editing one visible occurrence does not update others.

## Use one source for the reported quantities

Reuse the project's existing analysis outputs, exporters, build commands, and
formatting conventions. Identify the authoritative result set and its experimental
conditions before generating anything. The exporter must use the same filtering,
units, aggregation, weighting, uncertainty, and selection rules as the analysis.

Generate changeable reported quantities whenever they can be derived from code:
counts, dataset sizes, rates, estimates, uncertainty bounds, deltas, ratios,
statistical results, and measured costs. Do not calculate a headline difference
by hand from rounded table entries; calculate it from the underlying estimates
and then format it. Stable mathematical constants, citation years, and ordinary
section numbers do not need result macros.

Use descriptive, stable macro names that identify the quantity and its scope.
For distinct populations or conditions, use distinct names even when their
values happen to coincide. Follow the existing project's naming scheme. LaTeX
command names normally use letters; do not silently introduce digits or
underscores into a command name.

## Export macros and tables together

Use one lightweight export step to produce a macro file and the data-dependent
parts of tables from the same result set. Prefer generating a `tabular` fragment
that the manuscript includes inside a hand-authored float, so captions and the
scientific interpretation remain deliberate prose. Generate complete floats
when the project already does so. Keep labels, units, ordering, uncertainty,
precision, and semantic emphasis consistent with the scientific comparison.

The following values are invented solely to illustrate the source structure:

```latex
% generated/numbers.tex: emitted by the analysis exporter
\newcommand{\EvalTaskCount}{125}
\newcommand{\BaselineAccuracyPct}{71.3}
\newcommand{\ProposedAccuracyPct}{79.5}
\newcommand{\AccuracyGainPp}{8.2}
```

Load the macro definitions once, then use them in text, captions, and appendices:

```latex
% Preamble
\input{generated/numbers.tex}

% Body
Across \EvalTaskCount{} tasks, accuracy increases from
\BaselineAccuracyPct{}\% to \ProposedAccuracyPct{}\%,
a gain of \AccuracyGainPp{} percentage points.

\begin{table}[t]
  \centering
  \input{generated/accuracy-table.tex}
  \caption{Accuracy on the evaluated tasks.}
  \label{tab:accuracy}
\end{table}
```

Agree on whether a macro contains just a formatted number or also its unit.
The example uses numbers only and supplies the percent sign in the prose. Avoid
duplicated percent signs, lost units, and trailing-space errors. Braces after a
command preserve word boundaries. Use a shared formatter for prose macros and
table cells. Generated table cells may contain literal formatted values because
they are regenerated; do not hand-edit them as if they were the source data.

Keep scientific meaning in the manuscript: define the metric, population,
denominator, comparison, weighting, and uncertainty. Keep generator paths,
internal result identifiers, hashes, and run metadata in working notes or a
build manifest. Necessary `\input` paths in LaTeX source are build dependencies;
they must not appear as explanatory prose in the rendered manuscript.

## Make freshness part of the build

Regenerate numerical artifacts after a relevant analysis change and before
compiling a manuscript for review or delivery. Use the project's dependency graph
or build command so that changed inputs trigger the exporter. Generating text
from saved analysis outputs does not require rerunning training or expensive
experiments. Do not silently select a different run merely because its file is
newer.

For a project that checks generated files into version control, a useful check
is to regenerate into a temporary directory and compare the outputs with the
committed artifacts. Fail when their contents differ. Do not rely solely on
modification times: a newer file can still contain the wrong result set.
Record input identities privately when needed to establish which analysis was
exported. Keep generated content deterministic, including row order and rounding.

An exporter must fail on missing required results, duplicate quantity names,
invalid denominators, non-finite estimates, or an unexpected condition. Do not
turn missing values into zero, silently omit required rows, or emit a plausible
fallback. Escape LaTeX special characters in labels. Write complete outputs
before replacing the files used by the build so that a failure cannot leave a
mixture of old macros and new tables.

## Review the rendered claims as well as the values

Before delivery:

- Run the exporter from the intended finalized inputs and confirm success.
- Check that each macro denotes the population, condition, unit, and statistic
  intended by the surrounding sentence. A fresh value can support a stale claim.
- Check that deltas, ratios, percentages, confidence bounds, and significant
  digits agree across text, tables, captions, and appendices.
- Inspect new or revised prose for hand-entered experimental numbers that can
  use existing macros. Do not replace fixed mathematical constants mechanically.
- Check tables for omitted conditions, misleading ordering, stale highlighting,
  or captions that no longer match regenerated contents.
- Compile after regeneration and inspect the rendered numbers, symbols, units,
  table layout, and any sentence whose interpretation changed with the results.

If an exporter cannot run or its authoritative inputs are unavailable, identify
which values remain unverified. A successful LaTeX compilation does not prove
freshness. Do not hand-patch the generated `.tex` files to make the build pass;
fix the exporter or the source analysis. For a small prose-only task without
available analysis inputs, preserve existing macros and report the verification
limit instead of inventing a data pipeline.
