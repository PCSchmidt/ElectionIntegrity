# Election Integrity Document Corpus

This repository is a research collection about four election-integrity topics discussed in President Trump's July 16, 2026 address. It is designed to help a reader inspect the supplied records, understand how they relate to the address, and distinguish an allegation from a confirmed finding.

The collection is not a finding that every claim in the source documents or speech is true. Some material is redacted, many documents are agency records describing assertions or investigations, and the available local evidence has not independently corroborated every claim. Treat the repository as a starting point for careful review.

## Start Here

If you are visiting for the first time, read these files in order:

1. [Election Integrity Speech-to-Corpus Briefing](Election_Integrity_Speech_to_Corpus_Briefing.md): Plain-language explanation linking the address to specific source documents, their limits, possible policy implications, and questions still requiring evidence.
2. [Address Transcript](President%20Trump%20Address%20Transcript%20-%20July%2016%202026.md): Timestamped transcript used to identify what was said. This is a YouTube caption track, not an independently corrected official transcript.
3. One of the four numbered source folders below: Original PDFs grouped by topic.
4. [Evidence Registry](evidence_registry/): Searchable tables and visual aids for readers who want to trace claims to pages and review status.

## What Is in This Repository

The source collection contains 58 PDFs, totaling 269 pages. The four numbered folders are separate themes from the same address:

| Folder | Plain-language purpose | Examples of useful material |
| --- | --- | --- |
| [1. Vulnerabilities in Voting and Counting Systems](1.%20Vulnerabilities%20in%20Voting%20and%20Counting%20Systems/) | Cybersecurity, voting and counting infrastructure, and related intelligence reporting | The CISA election report, election-infrastructure assessments, and Venezuela-related intelligence material |
| [2. China Acquisition and Exploitation of American Voter Data](2.%20ChinaAcquisitionExploitationAmericanVoterData/) | Allegations and records concerning foreign collection, analysis, or use of U.S. voter data | Redacted intelligence records, voter-data tables, internal correspondence, and state-notification material |
| [3. Michigan Voter Registration Investigation](3.%20MichiganVoterRegistrationInvestigation/) | FBI and Justice Department records related to alleged voter-registration fraud in Michigan | Case timeline, interview memoranda, registration-application reviews, delay memo, and declination materials |
| [4. Noncitizens on State Voter Rolls](4.%20Noncitizens%20on%20State%20Voter%20Rolls/) | Voter-roll and citizenship-verification issues | Alien voter-registration summary and voter-registration database threats report |

The ZIP files in the repository are source-package copies. The numbered folders are the easier way to browse the extracted PDFs.

## How to Read the Evidence Carefully

The most important distinction in this repository is between a document **saying** something and the underlying event being **independently established**.

- A presidential speech is evidence of the President's public position.
- An agency memo or email is evidence that its author or agency recorded a view, decision, allegation, or investigative step.
- A redacted title, table, or report may be relevant, but it can leave out the source, method, context, and conclusion needed to verify a broad claim.
- An investigation, a database mismatch, or a witness statement is not the same as a court finding or proof of criminal liability.
- Optical character recognition, or OCR, makes a scanned page searchable. It can make mistakes; readers should check the original PDF page before relying on an exact quotation.

The briefing uses phrases such as **"what the visible record supports"** and **"material limitation"** to keep those categories separate.

## Useful Research Materials

### Briefing and evidence tracking

- [Election Integrity Speech-to-Corpus Briefing](Election_Integrity_Speech_to_Corpus_Briefing.md): The best narrative overview, including a dedicated section on federal agency conduct, disclosure, and accountability.
- [Claim Ledger](evidence_registry/claim_ledger.csv): Carefully limited claims that have been checked against a source page. Current entries are marked as `unverified_source_assertion` unless independently corroborated.
- [OCR Review Decisions](evidence_registry/ocr_review_decisions.csv): Tracks which OCR-flagged pages have been visually checked and whether they are suitable for quotation.
- [Unresolved Questions](evidence_registry/unresolved_questions.csv): Questions that should be answered before drawing stronger conclusions.
- [Speech Subtopic Traceability](evidence_registry/speech_subtopic_traceability.csv): Connects portions of the address to the four source themes.
- [Page Search Index](evidence_registry/page_search_index.csv): A page-level search aid for the corpus.

### Visual summaries

These images are descriptive tools. They show where topics and terms occur; they do not measure truth, culpability, or the strength of an allegation.

- [Topic Term Map](evidence_registry/visualizations/03_topic_term_map.png)
- [Address-to-Corpus Term Comparison](evidence_registry/visualizations/04_address_to_corpus_terms.png)
- [Descriptive Word Clouds](evidence_registry/visualizations/05_descriptive_word_clouds.png)
- [Speech Subtopic Traceability](evidence_registry/visualizations/06_speech_subtopic_traceability.png)
- [OCR Review Progress](evidence_registry/visualizations/07_ocr_review_progress.png)
- [Certainty and Limitation Language](evidence_registry/visualizations/08_certainty_and_limitation_language.png)
- [Shared Document Relationships](evidence_registry/visualizations/09_shared_document_relationships.png)

## For Readers Who Want to Audit the Work

The repository includes two Jupyter notebooks. They are optional; the briefing and source PDFs can be read without technical tools.

- [Corpus Inventory and OCR Notebook](00_corpus_inventory_and_ocr.ipynb): Inventories PDFs, extracts available text, performs OCR for scanned pages, and produces page-level metadata in [analysis_output](analysis_output/).
- [Evidence Registry and Claim Review Notebook](01_evidence_registry_and_claim_review.ipynb): Builds search aids, review queues, visualizations, and the evidence registry.

The notebooks preserve useful provenance information, including document paths, page numbers, extraction method, and source-file SHA-256 hashes. A hash is a digital fingerprint used to identify whether a source file has changed.

## Important Limitations

- This is a curated local corpus, not a complete public record of the matters discussed.
- Many PDFs contain redactions. A missing detail may reflect protection of sources, privacy, classification, legal limits, or other reasons; it should not be treated as proof of concealment.
- The original documents remain the authoritative local source. OCR text and CSV summaries are working aids.
- The evidence review is ongoing. Not every OCR-flagged page has received visual review, and the claim ledger is intentionally narrow.
- Questions of misconduct, criminal liability, election outcomes, or foreign attribution require fuller records and applicable legal or technical standards. They cannot be resolved from file names, isolated excerpts, or word-frequency graphics.

## Repository Layout

```text
README.md                                      This guide
Election_Integrity_Speech_to_Corpus_Briefing.md Source-linked plain-language briefing
President Trump Address Transcript - July 16 2026.md  Address transcript
1. ... through 4. ...                          Original source PDFs by topic
analysis_output/                               OCR text, inventory, and page metadata
evidence_registry/                             Claim tracking, review records, and visualizations
00_corpus_inventory_and_ocr.ipynb              OCR and inventory workflow
01_evidence_registry_and_claim_review.ipynb    Evidence-review workflow
```

## Contributing or Extending the Review

The most useful additions are source-specific and checkable: page references, original documents, reliable corroborating sources, corrections to OCR, or clearly identified contrary evidence. When adding a claim, record the source file, page, exact quotation, context, and whether the claim is a source assertion, independently corroborated fact, or unresolved allegation.
