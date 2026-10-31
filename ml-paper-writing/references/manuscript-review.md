# Required manuscript review

Run these passes before delivering drafted or revised manuscript text. For a
small edit, inspect the changed passage and surrounding definitions and claims.
For a full draft, cover the entire manuscript, including captions, tables,
footnotes, appendices, and supplementary prose. A review-only request produces
findings and suggested revisions; an editing request requires fixes.

## 1. Reconcile claims and evidence

Map each stated contribution to a result section and its supporting evidence.
Keep the evaluated setting, assumptions, comparison, and kind of evidence
consistent across that map. Narrow unsupported promises.

Trace the abstract, introduction, section takeaways, captions, and conclusion
to the private evidence map. Check numbers, denominators, comparisons, units,
weighting, uncertainty, and scope. Separate observation, interpretation, and
speculation. Check that a changed sentence preserves the scientific claim.
Mark unresolved evidence gaps in working notes and disclose them at delivery.
Regenerate numerical macros and `.tex` tables from the intended analysis inputs
using [generated-results.md](generated-results.md). Check macro meaning as well
as value, and replace hand-copied results where generation is available. A fresh
export does not excuse a stale interpretation or an outdated caption.

## 2. Read the argument as continuous prose

State the purpose of each paragraph in a few words privately. Split paragraphs
that do unrelated jobs and remove paragraphs that add no evidence or reasoning.
Check that setup precedes dependent results and that an essential premise is
not hidden in an appendix. Compare revisions with the author's unmodified
prose for voice, terminology, and level of formality.

Read neighboring paragraph endings and openings together. Name the relation:
control, inference, explanation, changed condition, or parallel comparison.
Remove decorative connectives that conceal a missing relation. Check the
transition between findings separately: the next analysis must address a
specific unresolved question, use an established premise, test a prediction,
or explicitly change the comparison axis. Do not force every finding to end
with a caveat. See [narrative-structure.md](narrative-structure.md).

## 3. Check terminology and definitions

Inspect every necessary borrowed term, coined label, acronym, metric, and symbol
against the terminology list. Verify that the first substantive use has a
definition and that later uses keep the same meaning. Check standalone abstracts
and captions separately. Replace unnecessary new labels with ordinary technical
descriptions. Do not introduce a second name simply to avoid repetition.

## 4. Inspect every compound and paragraph ending

Collect every hyphenated compound in new or revised prose and examine it in
context. Keep established technical spellings, official names, and grammatical
hyphens that prevent ambiguity. Rewrite unconventional or unnecessary compounds
as clear phrases or clauses. Check rendered text because macros can hide labels
and TeX can insert line-break hyphens. A search for hyphens finds candidates;
it cannot decide which phrases are conventional.

Read all paragraph endings consecutively. For each hedge or concession, ask
whether omitting it changes the claim's truth or interpretation. If it does,
scope the claim or retain a precise local qualification. If it does not, remove
it or consolidate the material in Limitations. Check that a repeated disclaimer
has not replaced a useful scientific inference. Preserve necessary uncertainty.

## 5. Remove internal provenance

Inspect every manuscript part for repository references, paths, release files,
filenames, internal versions, run identifiers, configuration keys, class or
function names, implementation bookkeeping, and references to internal knowledge.
Translate scientifically relevant operations into self-contained method
descriptions. Remove incidental mechanics. Do not hide them in appendices.

Searches for path separators, file extensions, code formatting, run/version
labels, and words such as “script,” “release,” or “repository” help find
candidates. Inspect them semantically: a public dataset identifier, a cited
software package, or an algorithm that studies code can be necessary scientific
content. Internal artifact provenance is not. Keep required venue availability
information concise and separate from scientific exposition.

## 6. Verify citations and presentation

Apply [citation-workflow.md](citation-workflow.md) to added or changed references.
Check that every citation supports its associated claim, not merely that the
paper exists. Inspect undefined citations, broken cross-references, inconsistent
names, unsupported precision, and captions that repeat nearby prose.

For LaTeX edits, compile and inspect the PDF using
[latex-and-layout.md](latex-and-layout.md). A successful build does not establish
readable layout or compliance with venue rules. If the toolchain is missing,
report the checks that remain unavailable.

## Delivery criterion

Deliver revised text after fixing violations within the requested scope. Do not
describe a manuscript as ready if citations, claims, or mandatory checks remain
unresolved. Keep the review record and artifact paths outside the manuscript.
A short delivery note can identify substantive changes, unresolved scientific
questions, and checks that could not be completed.
