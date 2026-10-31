# From repository evidence to manuscript

Read this reference when drafting from a research repository, experiment logs,
analysis outputs, or a mixture of these sources. Code establishes what happened;
the manuscript explains the scientific procedure and its meaning.

## Understand the evidence

Read high-level project instructions and conventions before drilling into code.
Start with the existing manuscript and experiment summaries. Follow the code
that computes each reported metric, selects observations, applies exclusions,
or aggregates results. Existing citations and draft claims are leads to verify.

Resolve the distinctions that affect interpretation:

- Observed results versus plans, predictions, pilot runs, and obsolete analyses.
- Experimental conditions versus incidental execution differences.
- Raw observations versus independent experimental units.
- Pooled estimates versus averages that weight groups equally.
- Absolute changes versus relative changes and percentage points.
- Prespecified analysis versus exploratory analysis or selection after inspection.

Do not launch expensive experiments, reconstruct a missing result, or refactor
research code merely to complete a writing task. Identify missing evidence
and continue the supported parts of the draft.

## Build private working notes

Use a compact evidence map instead of loading large raw outputs into context.
For each substantive claim, record:

| Field | What to establish |
|---|---|
| Claim | The narrowest useful assertion supported by the evidence |
| Evidence | Exact source artifact and relevant analysis or calculation |
| Comparison | Conditions, baseline, controls, and selection procedure |
| Measurement | Metric definition, unit, denominator, and direction |
| Aggregation | Unit of analysis, grouping, weighting, and exclusions |
| Uncertainty | Estimator, resampling unit or runs, interval meaning |
| Scope | Population, assumptions, and restrictions on interpretation |
| Manuscript role | Main claim, supporting result, appendix detail, or omission |

These notes may contain file paths and run identifiers. They are private
provenance, not manuscript text. Reuse an existing evidence record if the project
has one. A persistent file is useful for a sustained drafting task, but is not
necessary for a small paragraph edit.

Maintain a terminology list alongside the evidence map. Record each necessary
term, its ordinary-language definition, first use, canonical spelling, and any
symbol or operational definition. Avoid creating a label when an ordinary phrase
will do.

## Translate implementation into scientific description

Describe what the procedure does to experimental units and why that choice
matters. Do not narrate how the repository stores or executes the procedure.
These are invented editing examples, not empirical results:

| Internal description | Manuscript description |
|---|---|
| “The release script loads the cleaned file and drops rows using the valid flag.” | “We exclude responses that fail the prespecified validity check.” Then define that check. |
| “The v3 aggregator computes macro_score from task_results.” | “We compute accuracy for each task and average the task accuracies with equal weight.” |
| “The reviewer class sends failed records to the fallback queue.” | “A second annotator evaluates responses that the first annotator cannot score.” |
| “The configuration enables a retry and caches the result.” | Explain retries only if they alter the measured procedure, selection, cost, or outcome; omit cache mechanics. |

Removing an internal name must not remove the actual selection criterion,
normalization, prompt, stopping rule, or other choice needed to understand the
study. Spell out that scientific choice instead. Public model or dataset names
identify experimental conditions and must remain accurate. Internal release
labels and artifact versions do not belong in the manuscript.

Appendices obey the same boundary. Use them for proofs, hyperparameters,
participant instructions, prompts, additional analyses, and other scientific
detail. Put commands, directory layouts, and installation steps in a separately
requested reproducibility package, subject to venue instructions. Do not silently
expand a writing task into creating such a package.

## Design the argument

Write a provisional one-sentence central finding and identify the evidence that
would let a skeptical reader assess it. A useful sequence is:

1. Establish the question and the distinction the paper tests.
2. Define experimental units and the shared procedure.
3. Present the decisive comparison.
4. Test the explanation or characterize where the pattern changes.
5. Explain what the combined evidence establishes.

Adapt this order to empirical, theoretical, resource, and position papers. Do
not impose fixed section counts or contribution bullets on a manuscript that
already communicates its argument well.

For a complete paper or multiple findings, follow
[narrative-structure.md](narrative-structure.md). Map contributions to evidence,
state the purpose of each finding, and identify why the next analysis follows.
Use a clear change of comparison axis for parallel findings rather than inventing
a dependency.

Keep indispensable assumptions and evidence in the main text. Move supporting
derivations and secondary analyses to the appendix. Select results for their
role in the argument, rather than including every available run.

## Draft and reconcile

Write methods and results closely enough together to detect mismatches. Separate
shared setup from setup specific to one analysis, and put the latter immediately
before the corresponding result. State the result, report the decisive evidence,
and explain its meaning. Follow the paragraph practices in
[writing-guide.md](writing-guide.md).

Use [generated-results.md](generated-results.md) to export reported quantities
as LaTeX macros and generate `.tex` tables from the same analysis outputs. Reuse
those macros throughout the manuscript rather than copying numbers by hand.
Regenerate numerical artifacts before reconciling the prose and compiling.

Draft the introduction and abstract against the evidence map, then reconcile
their strongest claims with the actual results. Check that the conclusion makes
no broader claim than the body supports. Do not manufacture completeness when
the task or available evidence supports only selected sections.

Before delivery, run the passes in [manuscript-review.md](manuscript-review.md).
