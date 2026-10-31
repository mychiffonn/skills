# Verify citations and maintain the bibliography

Read this reference when adding references, writing related work, or checking
citation support. Verify both bibliographic identity and the associated claim.
An existing bibliography entry is a lead, not proof that its fields are correct.

## Find the primary source

Search the paper title, authors, or specific claim with available scholarly
search tools or web search. Prefer the publisher, conference proceedings,
ACL Anthology, OpenReview, or an author-submitted arXiv record. Discovery
services help locate a paper; they do not replace reading the source.

Confirm the title, authors, publication year, venue or preprint status, and a
stable identifier. Prefer the published version when it is the relevant source.
If metadata conflicts, resolve it against the publication record and PDF. A
single authoritative record can establish identity; do not require a second
index to contain a newly released paper.

## Check the claim

Read the passage, experiment, or theorem that supports the sentence being
written. An abstract can support an abstract-level summary; it is insufficient
for a claim about an ablation, assumption, proof, or detailed numerical result
that it does not report. Keyword overlap is not evidence of support.

Check the population, conditions, metric, and qualifications. Distinguish the
source's observation from the interpretation proposed in the new manuscript.
Cite the primary work instead of a survey when making a claim about that work.
Avoid stronger priority claims such as “first” without a defensible search.

## Retrieve and check metadata

Retrieve BibTeX from the authoritative record or an official metadata endpoint.
Use DOI content negotiation, ACL Anthology exports, OpenReview exports, or
arXiv citation metadata as available. Preserve the project's bibliography system
and citation-key conventions. Do not generate bibliographic fields from memory.

If an export is unavailable, transcribe only fields verified against the primary
record and record that provenance privately. An export can contain errors too:
check author order, title, year, venue, DOI, and publication type against the
actual source. Do not manufacture a DOI or silently treat a preprint as a
conference publication.

Useful primary documentation:

- [Crossref REST API](https://www.crossref.org/documentation/retrieve-metadata/rest-api/)
- [DOI content negotiation](https://citation.crosscite.org/docs.html)
- [ACL Anthology citation guidance](https://aclanthology.org/info/how-to-cite/)
- [Semantic Scholar API](https://api.semanticscholar.org/api-docs/)
- [arXiv API](https://info.arxiv.org/help/api/basics.html)

Use services already available before proposing a new dependency or MCP server.
Check current API usage policies before bulk retrieval. Do not bake prices,
index sizes, or request quotas into the writing workflow.

## Keep unresolved references explicit

Never invent a plausible reference. If the claim or identity cannot be verified,
keep a clearly labeled citation-needed marker in a working draft or working
notes, and report the exact gap at delivery. Do not add a fake bibliography
entry to suppress a build warning. Do not describe a draft with unresolved
citations as submission ready.

## Integrate and verify

- Reuse a verified entry rather than adding a duplicate for another version.
- Preserve accents, author order, and capitalization of technical names.
- Follow the venue's citation style and the manuscript's existing commands.
- Ensure each cited source supports the clause to which it is attached.
- Check for undefined citations, unused duplicate entries, and broken links.
- Rebuild the bibliography and inspect rendered citations when editing LaTeX.

Keep source locators, verification notes, and search history outside the paper.
Do not add internal artifact paths to the manuscript's bibliography or prose.
