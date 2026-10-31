# Clear, connected, readable ML writing

Apply the [core principles](../SKILL.md) across the manuscript. The decisions
below serve academic exposition, not a fixed paper template. For larger
arguments, use [narrative-structure.md](narrative-structure.md). Evidence comes
from the [original study](oral-writing-study-2026.md) and
[seven additional oral papers](oral-readability-study.md); exemplar habits are
not mandatory rules.

## Make the paper skimmable and worth reading closely

A skim should recover the central question, approach, supported answer, and
scope. A continuous reading should explain why the design and inferences follow.
Use the same scientific argument at different levels of detail:

| Surface | Reader's question | What belongs there |
|---|---|---|
| Abstract | What was asked, done, found, and established? | Standalone problem, approach, decisive evidence, conclusion, and indispensable scope |
| Introduction | Why this question and this approach? | Concrete gap, reason for the design, supported contributions, and their significance |
| Headings | Where is the question or evidence I need? | Specific topics, questions, or supported findings in the argument's order |
| Figures and captions | What is the comparison or relationship? | Understandable conditions, evidence, takeaway, and necessary measurement context |
| Paragraph openings | How does the argument develop? | A sequence of concrete points, not “we now discuss” announcements |

The introduction adds reasoning to the abstract, not just length. The body
establishes the claims rather than repeatedly advertising them. Repeat a main
finding where independent readers need it, but give each occurrence a role:
summary in the abstract, motivation and scope in the introduction, evidence and
interpretation in results, synthesis in the conclusion. Do not impose a fixed
sentence count, contribution-bullet count, or abstract formula.

For a skim check, read only the abstract, introduction, headings, figures, and
captions. Can the reader identify the same argument without mistaking a proposal
for a demonstrated benefit, a schematic for evidence, or a proxy for a construct?
Then read paragraph openings alone: do they expose a coherent progression, or
only a list of experiments? See [R4](oral-readability-study.md#r4) for question
reuse and [R7](oral-readability-study.md#r7) for a position-paper alternative.

## Use technical vocabulary only when it helps

Before introducing a label, ask whether the distinction recurs and whether an
established term already names it. A new acronym for a one-off operation adds
memory work without compressing the argument. Prefer “examples that identify
the target function” until a recurring technical distinction warrants a name.
Do not replace precise, familiar ML terminology with a longer vague paraphrase.

For indispensable unfamiliar language:

1. Explain the concept in ordinary words, using a small example when helpful.
2. Give its canonical name and the operational or mathematical definition the
   argument needs. Explain what a metric measures, not just its expanded acronym.
3. Reuse that name, spelling, and symbol consistently. Do not alternate “task,”
   “sample,” “response,” and “participant” when they denote different units.
4. Define it again briefly in a standalone abstract or caption if understanding
   would otherwise depend on an unseen passage. Do not copy a whole glossary.

Introduce formal detail when readers can understand its purpose. A notation
list can help lookup but does not replace a definition at first substantive use.
For a long manuscript, a private terminology list helps check headings,
captions, appendices, and the difference between a score and its target construct.
See the example-to-definition progression in [R5](oral-readability-study.md#r5).

## Connect sentences within a paragraph

Put familiar context where it connects to the previous sentence; place new
information where the next sentence can develop it. Keep the subject close to
its verb and make the actor or operation concrete. Prefer direct verbs over
nominalizations when meaning is unchanged. Passive voice is appropriate when
the experimental object is the topic and the actor adds nothing.

Name the referent when “this,” “it,” or “these results” could mean several things.
Preserve the comparison direction and the order of conditions. Use “therefore”
only for a supported consequence and “however” for an actual contrast; a
connective cannot supply a missing premise.

Invented example:

> Disconnected: “We measure overlap between selected units. The random baseline
> is low. This is reliable. We ablate units.”
>
> Connected: “The selected units overlap more across repeated samples than
> randomly selected units do. This consistency establishes stability of the
> selection, not its behavioral relevance. We therefore ablate the selected
> units to test whether they affect task accuracy.”

The revision distinguishes stability from relevance and explains the next test.
It is valid only if the stated comparison was made; do not add a control to
repair a sentence. For an equation sequence, use the same continuity: state the
obstacle, explain the transformation, then say what its output permits. See
[R3](oral-readability-study.md#r3).

## Give paragraphs distinct jobs without fragmenting a finding

Lead with the point or motivating question, then develop evidence or reasoning
and its meaning. Flexible patterns include finding → decisive comparison →
interpretation; purpose → procedure → design consequence; and intuition → formal
statement → scientific consequence. These are roles, not required sentence counts.

A single finding can need several paragraphs: establish the observation, test a
specific alternative, characterize variation, and synthesize. Keep the question
stable while making each paragraph's contribution distinct. Split an overloaded
paragraph when its purpose changes; combine short fragments that merely separate
setup, a statistic, and its obvious restatement. Do not make every sentence its
own paragraph or every paragraph its own subsection.

Put shared setup before dependent results and unique setup beside the affected
comparison. Define the population, condition, unit, grouping, weighting, and
quantity being estimated before interpreting it. Report the few numbers that
establish the pattern; leave exact secondary values in a display. Explain the
comparison rather than reading out every cell.

Invented example, assuming the controls isolate context access from response budget:

> Weak: “Table 2 shows 71% for B, 64% for C, and 79% for A. The results are
> promising. However, they may not generalize.”
>
> Revised: “Access to the additional context improves accuracy from 71% to 79%.
> Increasing the response budget without that context instead yields 64%.
> The contrast supports context access, rather than a longer response budget,
> as the explanation for the gain in this experiment.”

Keep metric, conditions, and uncertainty explicit in the actual paper; do not
claim that an apparent difference is negligible or causal without support.
End with the inference, example, or transition the argument needs. Delete a
closing sentence that merely repeats the opening or adds a ritual concession.

## Use headings for navigation, not paragraph decoration

Give a heading a substantial job: a new question, model component, theorem
stage, or evaluation axis that a reader may need to find. Make sibling headings
parallel in specificity and grammatical form. A finding heading is useful only
if the evidence supports its strength; retain conventional headings where they
already navigate well.

Prefer a topic sentence when the next paragraph develops the same question.
Merge one-paragraph subsections when their headings interrupt one finding.
Repeated bold run-in labels can fragment prose just as much as numbered headings.
A short subsection is justified when it is an independently useful destination,
not merely because every sibling needs the same shape. No heading quota follows
from these examples; several sampled papers themselves use dense local labels.

Open a substantial section with its purpose and reasoning. A roadmap can explain
why measurement precedes prediction or why a theorem needs another condition.
Do not add a roadmap to every short section or substitute subsection numbers
for the logic. Keep the actual paragraph transitions after headings are removed.

## Give each figure a distinct role in the argument

Privately state what each display adds: defines the problem, explains the method,
establishes the main comparison, tests an explanation, or examines a boundary.
These are possible roles, not a required figure sequence. Use the evidence the
paper has; do not invent an explanation or experiment to fill a slot.

Distinct roles do **not** require disjoint data. Reuse a baseline, task, or visual
context when readers need it to compare conditions. Remove or merge displays
that repeat the same inference without adding evidence or explanatory detail.
Separate panels that answer unrelated questions; keep panels together when their
comparison is the point. Match panel order to the prose and preserve names,
condition order, symbols, and encodings across the paper. See the different roles
of Figures 1–3 in [R5](oral-readability-study.md#r5) and the order mismatch in
[R7](oral-readability-study.md#r7).

A caption identifies the object or comparison, explains non-obvious units,
encodings, aggregation, and uncertainty, and states the supported takeaway.
Give enough local context to interpret the display without a search through the
body. Main text explains why the comparison matters and develops the inference;
it need not reproduce all values. A conceptual diagram illustrates a hypothesis
or mechanism; it is not a measurement establishing that mechanism.

For actual display design or redesign, use the
[figure-design companion](../../figure-design/SKILL.md). A table can preserve
exact values and an algorithm can expose procedure; neither must become a chart.

## Preserve precision while removing friction

- Scope assertions directly to their populations, comparisons, assumptions, and
  regimes. Keep a local qualification when it changes the interpretation; develop
  general restrictions in Limitations. Do not hide a confound there if it changes
  the main inference. Preserve null results and justified uncertainty.
- Distinguish percentage points from relative percentages, pooled estimates from
  equal-group averages, and standard deviation from standard error or confidence
  intervals. Avoid “significant” without a clear statistical or ordinary meaning.
- Keep quantities synchronized with the source analysis, preferably through
  generated numerical macros and `.tex` tables. A fresh number can still support
  a stale sentence; reconcile the interpretation too.
- Verify citations against the primary passage supporting the actual claim,
  including its assumptions and scope. Citation existence is not claim support.
- Describe scientific procedures, not internal repository bookkeeping. Remove
  paths, run identifiers, code names, and development history while retaining
  actual selection criteria, normalization, prompts, stopping rules, and settings.
- Rewrite overloaded compounds, not just their punctuation: “comparison with the
  same access to context” is clearer than “context-access-matched comparison.”
  Preserve conventional terms, official names, and disambiguating hyphens.
- Preserve effective voice and cadence. Cut empty transitions, generic openings,
  inflated novelty, and redundancy for a specific reader benefit, not because
  a word appears on a stylistic blacklist. Do not force short sentences when
  they sever the logical relation between clauses.

Keep review diagnostics out of the scientific narrative unless they explain
the result. For example, “On the evaluated arithmetic tasks, accuracy rises
from 71% to 79%” usually does not need “This does not establish general reasoning”
after it: the claim is already scoped. Report unavailable uncertainty honestly
in measurement/setup when material, and flag missing evidence in the delivery
note; do not append an audit-status sentence to every result. A planned analysis
can be introduced with future tense without repeatedly announcing that its
outcomes do not yet exist. Keep a local warning when the inference would
otherwise be misleading.

## Adapt to the scientific purpose

Methods and theory need motivation, assumptions, and the meaning of formal steps.
Results need a question, a decisive comparison, and an interpretation. Related
work should clarify differences in setting, assumptions, measurement, or approach,
not list miniature summaries of papers. Discussion and conclusion should explain
what the findings jointly establish, not merely repeat the largest scores.
Appendices carry supporting scientific detail, not an essential missing premise.

Preserve differences among paper types. A resource paper may establish coverage
and measurement validity; a theory paper may proceed through conditional results;
a position paper must separate evidence from hypothesis and implication.
Clarity does not require turning all three into the same empirical-method template.
