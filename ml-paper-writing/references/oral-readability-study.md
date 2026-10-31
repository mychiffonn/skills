# Readability practices from seven additional oral papers

This close reading extends [the original 25-paper study](oral-writing-study-2026.md).
It examines three NeurIPS 2023 orals, three ICLR 2024 orals, and one ICML 2024
**position-track** oral. The position paper is a separate rhetorical case, not
an addition to the original main-track cohort. No title overlaps that sample.
Official oral records and exact proceedings texts are linked below.

## Method and limits

Selection was purposive: these papers expose different explanatory problems—an
algorithmic shortcut, interpretable models, Bayesian inference, discrete tasks,
linked theoretical claims, a benchmark taxonomy, and a scientific hypothesis.
We examined abstracts, introductions, definitions, headings, connected main-text
passages, and figure captions at the stated locations. These are selected-passage
readings, not claims to have read every appendix or to rank the best prose.

Rendered proceedings pages were additionally inspected for the object-centric
paper (PDF pp. 2 and 4) and the position paper (pp. 1, 3, and 6), confirming
paragraph boundaries, visual hierarchy, and figure roles. Other figure-role
observations below are based on captions and extracted text; they do not certify
visual legibility. Proceedings versions, not later arXiv revisions, are the basis
for quotations and page locators.

Oral status establishes eligibility only. No poster control, readability score,
or comprehension experiment was used. Observations describe what a passage does;
principles are editorial judgments about what to retain. Broad claims, jargon,
figure density, and subheading frequency in an exemplar are not endorsements.

## What this adds to the existing guidance

| Existing emphasis | Additional principle | Evidence |
|---|---|---|
| Define necessary terms | Decide whether the label is needed at all; give an intuitive example before formal detail, then reuse one name | R2, R4–R7 |
| Match contributions to results | Make the abstract, introduction, headings, and figures a coherent skim path without turning the body into repeated summaries | R1, R3–R7 |
| Give sections a scientific purpose | Reserve headings for genuine changes of question; let related paragraphs develop the same finding | R1, R3, R4; density counterexamples below |
| Explain formal results | State the obstacle, introduce the operation that addresses it, and explain what the equation or theorem now permits | R3, R5 |
| Coordinate text and figures | Give each figure a distinct argumentative job; reuse context, not an identical takeaway | R1, R5–R7 |
| Preserve comparison order | Match term, condition, and panel order across prose and displays; a mismatch in a good exemplar is still a mismatch | R7 counterexample |
| Connect findings explicitly | Carry forward an established object, not just a connective; distinguish dependency, changed axis, and illustration | R1–R7 |

The distilled guidance is in [writing-guide.md](writing-guide.md) and
[narrative-structure.md](narrative-structure.md). The sample does not establish a
universal heading count, paragraph length, figure count, or section template.

## NeurIPS 2023

<a id="r1"></a>

### R1. Learning Transformer Programs

Dan Friedman, Alexander Wettig, and Danqi Chen.
[Official oral record](https://neurips.cc/virtual/2023/oral/73853).
[Proceedings PDF](https://proceedings.neurips.cc/paper_files/paper/2023/file/995f693b73050f90977ed2828202645c-Paper-Conference.pdf).
Read: abstract/introduction, pp. 1–2; background and Sections 3.1–3.2,
pp. 2–6; Sections 4.1–4.3 and discussion, pp. 6–10; Figures 1–4, 6–7.

- **Skim path:** The abstract's phrase “mechanistically interpretable by design”
  introduces a train-then-decompile approach. The introduction contrasts it with
  explaining an unconstrained model after training. Figure 1 supplies the workflow;
  later figures show internal structure, an executable program, and feature traces.
- **Definitions and progression:** Background explains circuits and the residual
  stream before Section 3 constrains information flow. The representation
  constraint precedes the attention modules that rely on it. A name acquires a
  concrete operational role, rather than serving as an unexplained slogan.
- **Paragraphs and headings:** Section 4.2 first distinguishes short-input success,
  exceptions, and longer-input degradation, then asks “What kinds of programs does
  the model learn?” The new question marks a real move from scores to a sorting
  example. Section 4.3 similarly separates NER performance from feature inspection.
- **Retain:** Connect aggregate evidence to an example that explains a different
  aspect of the result. Distinguish program mappability from simplicity or robustness.
- **Do not copy:** Frequent subheadings and task-dependent claims of parity with
  ordinary Transformers are not universal defaults. The body reports performance
  gaps and brittle solutions; the abstract must not erase those distinctions.

<a id="r2"></a>

### R2. Human-like Few-Shot Learning via Bayesian Reasoning over Natural Language

Kevin Ellis.
[Official oral record](https://neurips.cc/virtual/2023/oral/73840).
[Proceedings PDF](https://proceedings.neurips.cc/paper_files/paper/2023/file/2aa9b18b9ab37b0ab1fdaae46fb781d4-Paper-Conference.pdf).
Read: abstract/introduction, pp. 1–3; Section 3, pp. 3–4; Number Game,
pp. 4–6; Logical Concepts and discussion, pp. 6–10; Figures 1–6.

- **Skim path:** The opening examples make learning from few observations concrete.
  The phrase “expresses its concepts in natural language” (introduction, p. 2)
  gives the proposed representation before the machinery of Bayesian inference.
- **Definitions and progression:** The introduction explains induction and the
  distinction between a process model and a computational-level account. Section 3
  separates prior, likelihood, posterior, and proposal roles. When unavailable
  proposal probabilities prevent standard importance sampling, the replacement is
  described as heuristic beside that step, not hidden in a distant limitation.
- **Paragraphs and figures:** Results separate human-model fit, task accuracy, and
  explanatory cases. Figure 1 gives model structure; Figure 2 makes the Number Game
  and hypotheses concrete; Figure 3 examines fit and sampling budget; Figure 4
  explains the next task; Figures 5–6 give its evidence and cases.
- **Retain:** Use one concrete example to introduce an abstract distinction, then
  preserve the distinction through measurement and interpretation.
- **Do not copy:** Dense run-in labels and multi-purpose panels are not themselves
  readability devices. “Human-like” remains bounded by the studied symbolic tasks;
  behavioral fit and task accuracy are not interchangeable claims.

<a id="r3"></a>

### R3. Direct Preference Optimization: Your Language Model is Secretly a Reward Model

Rafael Rafailov, Archit Sharma, Eric Mitchell, Stefano Ermon,
Christopher D. Manning, and Chelsea Finn.
[Official oral record](https://neurips.cc/virtual/2023/oral/73865).
[Proceedings PDF](https://proceedings.neurips.cc/paper_files/paper/2023/file/a85b405ed65c6477a4fe8302b5e06ce7-Paper-Conference.pdf).
Read: abstract/introduction, pp. 1–2; Sections 3–5, pp. 3–6;
Section 6 and discussion, pp. 7–10; Figures 1–3 and Table 2.

- **Skim path:** Introduction examples distinguish knowing a behavior from producing
  it. Figure 1 contrasts the existing and proposed training processes. The method
  and experiment headings then identify derivation, interpretation, and evaluation.
- **Sentence-to-sentence logic:** Section 4 starts with the known objective, names
  the expensive partition function, rearranges the optimal-policy expression,
  and substitutes it into pairwise preferences, where “the partition function
  cancels” (p. 4). Each step uses the previous output. The next paragraph starts
  from the resulting preference probability to obtain the training objective.
- **Formal-to-verbal transition:** “What does the DPO update do?” (p. 5) changes
  from derivation to interpretation. The gradient's prose explains preferred and
  dispreferred responses and the example weight instead of merely restating symbols.
- **Figure roles:** Figure 1 is a process contrast; Figure 2 gives controlled
  reward–KL and summarization comparisons; Figure 3 gives dialogue and training
  behavior. Repeated method identities orient readers across different questions.
- **Retain:** Explain the bottleneck before the algebra and the consequence after it.
  In Section 6.1, explain why both reward and KL matter before interpreting the frontier.
- **Do not copy:** A multi-panel figure can mix questions and demand careful caption
  navigation. Strong abstract adjectives and a catchy title do not replace task,
  model, preference-model, or evaluator scope. GPT-4 judgments are proxy evidence.

## ICLR 2024

<a id="r4"></a>

### R4. Understanding In-Context Learning in Transformers and LLMs by Learning to Learn Discrete Functions

Satwik Bhattamishra, Arkil Patel, Phil Blunsom, and Varun Kanade.
[Official oral record](https://iclr.cc/virtual/2024/oral/19741).
[Proceedings PDF](https://proceedings.iclr.cc/paper_files/paper/2024/file/f7e7fabd73b3df96c54a320862afcb78-Paper-Conference.pdf).
Read: abstract/introduction, pp. 1–2; setup, pp. 2–4;
Sections 3–5 and conclusion, pp. 4–9; Figures 1–5.

- **Skim path:** The abstract groups its findings; the introduction names four
  motivating questions and contribution groups that return in the body. This is
  useful alignment, not evidence for a fixed number of questions or bullets.
- **Terminology:** “A teaching sequence is a sequence of examples that can uniquely
  identify the function” (p. 2) gives the ordinary-language meaning before formal
  treatment. The paper explains that “each sequence is a learning problem” (p. 3)
  before reasoning about learning an algorithm.
- **Across findings:** Section 3 separates capability and failure across function
  classes. Section 4 explicitly changes to informative examples, then compares
  ordinary and teaching-sequence training. A mixed-training test asks whether the
  learned behavior adapts to the example distribution. Section 5 returns to the
  introduction's question about pretrained LLMs and names its changed setup.
- **Figure roles:** Figure 1 explains the setting; Figures 2–3 test informative
  examples and adaptive behavior; Figures 4–5 address pretrained-model evaluation.
- **Retain:** Reuse question and task names so a skimmer can locate the evidence for
  each promise. Give a substantial finding several connected paragraphs.
- **Do not copy:** Dense local labels are not a reason to head every paragraph.
  Stylized Boolean-function evidence does not establish a universal LLM algorithm.

<a id="r5"></a>

### R5. Provable Compositional Generalization for Object-Centric Learning

Thaddäus Wiedemer, Jack Brady, Alexander Panfilov, Attila Juhos,
Matthias Bethge, and Wieland Brendel.
[Official oral record](https://iclr.cc/virtual/2024/oral/19788).
[Proceedings PDF](https://proceedings.iclr.cc/paper_files/paper/2024/file/57c89126d60c209f48d0e6395c766bb3-Paper-Conference.pdf).
Read: abstract/introduction and setup, pp. 1–4; Sections 3–4,
pp. 4–7; experiments/discussion, pp. 7–9; Figures 1–5.
Rendered PDF pp. 2 and 4 inspected.

- **Definitions:** Section 2 first explains unseen combinations of known objects
  with a red-square/blue-triangle example, then defines slots and the formal target.
  “This definition divides training an autoencoder that generalizes compositionally
  into two challenges” (p. 3) turns a definition into the section's organizing logic.
- **Linked argument:** Theorem 1 establishes identifiability on the observed subset.
  The next passage states the remaining generalization requirement. Section 3.1
  addresses decoder generalization; Section 3.2 starts from that result and explains
  why the encoder still need not invert it outside training support. The consistency
  condition addresses that gap; Section 3.3 combines the established conditions.
- **Figure roles:** Figure 1 introduces the problem and failure/repair distinction;
  Figure 2 maps the theoretical dependencies; Figure 3 explains the regularizer;
  Figure 4 tests the theory; Figure 5 examines assumptions in Slot Attention. Figures
  1–2 reuse the latent-space context but do different explanatory work.
- **Retain:** Plain-language meaning → formal definition → why the definition matters.
  A transition should say which part is established and which part remains, rather
  than adding a decorative “however.”
- **Do not copy:** The overview caption is dense, and the formal vocabulary is
  substantial. Do not import every definition into an abstract or caption. Guarantees
  depend on structural and optimization assumptions; synthetic non-occluding scenes
  do not establish general real-world performance.

<a id="r6"></a>

### R6. ExeDec: Execution Decomposition for Compositional Generalization in Neural Program Synthesis

Kensen Shi, Joey Hong, Yinlin Deng, Pengcheng Yin, Manzil Zaheer,
and Charles Sutton.
[Official oral record](https://iclr.cc/virtual/2024/oral/19726).
[Proceedings PDF](https://proceedings.iclr.cc/paper_files/paper/2024/file/c43b2989b1ba055aa713a4abbe4a8b05-Paper-Conference.pdf).
Read: abstract/introduction, pp. 1–2; Sections 2–4, pp. 2–6;
results/discussion, pp. 6–9; Figures 1–2, Algorithm 1, and Table 1.

- **Skim path:** Abstract and introduction link a measurable generalization target,
  benchmark, decomposition method, and evaluation. Section 2 makes each taxonomy
  item a concrete question with a train/test contrast and examples; “These five
  tasks can be grouped into three themes” (p. 3) compresses the taxonomy for recall.
- **Continuity:** The method preserves subgoal, synthesizer, execution, and updated
  specification through its stepwise explanation and Algorithm 1. Results distinguish
  the complete method from a no-subgoal ablation, then explicitly change to LLM
  prompting with its different evaluation constraints.
- **Distinct displays:** Figure 1 defines the benchmark taxonomy; Algorithm 1 supplies
  procedure; Figure 2 compares measured generalization; Table 1 reports the LLM
  setting. A table or algorithm can carry a narrative role without becoming a chart.
- **Retain:** Group a necessary taxonomy into meaningful distinctions, then carry
  those names into the comparisons. Use a small example to make the split operational.
- **Do not copy:** Do not introduce a taxonomy just to add labels. Results depend on
  the two program domains and available decompositions; LLM pretraining complicates
  interpretation of generalization. Human decomposition is motivation, not proof of
  human-like planning.

## ICML 2024 position track

<a id="r7"></a>

### R7. Position: The Platonic Representation Hypothesis

Minyoung Huh, Brian Cheung, Tongzhou Wang, and Phillip Isola.
[Official oral record](https://icml.cc/virtual/2024/oral/35559).
[Proceedings record](https://proceedings.mlr.press/v235/huh24a.html).
[Proceedings PDF](https://raw.githubusercontent.com/mlresearch/v235/main/assets/huh24a/huh24a.pdf).
Read: abstract/introduction and Sections 2–6, PDF pp. 1–9; Figures 1–6.
Rendered PDF pp. 1, 3, and 6 inspected.

- **Skim path:** The abstract distinguishes surveyed evidence, new measurements,
  hypothesis, possible explanations, and limitations. Main headings ask whether
  representations converge, why, toward what, and with what implications. Figure 1
  supplies the hypothesis; later figures address observations and proposed explanations.
- **Definitions:** Section 2 explains representations, kernels, and alignment in
  words before giving their mathematical forms. Section 2.3 names why cross-modal
  measurement needs paired inputs before defining the two kernels.
- **Across paragraphs and sections:** Section 2.1 distinguishes shared adoption of
  foundation models from alignment between different models: “it does not imply
  that different foundation models will arrive at the same representation” (p. 2).
  Section 4 changes from possible drivers to a candidate endpoint and explicitly
  marks its mathematical account as one candidate under modeling assumptions.
- **Figure roles:** Figure 1 conceptual hypothesis; Figure 2 within-vision alignment;
  Figure 3 cross-modal alignment; Figure 4 downstream association; Figure 5 possible
  drivers; Figure 6 a concrete color example. Shared language supports continuity,
  while the question changes. The diagrams are not empirical proof of a hypothesis.
- **Retain:** A hypothesis paper can be skimmable without contribution bullets.
  Separate observation, proposed explanation, idealized model, and implication.
- **Counterexample:** Figure 5 orders panels as task generality, simplicity bias,
  capacity, whereas Sections 3.1–3.3 order them as task generality, capacity,
  simplicity bias. Preserve a common order in a new manuscript instead of copying
  this mismatch. The metaphor and extra named hypotheses also show why memorable
  labels need precise definitions and should not proliferate without necessity.

## Principles deliberately not retained

No venue-specific style ranking, acceptance prediction, mandatory opening formula,
fixed sentence count, heading quota, figure quota, or universal experiment sequence.
No blanket ban on technical vocabulary, passive voice, or reuse of a control across
figures. No requirement that every result imply the next, every ending state a
limitation, or every figure be wholly disjoint in data. The useful constraint is
**distinct argumentative work with consistent terms, comparisons, and scope**.
