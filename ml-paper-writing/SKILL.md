---
name: ml-paper-writing
description: Draft, revise, and review academic ML/AI papers for clarity, readable technical language, coherent paragraphs and sections, logical transitions, scoped claims, and a consistent skim path through abstracts, introductions, headings, and figures. Includes task-specific workflows for drafting from research evidence, citation verification, generated results, LaTeX layout, and submission preparation. Pair with figure-design for visual redesign.
license: MIT
metadata:
  author: Orchestra Research
  version: "3.0.0"
---

# ML paper writing

Make the scientific argument easy to follow: what question the paper answers,
what the evidence establishes, how each step follows, and why it matters.
Preserve scientific meaning, justified uncertainty, and the author's voice.
The core guidance is academic writing principles. Supporting workflows are
task-specific references, not mandatory steps for every prose revision.

## Read only what the writing task needs

Read [writing-guide.md](references/writing-guide.md) for drafting or prose
revision. For a full paper or multiple findings, also read
[narrative-structure.md](references/narrative-structure.md). Use
[manuscript-review.md](references/manuscript-review.md) to review the result.

Load a supporting workflow only when the task needs it:

| Task | Supporting reference |
|---|---|
| Draft from a research repository, experiment logs, or analysis outputs | [repo-to-manuscript.md](references/repo-to-manuscript.md) |
| Generate or refresh analysis-derived numbers and tables | [generated-results.md](references/generated-results.md) |
| Add references, write related work, or verify citation support | [citation-workflow.md](references/citation-workflow.md) |
| Edit LaTeX, change venue format, or inspect rendered layout | [latex-and-layout.md](references/latex-and-layout.md) |
| Prepare a submission or camera-ready package | [checklists.md](references/checklists.md) |

These references preserve existing project conventions and supplement, rather
than replace, the core principles. A prose-only edit does not require an export
pipeline, venue conversion, or submission audit.

Evidence is optional reading, not a prerequisite for ordinary editing:

- [Additional oral-paper readings](references/oral-readability-study.md): seven
  papers from 2023–2024, with terminology, skim paths, headings, figures, and
  connected-passage observations.
- [Original oral-paper study](references/oral-writing-study-2026.md): 25 papers,
  emphasizing section architecture, transitions, and contribution scope.
- [Sources](references/sources.md): evidence limits and author preferences.

## Core principles

Apply these across abstracts, main text, captions, tables, appendices, and
supplementary prose. Adapt their form to empirical, theory, resource, and
position papers; do not impose a fixed template.

1. **Make the central question and answer recoverable early.** Explain the
   concrete problem, relevant gap, approach, supported finding, and consequence.
   Do not hide the answer to create suspense or start with generic field history.
2. **Support skimming without replacing the argument.** The abstract stands
   alone; the introduction explains the reasoning and contribution; headings
   identify questions or supported findings; figures and captions expose the
   key comparisons. These layers must agree in terminology and scope. Useful
   repetition orients readers; repeated summaries must not crowd out explanation.
3. **Order sections by questions and prerequisites.** Establish a definition,
   measurement, assumption, or premise before a result depends on it. Keep
   shared setup together and analysis-specific setup beside its comparison.
4. **Give each paragraph one argumentative job.** State its point, develop the
   necessary evidence or reasoning, and end with what advances that point.
   A finding can span several paragraphs. Split when the purpose changes, not
   at a fixed sentence count. Do not put a heading over every paragraph.
5. **Make transitions logical, not decorative.** Within paragraphs, connect
   familiar context to new information and keep referents explicit. Between
   paragraphs, results, and sections, carry forward the established object or
   inference and name the dependency, contrast, unresolved question, or changed
   comparison axis. Parallel findings need not imply one another.
6. **Use technical vocabulary only when it earns its place.** Prefer a precise
   ordinary phrase to unnecessary jargon, acronyms, or coined labels. Explain
   indispensable unfamiliar terms before relying on them; define metrics and
   symbols at first substantive use. Use one name for one concept consistently,
   including headings and captions. Repetition is better than a misleading synonym.
7. **Explain formal machinery.** Give the purpose or intuition before an equation,
   definition, theorem, or algorithm and its scientific consequence afterward.
   Keep assumptions attached. An example supports understanding, not a proof or
   an untested generalization.
8. **Give figures distinct argumentative roles.** Order displays by the questions
   they answer. A conceptual overview, decisive comparison, explanation, and
   boundary test do different work. Merge redundant takeaways, not necessary
   controls or context. Preserve names, comparison order, and encodings across
   prose and displays; captions orient the reader, while text develops the inference.
9. **Use only as much hierarchy as navigation needs.** Add a heading for a
   substantial change of question, method component, or evidence role. Prefer a
   topic sentence for a short continuation. Avoid nested one-paragraph sections,
   repeated run-in labels, and headings that interrupt a connected finding.
10. **Be precise without defensive prose.** Distinguish observation, association,
    intervention, theorem, hypothesis, and illustration. Scope claims directly;
    preserve local qualifications that change their meaning. Develop broader
    restrictions in Limitations rather than ending every paragraph with a caveat.

## Scientific and editorial invariants

- Never invent results, procedures, citations, uncertainty, or novelty. Read the
  primary passage supporting a citation. Keep units, denominators, comparisons,
  and assumptions consistent across every account of a result.
- Keep scientific procedures self-contained. Remove internal paths, run names,
  configuration keys, code identifiers, release bookkeeping, and development
  history from manuscript prose, including appendices. Preserve necessary public
  model/dataset names, experimental settings, and required software citations.
- Prefer analysis-generated numerical macros and `.tex` tables for changeable
  results. Reconcile prose, captions, and tables against the same result source;
  refreshed values still require a fresh interpretation.
- Rewrite invented compounds and overloaded modifier stacks as clear phrases or
  clauses. Keep established technical spelling, official names, and grammatical
  hyphens that prevent ambiguity; do not merely remove punctuation.
- Preserve the author's effective cadence and level of formality. Do not force
  conversational documentation style, second person, universal active voice,
  vocabulary bans, or artificial variation onto academic prose.

## Text and visual design

This skill covers the argumentative role of figures and their relationship to
prose. For creating or redesigning displays, read the
[figure-design companion](../figure-design/SKILL.md). Keep the scientific question,
source evidence, comparison, units, uncertainty, and scope intact. Do not turn a
prose-only revision into an unsolicited graphics project.

Before delivery, apply the [review checks](references/manuscript-review.md) to
the requested scope. Fix the text rather than merely listing issues unless the
user asked for critique. Report specific unresolved evidence or unavailable
checks; do not manufacture completeness. Oral selection supplies examples,
not authority over these principles or proof of writing quality.
