# Build the paper's argument and transitions

Read this reference for a full manuscript, a section with multiple findings, or
a revision of argument structure. It translates the
[25-paper writing study](oral-writing-study-2026.md) into drafting decisions.
The examples below are invented illustrations of prose structure, not research
results. Adapt them to the evidence and the author's existing voice.

## Plan sections around questions and dependencies

Write a compact outline in private working notes. For each section or major
finding, identify its question, the premise or definition it needs, its decisive
evidence, its supported conclusion, and its role in the overall contribution.
Reuse the evidence map from [repo-to-manuscript.md](repo-to-manuscript.md).

Order the argument so that readers can evaluate each claim when they encounter
it. Useful structures include:

- Measurement definition and validation → substantive analysis → practical use.
  See [A2](oral-writing-study-2026.md#a2) and [E3](oral-writing-study-2026.md#e3).
- Main comparison → alternative explanation → discriminating test → boundary or
  transfer. See [M3](oral-writing-study-2026.md#m3) and [E5](oral-writing-study-2026.md#e5).
- Formal setting → result under stated assumptions → interpretation → changed
  assumptions or illustrative application. See [M2](oral-writing-study-2026.md#m2)
  and [N2](oral-writing-study-2026.md#n2).
- Common protocol → separate design questions → evaluation of the assembled
  choices. See [I2](oral-writing-study-2026.md#i2).

These are alternatives, not a mandatory sequence. Do not impose an experiment
chronology, a repository layout, or a list of available figures on the argument.
Keep shared setup before the analyses that use it; place unique setup beside
the relevant finding. Use a substantive heading, question, or supported finding
to identify what a section contributes.

Open a substantial section with its purpose and the logic of its analyses.
A useful roadmap explains why the order matters: establish a measurement,
answer the main question, then test an explanation or extend the setting.
Do not replace that explanation with a list of subsection numbers.

## Develop a finding across purposeful paragraphs

A finding can require several paragraphs. Preserve one scientific question while
giving each paragraph a distinct job: establish the observation, make a decisive
comparison, test an alternative, characterize variation, or interpret the result.
Do not compress all of those jobs into one overloaded paragraph or split them
into isolated statistics with no inference connecting them.

For example, an analysis of an apparent gain might proceed as follows:

1. State the observed gain and define the comparison sufficiently to assess it.
2. Compare with a control that distinguishes the proposed explanation from a
   specific alternative.
3. Describe meaningful variation across conditions and what that variation adds.
4. State the conclusion supported by the combined evidence.

Use only the roles the finding needs, in the order it needs them. Do not invent
a control or an explanation to complete this shape. Report the few numbers that
establish the pattern, using generated macros where available, and leave exact
secondary values in a table. Interpret the comparison instead of narrating cells.

When a result is unexpected, establish the expectation or reference first so
that the reader can understand the contrast. When a secondary analysis tests an
explanation, state the prediction that would distinguish that explanation from
an alternative before reporting the evidence.

## Connect neighboring paragraphs

Read the final sentence of one paragraph together with the first sentence of
the next. Identify the logical relation privately. A useful transition names a
known object or conclusion, then adds the new question, comparison, or inference.
Repeat the necessary term instead of using an ambiguous “this” or a new synonym.

| Relation | What the next paragraph does | Invented transition |
|---|---|---|
| Contextualize | Supply the reference needed to interpret an observation | “We compare this overlap with the overlap expected under random selection.” |
| Discriminate | Test a specific alternative explanation | “A larger response budget could also explain the gain. We therefore compare the systems at the same budget.” |
| Explain variation | Follow a pattern with the factor that may account for it | “The gain varies across tasks. We next test whether task length predicts that variation.” |
| Refine | Ask a stronger question than the first measure answers | “Agreement in rankings can arise from shared model strength. We test whether the score adds information after controlling for that strength.” |
| Use an output | Make the previous result an input to the next choice | “With the candidate sources fixed, the remaining choice is how to combine them.” |
| Change an axis | Introduce a parallel comparison honestly | “We next hold the data budget fixed and compare the compute required by each method.” |

“Moreover,” “however,” “therefore,” and “taken together” cannot supply a missing
relation. Use them only when the actual relation warrants them. Avoid adding a
transition sentence that merely repeats both paragraphs without advancing either.
The example transitions above are semantic patterns, not stock sentences to
paste into every paper.

## Connect findings without manufacturing a story

For each move to a new finding, make one of the following relations clear:

- **Dependency:** the first finding establishes a premise needed by the next.
- **Unresolved inference:** the first result leaves a specific question open,
  and the next comparison can answer it.
- **Mechanism or prediction:** an explanation of the first result predicts a
  new outcome that the next experiment tests.
- **Boundary:** a condition, assumption, population, or scale changes.
- **Parallel evidence:** another axis addresses the central question from a
  different direction, without depending logically on the first result.
- **Synthesis:** independently established findings jointly constrain a
  conclusion, at the strength the design supports.

For an unresolved inference, carry forward what is established, name what it
does not determine, and introduce the test that resolves that gap. The analysis
of shared structure → transfer → localization in
[E5](oral-writing-study-2026.md#e5) illustrates this progression. The qualification
is useful because it motivates a precise test; it is not a generic concession.

A parallel finding can simply name the new question and the axis being changed.
Do not imply that one positive result proves the next. Similarly, an application
in another domain provides additional evidence; it is not a universal guarantee.
See [I4](oral-writing-study-2026.md#i4) and [N4](oral-writing-study-2026.md#n4).

A finding can end with its conclusion. Put the transition at the start of the
next finding when that reads better. Do not make every ending a limitation,
open question, future-work sentence, or promise of another experiment. Preserve
local qualifications that change the inference; consolidate general limits in
Limitations, following [writing-guide.md](writing-guide.md).

## State contributions at the strength and scope of the evidence

For each contribution, identify the action or result, its scientific object,
the relevant setting or assumptions, and the evidence that supports it. A useful
private check is: “What exactly is established, for which objects, under which
conditions, and by which comparison or argument?”

| Contribution type | Scope that must stay attached |
|---|---|
| Method | The problem and interface it addresses; distinguish a proposed construction from demonstrated benefit |
| Empirical finding | The evaluated population, conditions, metric, comparator, and material resource control |
| Theoretical result | The object, assumptions, quantifiers, and finite-sample or asymptotic regime |
| Resource or measurement | The covered population, annotation or collection design, and evidence of validity |
| Mechanistic explanation | The distinction between representation, association, intervention, and identification of a cause |

Use a narrow, direct assertion instead of a sweeping claim followed by a hedge:

- Instead of “The method improves reasoning,” state that it improves the named
  measure on the evaluated tasks under the relevant resource constraint.
- Instead of “The two processes are the same,” distinguish shared measured
  structure from interchangeability or a common causal mechanism.
- For an impossibility result followed by a positive example, name the changed
  assumptions explicitly. The latter does not retract the former.
- For a construct borrowed from another field, define the operational measure
  early and keep its limits distinct from the broader construct.

Keep the claim grammatically readable. Important conditions belong near the
assertion or in clearly introduced shared setup, not in a long suffix of every
sentence. Repeat indispensable scope in an abstract, caption, or conclusion
that could otherwise be read as a broader standalone claim.

Use “prove” for what is proved under its assumptions, “estimate” for an estimate,
and “observe” or “find” for an empirical pattern. Preserve justified uncertainty;
confident wording does not turn a proxy into the construct or an association into
a cause. Do not use novelty verbs to hide a modest but accurate contribution.

## Reconcile the paper's promises with its findings

Map each introduction contribution to the section and evidence that establish
it. Check the abstract, result headings, captions, and conclusion against that
map. Remove or narrow a promise that has no supporting analysis. Keep the
methodological contribution and the empirical benefit separate when one is
established more strongly than the other.

In synthesis, explain what the findings jointly establish, which explanations
they distinguish, and what follows for the central question. Avoid a conclusion
that merely repeats the largest numbers or claims an untested generalization.
Regenerate reported macros and `.tex` tables before checking whether these
sentences still match the evidence; see [generated-results.md](generated-results.md).

Before delivery, perform the contribution-to-evidence and paragraph-transition
checks in [manuscript-review.md](manuscript-review.md).
