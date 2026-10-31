---
name: ml-paper-writing
description: Draft and revise ML/AI research manuscripts from code, experimental results, and existing prose. Use for textual narrative, section structure, logical transitions, scoped contributions, clear technical writing, verified citations, and conference submission preparation. Pair with figure-design when the user requests visual storytelling or a table/prose-to-figure redesign.
license: MIT
metadata:
  author: Orchestra Research
  version: "2.0.0"
---

# ML paper writing

Turn research evidence into a clear textual argument: what the work establishes,
how the evidence establishes it, and why the finding matters. Preserve the
author's voice and scientific meaning. Make the best supported draft within the
requested scope; flag consequential unknowns without making the user approve
each section.

## Start with the relevant references

Read [writing-guide.md](references/writing-guide.md) for every drafting or prose
revision task. It contains writing practices and concrete revision examples.
Then load only the references needed for the task:

| Task | Reference |
|---|---|
| Draft from a repository, results, or experiment notes | [repo-to-manuscript.md](references/repo-to-manuscript.md) |
| Structure sections, connect findings, or scope contributions | [narrative-structure.md](references/narrative-structure.md) |
| Inspect the 25-paper sample: five main-track orals per venue | [oral-writing-study-2026.md](references/oral-writing-study-2026.md); consult its manifest only when needed |
| Add or check citations | [citation-workflow.md](references/citation-workflow.md) |
| Report quantities from analysis or refresh numerical content | [generated-results.md](references/generated-results.md) |
| Compile LaTeX, change venue, or inspect layout | [latex-and-layout.md](references/latex-and-layout.md) |
| Prepare a submission | [checklists.md](references/checklists.md) |
| Respond to reviews or assess the argument | [reviewer-guidelines.md](references/reviewer-guidelines.md) |
| Trace advice to sources | [sources.md](references/sources.md) |

## Required writing rules

Apply these rules to the entire manuscript, including abstracts, captions,
tables, footnotes, appendices, and supplementary prose. They are acceptance
criteria, not optional polish. The review procedure is in
[manuscript-review.md](references/manuscript-review.md).

1. **Keep repository knowledge out of the manuscript.** Use code and artifacts
   to establish facts privately. Remove repository references, release files,
   internal paths, filenames, classes, functions, configuration keys, internal
   versions, run identifiers, development history, and implementation
   bookkeeping. Explain scientific procedures, assumptions, and design
   decisions in language that stands alone. Do not move this material into an
   appendix. Preserve scientifically necessary public model/dataset identities,
   mathematical details, and experimental settings; these differ from internal
   artifact names. A separately requested reproducibility package can contain
   operational instructions. Follow explicit venue requirements for availability
   or software citations without adding an unsolicited code tour.
2. **Define necessary terms early and use them consistently.** Prefer established,
   precise technical language. Explain a borrowed or coined concept in ordinary
   language before using it to reason about an experiment. Define symbols,
   metrics, populations, and acronyms at first substantive use. Keep a private
   terminology list and check headings, captions, and appendices against it.
3. **Rewrite unnecessary or unconventional hyphenated compounds.** Inspect every
   compound in new or revised prose. Prefer a direct phrase or a clause over an
   invented label or a stack of modifiers. Keep conventional technical spelling,
   official names, and hyphens that prevent a real ambiguity. Do not remove a
   hyphen mechanically if the resulting phrase is still awkward or misleading.
   Check rendered text as well as source.
4. **End paragraphs with what advances the argument.** A finding, interpretation,
   example, or necessary transition is usually sufficient. Do not routinely add
   a hedge, disclaimer, limitation list, or future-work sentence. Put general
   qualifications in Limitations. Keep a local qualification only when omitting
   it would materially change that claim's meaning; scope the claim itself or
   state the qualification once in shared setup. Preserve actual uncertainty,
   confounds, null results, and restrictions on causal inference.
5. **Keep every claim traceable to evidence.** Do not invent measurements,
   procedures, approvals, citations, uncertainty estimates, or novelty claims.
   Describe an association as an association and a conjecture as a conjecture.
   Never strengthen a claim merely to make the prose sound confident.
6. **Generate reported numbers and tables from analysis.** Prefer code-generated
   LaTeX macros for changeable numerical results and code-generated `.tex` tables
   over hand-copied values. Reuse the project's export workflow and one result
   source for prose, captions, appendices, and tables. Regenerate before delivery
   and verify that the surrounding claims still fit the refreshed values. Read
   [generated-results.md](references/generated-results.md) for the workflow.

These preferences take priority over stylistic habits found in exemplar papers.
Oral selection is a source of examples, not proof that a writing device is good.

## Work from evidence to argument

For full papers or sections containing multiple findings, also read
[narrative-structure.md](references/narrative-structure.md). Give each section a
scientific question, develop each finding through purposeful paragraphs, and
make the logical relation to the next finding explicit. Map contribution claims
to evidence and keep their setting and assumptions attached.

For a manuscript based on a codebase, follow
[repo-to-manuscript.md](references/repo-to-manuscript.md):

1. Read project instructions, the existing draft, experiment descriptions,
   result summaries, and the code that determines the reported quantities.
   Distinguish completed observations from intended experiments.
2. Build a private evidence map linking each proposed claim to its result,
   comparison, unit of analysis, aggregation, and scope. Keep artifact paths and
   other provenance in these working notes, outside the manuscript.
3. State the central finding in one sentence and order sections around the
   questions needed to establish it. For an existing draft, learn its voice from
   unmodified prose before editing. Use a provisional framing when evidence is
   clear; ask only about ambiguities that materially change the argument.
4. Draft the requested deliverable. Place shared setup before dependent results
   and analysis-specific setup beside the analysis. Write results as evidence
   and interpretation, rather than an inventory of experiments or table cells.
5. Verify citations against primary sources, regenerate numerical artifacts,
   reconcile numbers, and perform the required review below. Compile and inspect
   the PDF when the task changes a LaTeX manuscript and the toolchain is available.

If evidence is missing or contradictory, narrow the draft to what is supported
and identify the specific gap in working notes or the delivery message. Do not
fill the gap with plausible prose or label a partial draft submission ready.

## Review before delivery

Read [manuscript-review.md](references/manuscript-review.md) and complete its
passes before delivering manuscript text. Fix issues within scope; a list of
violations is not a substitute for revising the prose unless the user requested
review only.

- Trace headline claims and numbers back to the evidence map; regenerate numerical
  macros and `.tex` tables from the intended analysis inputs.
- Read each paragraph for a single purpose, sufficient evidence, and an ending
  that serves the argument. Check each transition within and across findings
  for an actual dependency, inference, contrast, or clearly named change of axis.
- Audit terminology, first-use definitions, and notation across the manuscript.
- Inspect all newly written compounds and all paragraph endings individually.
- Remove internal provenance and operational detail from every manuscript part.
- Check citations, cross-references, captions, and rendered layout when
  applicable. Report missing evidence or unavailable checks accurately.

Deliver the artifact and a short account of substantive changes and unresolved
scientific questions. Keep the audit and repository provenance out of the paper.

## Coordinate textual and visual narrative

This skill owns the textual narrative. The sibling
[figure-design skill](../figure-design/SKILL.md) owns the visual narrative.
When the user asks for a visual redesign, charts instead of a table, a summary
figure instead of long prose, or a clearer research story through figures,
invoke `figure-design` and read its instructions before designing the display.
If that relative link is unavailable, discover the installed skill by name;
do not assume another machine has the same absolute path.

Pass it the scientific question, intended takeaway, source data, comparison or
mechanism, units, denominators, weighting, uncertainty, and venue/figure slot.
Use charts for patterns and comparisons, tables when exact values matter, and
summary diagrams for relationships or processes. A redesign must preserve the
information needed to assess the claim. Do not invent data or force every table
into a chart. After visual changes, align the argument, captions, terminology,
and cross-references with the display without duplicating its values.

If a writing task would benefit from a visual, propose a specific conversion and
its purpose. Invoke the companion when prompted or when visual work is already
within the user's requested scope; do not turn a prose-only edit into a graphics
project.
