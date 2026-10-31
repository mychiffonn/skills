# Submission preparation

Read this reference when preparing a submission or camera-ready version. Venue
rules vary by year, track, and stage. This file routes verification; it does not
freeze historical page limits or make every venue share one checklist.

## Verify the actual requirements

Consult the official instructions for the requested venue and year. Record the
source and relevant requirements in private working notes. Check the submission
system as well as the PDF instructions when a required form is separate.

These are starting points, not interchangeable policies:

| Venue | Official starting point | What to verify |
|---|---|---|
| ICML | [2026 author instructions](https://icml.cc/Conferences/2026/AuthorInstructions) | Track and stage, page budget, template, impact and reproducibility requirements |
| ICLR | [2026 author guide](https://iclr.cc/Conferences/2026/AuthorGuide) | Page budget, anonymous review, reproducibility, disclosure, supplementary material |
| ACL | [2026 main-paper call](https://2026.aclweb.org/calls/main_conference_papers/) and [ARR](https://aclrollingreview.org/) | Long/short track, Limitations, responsible NLP forms, commitment and disclosure rules |
| EMNLP | [2026 main-paper call](https://2026.emnlp.org/calls/main_conference_papers/) and [ARR](https://aclrollingreview.org/) | Long/short track, Limitations, responsible NLP forms, integrity and disclosure policies |
| NeurIPS | [Conference site](https://neurips.cc/) and [paper checklist guide](https://neurips.cc/public/guides/PaperChecklist) | Target year's call, checklist, page budget, template, ethics and disclosure rules |
| AAAI | [Conference site](https://aaai.org/conference/aaai/) | Target year's author kit, track, page budget, allowed packages and supplementary material |
| COLM | [Conference site](https://colmweb.org/) | Target year's call, template, page budget, disclosure and supplementary material |

Do not submit, upload, or certify declarations on the author's behalf merely
because a manuscript is being prepared. Do not claim approval, consent,
licensing, or artifact availability without evidence.

## Check the scientific report

- Headline claims match the evidence and are scoped to the evaluated setting.
- Experimental units, baselines, data splits, exclusions, metrics, aggregation,
  and selection procedures are explicit.
- Reported uncertainty names its calculation and unit of replication. Explain
  missing or inapplicable uncertainty instead of inventing error bars.
- Relevant hyperparameters, selection criteria, prompts, compute, assumptions,
  and proofs are documented at the level the study needs.
- Material limitations and consequences are developed in Limitations. Necessary
  local qualifications remain beside the affected claims without repeated
  paragraph-ending disclaimers.
- Citations and bibliography metadata are verified against primary sources.
- Applicable human-participant, data, license, and ethics information reflects
  the actual study and the venue's requirements.

## Check the manuscript and submission package

Follow [manuscript-review.md](manuscript-review.md) for the required language and
argument review. Then follow [latex-and-layout.md](latex-and-layout.md) to verify
rendered pages, cross-references, citations, readability, and page limits.

Check anonymity and required sections against the specific venue instructions.
Do not remove legitimate self-citations indiscriminately. Keep internal artifact
provenance out of manuscript prose and appendices. Put operational commands and
environment details in a separately requested code package when appropriate;
include only the availability, software identification, or reproducibility
information explicitly needed by the venue and study.

Report remaining evidence gaps, unresolved citations, and unavailable checks.
A clean build alone does not justify calling the manuscript submission ready.
