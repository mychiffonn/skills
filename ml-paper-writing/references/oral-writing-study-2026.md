# Writing practices from 25 main-track oral papers

This study examines **five papers each from ICML, ACL, EMNLP, NeurIPS, and ICLR
2026**. Its purpose is to improve textual narrative: section architecture,
logical transitions within and across findings, and scoped contribution claims.
The resulting drafting procedure is in [narrative-structure.md](narrative-structure.md).

## Sample and reading method

This is a purposive sample spanning theory, methods, benchmarks, and empirical
analysis. It is not random, representative of each venue, or a ranking of the
best writing. Existing cases were retained where they fit the revised scope;
additional cases brought each venue to five. A candidate without accessible
full text was replaced before analysis. Selection was not based on a writing
score. The [sample manifest](oral-writing-sample-2026.json) records all 25 paper
identities, oral selection sources, document versions, and passage locations.

For every paper, the reading examined its section sequence, contribution or
scope statements, and connected main-text passages that show both paragraph
progression within a finding and a transition to another finding or question.
The notes below describe rhetorical functions rather than summarize the research
idea. Selected rendered pages from all five venues were inspected to confirm
paragraph boundaries obscured by text extraction. This is a close reading of
specified argument passages, not a claim to have read every page or appendix.

Main-track oral eligibility was checked against the official
[ICML feed](https://icml.cc/static/virtual/data/icml-2026-orals-posters.json),
[ACL program](https://2026.aclweb.org/program/),
[EMNLP program](https://2026.emnlp.org/program/),
[NeurIPS feed](https://neurips.cc/static/virtual/data/neurips-2026-orals-posters.json),
and [ICLR feed](https://iclr.cc/static/virtual/data/iclr-2026-orals-posters.json).
Auxiliary tracks and spotlight-only records are excluded. The larger
[inventory](oral-papers-2026.csv) is a sampling aid; its unresolved NeurIPS census
gap does not affect the five verified sample identities. Counting details remain
in [oral-corpus-2026.json](oral-corpus-2026.json), outside the writing workflow.

ACL and EMNLP texts use Anthology PDFs. Where OpenReview access was blocked,
the other venues use matched author-submitted arXiv versions or an author's PDF.
Exact text sources are pinned in the manifest; these can differ from the
camera-ready version. Oral selection identifies the cohort, not a guarantee
that every wording choice in these versions is good.

## Practices to use when drafting

| Practice | What it does for the reader | Illustrative cases |
|---|---|---|
| Order sections by questions and prerequisites | Establish the measurement or object before an inference depends on it | A2, E3, E5 |
| Map each contribution to a result and its scope | Make the introduction's promises assessable in the body | M2, M5, I3 |
| Develop one finding across several purposeful paragraphs | Separate measurement, control, variation, and interpretation without fragmenting the claim | A2, N5, I1 |
| Connect an established result to a specific unresolved inference | Explain why the next analysis is necessary | E1, E5, M5 |
| Make a changed comparison axis explicit | Keep parallel findings clear without inventing a dependency | A3, I1, I4, I5 |
| Carry forward the previous output into the next design choice | Make a sequence of procedures form an argument | M2, I2, N1 |
| Turn an explanation into a testable prediction | Connect diagnosis to an intervention or stronger test | M3, A5, N4 |
| Attach conditions to the contribution itself | Preserve meaning without a disclaimer at every paragraph end | M2, N2, I3 |
| Distinguish kinds of evidence | Separate construct, proxy, association, intervention, illustration, and theorem | E1, E3, N2, I5 |
| Preserve the same comparison order and terminology | Reduce the reader's need to remap conditions between methods and results | N5, I4, E4 |

These are transferable editorial judgments supported by the cited passages,
not frequency estimates or evidence that a writing device causes acceptance.
The user's requirements on internal provenance, definitions, compounds, and
hedging take priority over contrary habits in an exemplar.

## ICML: five papers

<a id="m1"></a>

### M1. Benchmarking at the Edge of Comprehension

[Text examined](https://arxiv.org/pdf/2602.14307v4). Locations: Sections 2–7; PDF pp. 3–8.

- **Sections:** Motivation and design requirements precede a correctness criterion, protocol, ranking model, and two evaluation questions.
- **Within a finding:** The first results passage separates external agreement from prediction on unseen interactions, so two kinds of validation support one finding.
- **Across findings:** The second question changes from whether scores are useful to whether less capable adjudicators can supply reliable judgments. Stable question labels preserve that distinction.
- **Scope:** Treat the evaluated setting as evidence for bounded verification; a weaker-model proxy does not directly establish evaluation of genuinely superhuman systems.

<a id="m2"></a>

### M2. Mixtures Closest To A Given Measure: A Semidefinite Programming Approach

[Text examined](https://arxiv.org/pdf/2509.22879v2). Locations: Introduction; Sections 2–4; PDF pp. 2–7.

- **Sections:** The formal problem and common relaxation precede distance-specific results, an algorithm, and an illustrative application.
- **Within a finding:** A shared construction is explained before equations; each special case inherits it instead of restarting the exposition.
- **Across findings:** The algorithm opening takes a rank condition from the preceding theorems and explains what changes when it must be used numerically.
- **Scope:** The contribution specifies accessible moments and an admissible parameter family; distinguish asymptotic guarantees, conditional finite recovery, and preliminary application evidence.

<a id="m3"></a>

### M3. Are VLMs Seeing or Just Saying? Uncovering the Illusion of Visual Re-examination

[Text examined](https://arxiv.org/pdf/2605.15864v2). Locations: Introduction; Sections 4.2 and 5.1–5.3; PDF pp. 2, 4–6.

- **Sections:** A diagnostic intervention and its data precede the main failure, alternative explanations, and a proposed mechanism.
- **Within a finding:** Consecutive results paragraphs keep the same phenomenon while changing the comparison: overall failure, model variant, then scale.
- **Across findings:** The discussion first tests whether the replacement input is inherently harder, then contrasts independent capability with behavior during reasoning, before examining attention.
- **Scope:** Name the tested model families and intervention. Broad mechanism language in the exemplar still requires stronger support than an observed attention association alone.

<a id="m4"></a>

### M4. Learning Unmasking Policies for Diffusion Language Models

[Text examined](https://arxiv.org/pdf/2512.09106v4). Locations: Introduction; Sections 4.1–4.4; PDF pp. 1–2, 6–10.

- **Sections:** Define the decision problem, present a learned policy, then test the standard regime, a less restricted regime, transfer, and design choices.
- **Within a finding:** Setup identifies what remains fixed; the finding concerns an accuracy–efficiency tradeoff rather than an isolated best score.
- **Across findings:** The transfer section recalls a practical advantage of heuristics and asks whether learned policies retain it. The new question follows from an unresolved cost of the proposed approach.
- **Scope:** The underlying language model remains fixed. Claims must distinguish decoding regimes and the evaluated model, domain, and sequence-length transfers.

<a id="m5"></a>

### M5. Activation Oracles: Training and Evaluating LLMs as General-Purpose Activation Explainers

[Text examined](https://arxiv.org/pdf/2512.15674v2). Locations: Introduction; Sections 4–6; PDF pp. 2, 5–11.

- **Sections:** After downstream auditing evaluations, broaden the evaluation settings and then investigate which training choices explain the gains.
- **Within a finding:** The training-mixture finding states the overall trend, then describes exceptions and sensitivity rather than listing every result.
- **Across findings:** The next ablation names a confound introduced by adding datasets: quantity and diversity changed together. Holding quantity fixed motivates the next comparison.
- **Scope:** The contributions distinguish performance on the evaluated task suite from general capability and describe the controlled analysis as only partially separating the two factors.

## ACL: five papers

<a id="a1"></a>

### A1. No Reader Left Behind: Multi-Agent Summaries Everyone Can Understand

[Text examined](https://aclanthology.org/2026.acl-long.2.pdf). Locations: Introduction; Sections 3 and 5.1–5.5; PDF pp. 2–9.

- **Sections:** Map the accessibility problem to two method stages, then evaluate revision effects, components, feedback size, baselines, and human judgments.
- **Within a finding:** An aggregate revision pattern is followed by variation across models and a tradeoff across revision rounds; that tradeoff explains a concrete stopping choice.
- **Across findings:** After showing the whole system’s behavior, component comparisons ask what contributes to it. These are distinct evaluation questions, not a causal story supplied by section order.
- **Scope:** Keep the evaluated reader profiles, datasets, and measured outcomes explicit; the inclusive title does not itself establish accessibility for every reader.

<a id="a2"></a>

### A2. Different types of syntactic agreement recruit the same units within large language models

[Text examined](https://aclanthology.org/2026.acl-long.7.pdf). Locations: Introduction; Sections 4.1–4.3; PDF pp. 1–2, 3–7.

- **Sections:** Establish reliable and behaviorally relevant units before comparing units across phenomena and then across languages.
- **Within a finding:** The first finding proceeds from repeated-sample consistency to controls and ablation, distinguishing a stable measurement from evidence of functional relevance.
- **Across findings:** The next subsection explicitly carries forward those established properties before asking whether phenomena share units. A later opening changes only the language scope.
- **Scope:** Contributions name the studied phenomena, model set, and language comparisons. Evidence of overlap supports a narrower claim than a universal account of grammar.

<a id="a3"></a>

### A3. SenseRel: A Sense-Level Benchmark for Denotational and Connotational Meaning Relations

[Text examined](https://aclanthology.org/2026.acl-long.20.pdf). Locations: Introduction; Sections 2–5.3; PDF pp. 1–7.

- **Sections:** Define two conceptual axes before annotation and measurement; evaluate each axis before studying their relationship jointly.
- **Within a finding:** Within an axis, paragraphs change the comparison explicitly: evaluation setting, error pattern, or individual model. Interpretation follows the decisive comparison.
- **Across findings:** The two axis-specific findings are parallel, not premises that prove each other. Their outputs become inputs to the later joint analysis.
- **Scope:** Separate creation of a resource, evaluation on annotated pairs, and a larger exploratory application; each has a different evidence base and scope.

<a id="a4"></a>

### A4. How Memory Management Impacts LLM Agents: An Empirical Study of Experience-Following Behavior

[Text examined](https://aclanthology.org/2026.acl-long.27.pdf). Locations: Introduction; Sections 3–5; PDF pp. 1–2, 4–8.

- **Sections:** Organize around two memory operations, then examine their behavior under changed task distributions and resource constraints.
- **Within a finding:** A performance contrast motivates a behavioral property; the following explanation connects that property to a failure mode instead of appending a generic caveat.
- **Across findings:** An observed deletion benefit raises a new question about apparently acceptable records that still provide poor guidance. Challenging conditions then test a broader setting.
- **Scope:** State the studied agents and evolving retrieval setting. Distinguish the observed behavioral property, a proposed explanation, and the tested intervention.

<a id="a5"></a>

### A5. Accommodation and Epistemic Vigilance: A Pragmatic Account of Why LLMs Fail to Challenge Harmful Beliefs

[Text examined](https://aclanthology.org/2026.acl-long.736.pdf). Locations: Introduction; Sections 2, 4–6; PDF pp. 1–2, 6–9.

- **Sections:** Define borrowed pragmatic concepts, test contextual factors, test interventions predicted by that account, and discuss consequences for evaluation.
- **Within a finding:** The account leads to a prediction, while the intervention evaluation introduces a countermetric for inappropriate challenges before reporting gains.
- **Across findings:** The intervention section summarizes the diagnosed default and turns the explanation into a testable behavioral prediction.
- **Scope:** Describe the benchmark contexts and the countermetric. A useful account of these conditions is narrower than direct observation of a general psychological capacity.

## EMNLP: five papers

<a id="e1"></a>

### E1. Gold vs. Translation: Are We Measuring Language, Knowledge, or Locality in Translated Benchmarks?

[Text examined](https://aclanthology.org/2026.emnlp-main.32.pdf). Locations: Introduction; Sections 3–5.4; PDF pp. 1, 3–7.

- **Sections:** Comparison setup and measurement validation precede ranking agreement, incremental prediction, and robustness.
- **Within a finding:** The ranking result orders substantive patterns and local exceptions; it distinguishes a possible explanation from an identified mechanism.
- **Across findings:** The final ranking paragraph identifies what agreement cannot establish because general model strength could explain it. The next subsection tests the remaining predictive question.
- **Scope:** Name the benchmark pairings and target construct. Ranking agreement, incremental validity, and broad cultural coverage are different claims.

<a id="e2"></a>

### E2. When Does Auxiliary Classification Help Regression in Practice? A Case Study in Arabic Dialectness Modeling

[Text examined](https://aclanthology.org/2026.emnlp-main.30.pdf). Locations: Introduction; Sections 4.1–5; PDF pp. 1–2, 4–7.

- **Sections:** Follow a motivating failure with design comparisons, a controlled ablation, external comparisons, a transfer example, and error analysis.
- **Within a finding:** An unsuccessful initial comparison supplies a reason to inspect specific design factors; results are explained through those factors.
- **Across findings:** The controlled ablation explicitly asks whether architecture or tuning accounts for the gains. A later transfer changes the domain and names that scope change.
- **Scope:** Do not treat a sequence of refinements as isolated causal effects. Separate the controlled comparison from preliminary design exploration and from the single transfer setting.

<a id="e3"></a>

### E3. What Makes a Good Response? An Empirical Analysis of Quality in Qualitative Interviews

[Text examined](https://aclanthology.org/2026.emnlp-main.51.pdf). Locations: Introduction; Sections 2 and 4.1–4.3; PDF pp. 1–3, 5–7.

- **Sections:** Define a quality criterion and candidate measures, validate automated measurement, test prediction, then illustrate practical use.
- **Within a finding:** A validation passage explains the reference comparison and then states what the agreement permits the following analysis to do.
- **Across findings:** Measurement validity is a prerequisite for the prediction finding. The final case study changes purpose from explaining variation to illustrating how the measures might inform practice.
- **Scope:** Keep the operational criterion and sampled research projects explicit. Predictive associations do not establish that changing an interview technique causes better responses.

<a id="e4"></a>

### E4. Learning Diagnostic Clarifying Questions for Conversational Question Answering via Data-Efficient Dynamic Distillation

[Text examined](https://aclanthology.org/2026.emnlp-main.22.pdf). Locations: Introduction; Sections 3 and 4.1–4.5; PDF pp. 1–2, 3–8.

- **Sections:** Method components lead to questions about overall effectiveness, component contribution, process behavior, and transfer.
- **Within a finding:** The main result reports the comparison and then checks whether a larger interaction budget could explain it.
- **Across findings:** Component analysis asks what produced the overall effect; process analysis examines the intended behavior; the final question changes to an unseen distribution.
- **Scope:** Contributions specify ambiguous and unambiguous questions, evaluated backbones, and comparable interaction budgets; they do not establish a general dialogue capability.

<a id="e5"></a>

### E5. A Unified Mechanistic Analysis of Knowledge- and Safety-Based Refusals

[Text examined](https://aclanthology.org/2026.emnlp-main.1111.pdf). Locations: Introduction; Sections 3 and 4.1–4.4; PDF pp. 1–4, 6–8.

- **Sections:** A controlled comparison supports an ordered analysis of shared structure, transfer, localization, and behavioral intervention.
- **Within a finding:** The first finding decomposes one question into alternative-explanation checks, direct measurement, and separation of shared versus specific components.
- **Across findings:** Each opening states the previous inference and its remaining gap: shared direction does not imply interchangeability; transfer asymmetry does not locate a signal; geometry does not establish a behavioral consequence.
- **Scope:** Tie the contribution to controlled conditions and examined models. Distinguish representational association, transfer evidence, and intervention-based evidence.

## NeurIPS: five papers

<a id="n1"></a>

### N1. Bridging Compute- and Data-Optimal Pretraining

[Text examined](https://arxiv.org/pdf/2607.25271v1). Locations: Introduction; Sections 3–5; PDF pp. 1, 4–10.

- **Sections:** Define the quantities, characterize an empirical pattern, choose and validate a functional form, then derive allocation implications.
- **Within a finding:** Observed regularities become explicit requirements for the parametric family, making the equation answer the observations rather than appear without motivation.
- **Across findings:** After validating loss prediction, ask whether it predicts a downstream outcome. Only then move from a descriptive fit to its practical implications.
- **Scope:** State the expansion strategies and evaluated scales. Distinguish a fitted relationship, validation within the studied range, and implications conditional on that model.

<a id="n2"></a>

### N2. Impossibility of Distribution-Free Predictive Inference for Individual Treatment Effects

[Text examined](https://arxiv.org/pdf/2605.05051v1). Locations: Introduction; Sections 2.1–3; PDF pp. 1–4.

- **Sections:** Specify the inferential target and assumptions before an impossibility result, a restricted positive example, and a reassessment of prior methods.
- **Within a finding:** A theorem is followed by its ordinary-language consequence before the next formal development.
- **Across findings:** The positive example changes the assumptions explicitly. It answers what extra structure permits, rather than appearing to contradict the preceding impossibility result.
- **Scope:** State the covariate setting, validity requirement, and assumptions in the claim. Distinguish an illustrative positive case from broad applicability.

<a id="n3"></a>

### N3. CLIOPATRA: Extracting Private Information from LLM Insights

[Text examined](https://arxiv.org/pdf/2603.09781v3). Locations: Introduction; Sections 3.1 and 4.2–4.6; PDF pp. 1, 3, 8–11.

- **Sections:** Fix the adversary and procedure before testing feasibility, a stronger deployment constraint, factor sensitivity, another domain, and mitigations.
- **Within a finding:** The first evaluation checks an upstream prerequisite before interpreting downstream attack results; variants are compared at a stated common coverage.
- **Across findings:** A later evaluation introduces inspection as a new constraint, motivating a different variant and explicit setup changes. Domain extension and mitigation ask separate subsequent questions.
- **Scope:** Name the adversary’s knowledge, insertion budget, target attribute, and tested configuration. Limited observed success does not justify certainty about every future extracted attribute.

<a id="n4"></a>

### N4. Generative Modeling via Drifting

[Text examined](https://arxiv.org/pdf/2602.04770v2). Locations: Introduction; Sections 3 and 5.1–5.3; PDF pp. 1–4, 6–8.

- **Sections:** Present a distribution-level idea, derive its field and objective, explain a practical instantiation, and evaluate increasing application complexity.
- **Within a finding:** A derived field property motivates a destructive ablation: change that property, observe the effect, and connect it back to the construction.
- **Across findings:** Toy behavior supplies intuition before the image experiment. The control application is an additional domain test, not a consequence proved by the image results.
- **Scope:** Keep conceptual formulation, toy illustration, necessary mathematical conditions, and benchmark performance as distinct levels of evidence.

<a id="n5"></a>

### N5. Leaderboard Hacking: Preference-Based Model Evaluations are Vulnerable to Manipulation

[Text examined](https://www.efleisig.com/files/leaderboard-hacking.pdf). Locations: Introduction; Sections 3–6; PDF pp. 1, 3–9.

- **Sections:** Three intervention families appear in the same order in methods and results, followed by combination, heterogeneity, feasibility, and defenses.
- **Within a finding:** A finding moves from the overall effect to differences across target models and required resources, so the interpretation is more useful than the maximum effect alone.
- **Across findings:** Variation shared across the three results motivates an analysis of which targets are easier to move. Feasibility then changes the question from possible effects to deployment constraints.
- **Scope:** Keep evaluation on the specified preference data separate from a demonstrated compromise of a live service. State the manipulation budget and measured ranking outcome.

## ICLR: five papers

<a id="i1"></a>

### I1. GEPA: Reflective Prompt Evolution Can Outperform Reinforcement Learning

[Text examined](https://arxiv.org/pdf/2507.19457v2). Locations: Introduction; Sections 4–5; PDF pp. 2, 8–12.

- **Sections:** A bottleneck and an overlooked feedback source motivate the method; common evaluation setup supports several named observations and later applications.
- **Within a finding:** The first observation reports performance and then decomposes the rollout cost, explaining the comparison’s denominator.
- **Across findings:** Later observations change the comparator or the use of the same approach. They are parallel tests of usefulness, not automatic consequences of the first gain.
- **Scope:** Name the evaluated tasks, model access, comparator, and budget. Separate total evaluation cost from the subset of interactions used as learning feedback.

<a id="i2"></a>

### I2. OpenThoughts: Data Recipes for Reasoning Models

[Text examined](https://arxiv.org/pdf/2506.04178v2). Locations: Introduction; Sections 4.1–5; PDF pp. 2–3, 5–10.

- **Sections:** A common controlled protocol supports decisions at successive data-construction stages, followed by evaluation of the assembled pipeline at scale.
- **Within a finding:** Each stage contrasts alternatives under shared conditions and ends with the consequence for the next stage.
- **Across findings:** Selecting question sources creates the next unresolved choice of how to mix them; the resulting candidate pool creates the need for filtering. Later scale tests evaluate the assembled choices.
- **Scope:** Distinguish selection experiments from final evaluation. Claims about a chosen recipe remain tied to its backbones, domains, and scale.

<a id="i3"></a>

### I3. Scaling Laws and Spectra of Shallow Neural Networks in the Feature Learning Regime

[Text examined](https://arxiv.org/pdf/2509.24882v3). Locations: Introduction; Sections 2.1–2.4; PDF pp. 3, 5–10.

- **Sections:** Define a shared effective quantity, present risk behavior, characterize learned weights, and connect the two through an error decomposition.
- **Within a finding:** Formal statements are followed by interpretations of the regimes; a common quantity makes the two model families comparable.
- **Across findings:** The spectrum result is not left as a separate artifact: the next analysis explicitly connects spectral components to the previously established risk behavior.
- **Scope:** Attach model class, target assumptions, and asymptotic regime to the contribution. Preserve the distinction between formally justified regimes and extensions discussed through the analytical approximation.

<a id="i4"></a>

### I4. Latent Speech-Text Transformer

[Text examined](https://arxiv.org/pdf/2510.06195v2). Locations: Introduction; Sections 4–5.3; PDF pp. 1–2, 5–8.

- **Sections:** Describe representation and shared setup before fixed-budget comparisons, scaling, transfer tasks, and explanatory analyses.
- **Within a finding:** Parallel paragraphs name which resource is fixed and interpret the changed quantity, preventing two different fairness conditions from collapsing into one comparison.
- **Across findings:** Scaling and downstream tasks expand the evaluation axes after the main budget comparison. Their openings identify the new condition rather than merely adding another positive result.
- **Scope:** Identify the modeled interaction setting and resource control. A result under a fixed data budget is not automatically a result under fixed compute.

<a id="i5"></a>

### I5. Beyond Prompt-Induced Lies: Investigating LLM Deception on Benign Prompts

[Text examined](https://arxiv.org/pdf/2508.06361v4). Locations: Sections 3–5.4; PDF pp. 3–9.

- **Sections:** A borrowed conceptual definition is separated into two operational measures before the evaluation framework, individual-model results, and pooled analysis.
- **Within a finding:** Consecutive paragraphs distinguish change with difficulty, association between measures, and consistency within a model.
- **Across findings:** The pooled analysis changes the unit of comparison; an incentivized-prompt extension changes the experimental setting. Those changes need explicit setup rather than a generic connective.
- **Scope:** Treat the named psychological construct as operationalized by this controlled task. The paper itself notes an unobserved objective; measured scores do not directly reveal an internal intention.

## Apply the observations without copying a template

Use [narrative-structure.md](narrative-structure.md) to plan section purposes,
write connected finding blocks, and scope contributions. Preserve differences
between theory, empirical, and resource papers. Do not force every transition to
be a limitation, every result to be causal, or every section to follow the same
sentence count. An independent analysis can simply name its new question and
comparison axis.

The evidence does not justify venue-specific style rankings, universal section
lengths, or claims that oral status measures prose quality. No matched poster
control or reader-comprehension experiment was conducted. The rule prioritizing
code-generated numerical macros and `.tex` tables is an author requirement for
freshness, documented in [generated-results.md](generated-results.md); it is not
an inference about how these 25 papers were implemented.
