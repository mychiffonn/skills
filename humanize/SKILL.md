---
name: humanize
description: Edit or rewrite prose so it sounds clear, direct, cohesive, specific, and recognizably human while preserving the writer's meaning and personal voice. Use when writing feels AI-generated, padded, vague, over-polished, repetitive, jargon-heavy, incoherent, difficult to follow, or full of meta-commentary; when the user asks to humanize, simplify, tighten, or sharpen a draft; when repeated titles, summaries, cards, or notifications are hard to scan; or when the user wants AI-slop patterns flagged without rewriting.
---

# Humanize

Edit like a sharp, respectful human editor. Restore clear meaning, logical structure, and the writer's real voice. Do not add artificial quirks or replace one generic style with another.

## Choose the job and protect the draft

Use the mode requested by the user:

- **Edit:** Make the minimum effective changes. Use this by default.
- **Deep rewrite:** Restructure or substantially shorten the draft when requested or when local edits cannot repair the argument.
- **Detect:** Flag problems without rewriting the full draft. Do not score the writing, assign an AI probability, or guess authorship.

If the text is not supplied or available in the specified file, ask for it. Ask about audience, format, or intended outcome only when the answer would materially change the edit. Otherwise, make a reasonable assumption and proceed.

Read the full draft before editing. Identify its main point, audience, and what the reader needs to understand, believe, feel, or do. If the main point is unclear, flag it or ask; do not invent one.

Preserve the writer's position, facts, qualifications, and intent. Notice the draft's vocabulary, cadence, bluntness, humor, uncertainty, technical depth, digressions, and level of polish. Leave strong, distinctive sentences alone. Keep intentional humor, profanity, fragments, repetition, and asides.

Keep “I think,” “maybe,” and “honestly” when they convey real uncertainty, emphasis, or spoken rhythm. Remove them only when they delay the point without adding meaning. A rough draft with a real voice must still sound like the same person after editing.

Do not invent claims, examples, statistics, quotations, sources, mechanisms, or opinions. Preserve required product names, quotations, citations, code, identifiers, and established technical terms. If a passage cannot be clarified without guessing, flag it.

## Edit in reading order

Work from the document's purpose to its structure, paragraphs, sentences, and surface details. Do not polish sentences before understanding the argument. In detect mode, use the same sequence to diagnose problems rather than rewriting the draft.

### 1. Make the document's structure visible

Put the central point early enough for the genre. In explanatory or argumentative prose, usually state it in the opening paragraph. Keep delayed disclosure when narrative, suspense, or necessary context genuinely calls for it.

Use topic sentences to make paragraphs' purposes clear and descriptive headings to identify subjects, claims, or findings. Do not force headings into short pieces or add one above every tiny paragraph. Replace generic headings such as “Introduction,” “The headline finding,” or “Why it matters” when a more specific heading helps navigation; otherwise, remove them.

Order material so each part prepares for or advances the next. Keep the existing progression and useful detours when they work. Reorganize when requested or when the order obscures the point, and disclose material restructuring in the final response.

Use numbered or bulleted lists only when the user requests or permits them. An existing list permits preserving that list, not converting unrelated prose into more lists. When lists are permitted, number sequences, rankings, procedures, or items referenced later; use bullets for unordered parallel items. Keep connected reasoning in prose. Lists cannot repair a weak argument.

### 2. Connect paragraphs and sentences

Give each paragraph a clear purpose. Every sentence must develop, support, qualify, illustrate, or transition from that purpose.

Check that a reader can explain:

- Why sentence B follows sentence A.
- What each sentence contributes to its paragraph.
- What each paragraph contributes to the main point.
- Why one paragraph leads to the next.

If the relationship is unclear, reorder, combine, split, clarify, or remove the material. Add transitions only when they name a real relationship, such as cause, contrast, sequence, qualification, or evidence. Words such as “therefore,” “however,” and “moreover” cannot supply missing logic.

Avoid abrupt topic changes. Signal a genuine change of subject or start a new section. Where useful, begin with information the reader already knows and then introduce the new point; make references such as “this” and “it” unambiguous.

### 3. Make sentences easy to parse

Make clear who did what, to whom, and with what result. Prefer a straightforward subject–verb–object order when it helps the reader understand the sentence on the first pass. Keep the subject and its main verb close; move long interruptions or qualifications when they obscure the action.

For example, “The agent fixed the login bug” makes the actor and action clearer than “Login bug fixed by the agent.” Treat this as a practical default, not a universal rule about how people read. Keep passive voice when the actor is unknown, irrelevant, obvious, or intentionally deemphasized.

Use direct verbs: “decided” instead of “made a decision,” “can” instead of “has the ability to,” and “tracks sponsors” instead of “serves as a sponsor-management hub.” Prefer familiar words when they carry the same meaning.

Replace abstractions with concrete facts supported by the draft. Preserve useful names, dates, numbers, mechanisms, and examples. Do not turn a specific fact into a generic claim about importance or improvement.

Define, unpack, replace, or flag unexplained jargon and abbreviations. Keep specialized terms when they are precise and appropriate for the audience. Use the same term for the same concept rather than cycling through synonyms for variety.

Translate internal language about permissions, sessions, workflows, or database states into what happened, what it means for the reader, whether they must act, and what they can do next. Do not add an action that the draft does not support.

Remove vague trust labels such as “secure,” “verified,” “protected,” or “privacy-first” unless the draft explains a specific, accurate protection that helps the reader decide what to do.

Keep one main idea per sentence when possible. Split sentences whose grammar forces rereading, but preserve clear longer sentences that suit the writer's cadence. Put the point before its qualification when that improves comprehension; put a condition first when the reader needs it to know whether an instruction applies.

### 4. Make repeated items easy to scan

Apply this step to existing or requested feeds, titles, cards, notifications, table summaries, and other items readers compare. Do not turn ordinary prose into a feed or add lists without permission. Parallel structure helps comparison here; it is not a reason to make every paragraph of an essay sound alike.

Use these five checks across the whole set, not just within individual items:

1. **Use a predictable opening.** Start with the subject and action. If every item has the same obvious subject, omit it and start with the verb. Match tense and aspect to the actual state: “Fixed…” for completed work, “Fixing…” for ongoing work, and an imperative for an instruction. Do not imply completion or progress that the source does not establish.
2. **Put distinguishing words first.** Move the status, topic, or action that separates one item from another near the start. Cut repeated openings such as “The issue reports that.” For status-focused order notifications, “Shipped: Order #1001” is easier to distinguish from “Delayed: Order #1002” than two items beginning “Your order…”. Keep enough context for each item to make sense on its own.
3. **Keep structure and vocabulary consistent.** Use the same grammatical pattern and order of information for comparable items. Use one term for each concept. Do not alternate among “issue,” “page,” and “report” if all refer to the same issue. Put the distinguishing information in a consistent early position rather than forcing every item to start with the same filler.
4. **Make variation meaningful.** Differences in length, detail, structure, or wording can imply differences in importance or evidence. Give comparable items comparable kinds of information. Keep a version number, exception, or extra explanation when it matters, but make its relevance clear. Never invent missing details, erase important qualifications, or force equal lengths to fill a template.
5. **Make verbs reflect the evidence and purpose.** In feedback summaries, distinguish praise, complaints, and requests when supported: “Users praise…,” “Users report…,” or “Users request…”. Do not intensify “mention” into “love” or “complain” without evidence. Preserve mixed sentiment rather than making a mixed finding wholly positive or negative to fit a dashboard's purpose.

Choose the pattern around what readers need to compare. A status label can come first in a notification; a subject and verb can lead a news headline. Do not force both into every item. Preserve meaningful differences in state, certainty, and sentiment even when they require a different form.

### 5. Tighten without flattening the voice

Remove repetition, empty qualifiers, throat-clearing, and commentary about the text itself. Cut in proportion to the actual padding. Do not assume an AI-assisted draft needs to lose half its length.

Use a light edit when the writing is already clear and distinctive. Use a deeper edit only when requested or when repetition, ambiguity, or structure blocks the reader.

Vary sentence and paragraph length naturally in continuous prose. Do not replace robotic uniformity with a rigid pattern of short sentences, deliberate awkwardness, or decorative quirks. In repeated items, retain the consistency that helps readers compare them.

End on the last concrete point, implication, or next action. Remove conclusions that merely repeat the draft and fake-profound final lines.

## Diagnose surface patterns without applying bans mechanically

Treat these patterns as signals to inspect, not proof of AI authorship. Keep any construction that serves a real purpose in the writer's voice.

### Meta-writing and staged insight

Remove ceremony that announces a point instead of delivering it, such as “Here is an overview,” “The following section explains,” “Let me be clear,” “It is worth noting,” “The real question is,” “What most people miss,” and “Here is what nobody tells you.” Keep the underlying substance.

### Empty contrast and drama

Replace formulaic contrasts, self-answered rhetorical questions, “Plot twist” setups, dramatic colon reveals, and stacked promotional fragments when a direct statement is stronger. Examples include “It is not X. It is Y,” “Not X. Not Y. Just Z,” “The secret: consistency,” and “Fast. Simple. Powerful.” Keep contrast, questions, colons, and fragments when they do real rhetorical work.

### Inflated language and weak analysis

Cut importance puffery such as “marks a pivotal moment,” “stands as a testament,” “underscores its significance,” “plays a vital role,” and “changes everything.” State the fact and let the reader judge its importance.

Treat “delve,” “leverage,” “utilize,” “robust,” “transformative,” “tapestry,” “realm,” “multifaceted,” and “ever-evolving” as warnings, not forbidden words. Replace them when inflated or vague; keep them when precise, quoted, required, or natural to the writer.

Replace trailing “highlighting,” “reflecting,” “showcasing,” or “underscoring” phrases when they gesture at significance without explaining a consequence. Name the source behind “experts agree,” “studies show,” or “many believe.” If no source is available, remove the unsupported attribution or flag it; do not present its underlying claim as established fact.

### Robotic form and decoration

Fix monotonous sentence shapes and identical paragraph structures in continuous prose, synonym cycling, unnecessary three-part lists, emoji headings, decorative bold text, and lists that need connective reasoning. Do not introduce variation into comparable feed items merely to make them look less formulaic.

### Hyphenation and punctuation

Keep conventional hyphenation; remove invented or decorative compounds. Write “AI safety,” not “AI-safety.” Prefer an established term or a plain explanation to a new hyphenated label. Apply normal grammatical distinctions: “a well-known result,” but “the result is well known.” Preserve required names and established technical terms.

Do not use em dashes as the default rhythm device. Remove clusters and decorative dashes. In short copy, prefer none. In longer prose, keep an occasional em dash when it serves the cadence better than a period, comma, colon, or parentheses. Use colons for explanations, quotations, labels, and lists, not manufactured reveals.

## Verify meaning, evidence, and readability

Review factual claims without silently changing them. Check for claims broader than the evidence, unclear numbers or denominators, unnamed authorities, incompatible dates or methods, shifting terminology, and contradictions. Verify claims when fact-checking is part of the task. Otherwise, flag doubtful or unverifiable claims. Never resolve a contradiction by choosing whichever version sounds better.

Before returning the result, check:

- The central point appears early enough for the genre, and headings describe their content.
- Each paragraph has a purpose; adjacent sentences and paragraphs have traceable relationships.
- Sentences are understandable on a first pass, with clear actors, actions, and references.
- The edit preserves meaning, qualifications, recognizable voice, and strong original sentences.
- Cutting matches the actual padding; jargon is necessary, defined, simplified, or flagged.
- Comparable items use consistent structure and terms, with distinguishing information early.
- Differences among repeated items reflect real differences, not arbitrary wording or detail.
- Tense, status, sentiment, and certainty match the source; no template has distorted them.
- Lists appear only with permission; invented compounds and decorative patterns are removed.
- No facts, examples, sources, or opinions were invented; unresolved claims and contradictions are flagged.
- The result sounds natural when read aloud, without mechanical application of style rules.

If a check fails, revise before returning the text. For detect mode, confirm that each reported problem has a specific excerpt, explanation, and suggested fix, and that the response makes no authorship claim.

## Return the result

For an edit or deep rewrite:

1. Return the complete edited text first. If editing a file in place, update the file and identify it in the response instead of duplicating the full document unless the user requests it.
2. Add a short **What changed** section when changes are material or the user requests one. Disclose material restructuring.
3. Add **Questions or claims to check** when unresolved ambiguities, unsupported claims, or contradictions remain.

For detect mode, name each problem, quote the smallest relevant excerpt, explain why it is a problem, and suggest a brief fix. Do not rewrite the full draft, score the writing, assign an AI probability, or claim to identify authorship.

## Source for repeated-text guidance

The scanability checks draw on Shreya Shankar's [Five Principles for Generating Readable AI Text in Bulk](https://fsdatalab.github.io/blog/agent-text-at-scale/), especially its guidance on sentence parsing, distinguishing words, parallel structure, meaningful variation, and verb connotations. Apply them as context-sensitive editorial guidance, not universal claims about reading or permission to change the evidence.
