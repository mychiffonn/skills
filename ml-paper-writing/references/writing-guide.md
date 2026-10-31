# Writing practices for a clear research argument

Read this reference whenever drafting or revising prose. Apply the required
rules in [SKILL.md](../SKILL.md) across the entire manuscript. Use these practices
as decisions to make for the reader, rather than as a fixed paper template.
For section architecture, transitions within and across findings, and scoped
contributions, read [narrative-structure.md](narrative-structure.md) when drafting
full papers or sections with multiple findings. Source-specific observations
come from [25 main-track oral papers](oral-writing-study-2026.md), five per venue.

## Structure the reader's understanding

1. **State a concrete question or result early.** An opening identifies the
   actual problem, distinction, or finding. Remove background that could begin
   almost any paper. Give enough context to explain why this question matters;
   a contribution-first opening is useful but not obligatory.
2. **Make the gap explain the design.** Describe what existing evidence cannot
   distinguish, then explain how the proposed comparison addresses that gap.
   Avoid a generic “few studies have explored” sentence followed by an unrelated
   method inventory.
3. **Give each section a scientific purpose.** Order sections by the questions
   the argument must answer. Prefer a descriptive heading or precise question
   to “More results.” Open a substantial section with its main question and
   evidence, not a list of subsection numbers. Do not add roadmaps mechanically
   to short sections.
4. **Keep conceptual structure visible.** When an argument has two conditions,
   stages, or hypotheses, name them once and preserve that order across the
   introduction, methods, results, figures, and conclusion. Parallel structure
   reduces the amount readers must remember.

## Build paragraphs that do one job

A useful results paragraph moves from a finding or question to decisive evidence
and then interpretation. A methods paragraph moves from purpose to procedure
and then the consequence of a design choice. A theory paragraph moves from
intuition to formal statement and then its meaning. These are flexible shapes,
not mandatory sentence counts.

5. **Lead with the paragraph's point.** Give the reader a reason to process the
   details that follow. Split a paragraph when its scientific purpose changes.
   A topic sentence says something concrete, rather than announcing that results
   are “interesting” or “important.”
6. **Put setup beside the claim that depends on it.** Define the population,
   condition, grouping, weighting, and estimand before reporting that analysis.
   Keep shared setup in one place; do not make readers search a distant methods
   section for a detail unique to one comparison.
7. **Interpret the evidence instead of reading out the display.** Report the
   numbers that establish the pattern. Then explain what changes, persists, or
   differs across conditions and why it matters for the question. If an average
   conceals different behavior across groups, explain that difference directly.
8. **Give endings a purpose.** Finish with the inference, concrete example, or
   transition the argument needs. Delete a final sentence that merely repeats
   the topic sentence. Do not append a general concession to every paragraph.

An invented example of revising a results paragraph:

> Weak: “Table 2 shows 71% for A, 63% for B, and 64% for C. These results are
> promising. However, they may not generalize and do not prove causality.”
>
> Revised: “Condition A improves accuracy by 8 percentage points over B. The
> negligible difference between B and C indicates that the gain depends on
> access to the additional context, rather than the longer response budget.”

The revision is valid only if the experiment isolates those factors and the
evidence supports that interpretation. If it does not, narrow the inference.
Define the evaluation population and uncertainty in shared setup instead of
attaching the same generic caveat to every result.

## Make technical language precise

9. **Define terms before relying on them.** Explain a necessary borrowed or
   coined concept in ordinary language, then give its operational definition.
   Introduce acronyms after their expanded forms. Define what a metric measures,
   not just how its acronym expands. An abstract and a standalone caption must
   be understandable without definitions hidden later in the paper.
10. **Keep the same name for the same object.** Use a private terminology list.
    Do not alternate “sample,” “task,” “response,” and “participant” when they
    denote different units. Distinguish an observed score from a capability or
    construct it is intended to measure. Repetition is preferable to a synonym
    that changes the reader's interpretation.
11. **Make actors and operations concrete.** Prefer “Annotators score each
    response” to “Human labels carry the score,” and “We average task
    accuracies” to “We perform an aggregation of task-level performance.” Use
    active voice when it clarifies responsibility. Passive voice is useful when
    the experimental object is the topic and the actor is irrelevant.
12. **Use numbers to specify a claim.** Name the metric, baseline, denominator,
    and unit. Distinguish percentage points from relative percentages, pooled
    results from equal-group averages, and standard deviation from standard
    error or confidence intervals. Avoid “significant” unless its statistical
    meaning or intended ordinary meaning is clear. Do not invent uncertainty.
    Prefer [generated numerical macros and `.tex` tables](generated-results.md)
    for analysis-derived values, and regenerate them before delivery.

Keep the subject close to its verb. Put familiar context before new information
when that creates a natural connection to the preceding sentence. Use “this
comparison” or “this estimate” when a bare “this” has several possible referents.
Choose direct verbs over noun phrases. Do not replace an accurate verb such as
“combine” or “extend” merely to make a contribution sound more novel.

## Edit without flattening the author's voice

Make the minimum effective edit by default. Preserve strong, distinctive
sentences, the author's intended cadence, and meaningful variation in sentence
length. Restructure more deeply only when requested or when the argument is hard
to follow.

Treat patterns associated with generic or AI-sounding prose as signals to inspect,
not as banned words or constructions. Remove padding, empty transitions,
unsupported claims, and inflated language when they weaken the argument; retain
them when they express a precise idea or the author's natural voice. Do not add
artificial quirks to make prose sound human.

Apply general technical-documentation advice only when it serves the research
paper. Prefer clear actors and direct verbs when they improve precision, but
retain passive voice when the actor is unknown, irrelevant, or deliberately
de-emphasized. Do not force second person, conversational tone, or documentation
style onto scholarly prose.

Preserve scientific meaning, evidence, uncertainty, and qualifications throughout
editing. If a passage cannot be clarified without guessing, flag it instead of
inventing a claim or silently changing the author's position.

## Enforce the author's style preferences

### Remove implementation bookkeeping

The manuscript must stand alone for a reader who has never seen the repository.
Describe scientific procedures without file paths, release files, internal
versions, code identifiers, run names, development history, or references to
internal knowledge. This applies to appendices and captions too. Keep provenance
in private working notes. See [repo-to-manuscript.md](repo-to-manuscript.md) for
examples that preserve scientific detail while removing repository language.

### Rewrite awkward compounds

Inspect each compound in new or revised prose. Established terms such as
“out-of-distribution” may need their conventional spelling; an official model
name must remain accurate. For an improvised compound, prefer a direct phrase:

| Avoid | Prefer |
|---|---|
| language-review audit | audit of language use |
| error-type schema | categories of errors, or schema for error types |
| evidence-carrying subset | subset that supports the claim |
| context-access-matched comparison | comparison with the same access to context |
| model-developer-facing implication | implication for model developers |

Do not merely replace hyphens with spaces in an overloaded noun phrase. Rewrite
the relationship. Retain grammatical hyphens where their removal creates
ambiguity. Distinguish lexical hyphens from minus signs, number ranges, official
identifiers, and hyphens inserted by TeX at a line break.

### Scope the claim instead of repeatedly hedging

Generalizability concerns, untested settings, and broader restrictions belong in
Limitations unless a reader needs them immediately to interpret the result.
Preserve a local qualification when it separates association from causation,
identifies a material confound, limits a theorem, or prevents an unsupported
generalization. Prefer a precisely scoped statement to an observation followed
by a ritual disclaimer.

| Weak pattern | Better treatment |
|---|---|
| “The intervention works. However, we test only these models.” | “The intervention increases accuracy in the evaluated models.” Discuss untested model families in Limitations. |
| “The association may possibly suggest a potential relationship.” | State the measured association and its uncertainty directly. |
| Every paragraph ends “This does not establish causality.” | Define the observational design once, use associational language throughout, and retain a local warning only where a causal reading would otherwise be likely. |
| A confound is moved to Limitations even though it changes the main inference | Name the confound next to the affected inference and narrow the claim. |

Review paragraph endings together to catch a repeated concession pattern. Do
not remove scientific uncertainty to satisfy a stylistic preference.

## Adapt each manuscript part

**Abstract.** Make the question, approach, evidence, and main conclusion legible
without the body. A five-sentence sketch can help, but do not force a fixed
length. Include a decisive quantitative result when appropriate. Define any
indispensable unfamiliar concept briefly. Remove code-release announcements
unless explicitly required for the task or venue.

**Introduction.** Connect the question, gap, design, and finding. Make
contributions specific and supported. Use bullets only if they improve
navigation; neither a fixed bullet count nor a page number is a universal rule.
Explain the contrast with prior work fairly and precisely.

**Methods and theory.** Provide purpose and intuition before formal machinery.
Define notation, assumptions, experimental units, selection, and procedures.
State what a theorem establishes before elaborating its proof. Distinguish a
proved result from a heuristic argument. Introduce equations as sentences and
explain their terms rather than leaving the reader to decode them.

**Experiments and results.** Use the paragraph practices above. Name the claim
each experiment tests. Explain the decisive comparison and interpret the
result. Place analysis-specific setup just before the result. Reserve detailed
secondary values for a table or appendix.

**Related work.** Organize around distinctions needed to understand this work:
assumptions, setting, measurement, or mechanism. Cite sources for actual
relationships and claims. Avoid a sequence of miniature paper summaries or
citing a paper merely because a reviewer might have written it.

**Discussion, conclusion, and Limitations.** Synthesize what the evidence
establishes and why it matters. Keep the conclusion within the demonstrated
scope. Use Limitations to develop material restrictions and their consequences,
rather than repeating a disclaimer after each finding. Do not invent generic
limitations that have no bearing on the manuscript.

**Captions and appendices.** State context and takeaway without transcribing
visible values. Explain non-obvious units, weighting, uncertainty, and encodings.
Two sentences can be a useful caption budget, but clarity governs length.
Appendices contain scientific detail, not a code inventory. For a requested
visual redesign, use the [figure-design companion](../../figure-design/SKILL.md)
and retain a concise textual interpretation of the resulting figure.
