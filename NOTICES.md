# Notices: third-party text and its licences

_Last updated: 2026-09-24_

This repository's own files are MIT ([`LICENSE`](LICENSE)). The texts below are other people's,
under their own terms. None of their authors endorses this repository.

## Inputs

| File | Source | Licence |
|---|---|---|
| `inputs/uk-civil-service-generative-ai-guidance.txt` | "Guidance to civil servants on use of generative AI", Cabinet Office, Government Digital Service and Central Digital and Data Office, GOV.UK, first published 29 June 2023, updated 29 January 2024, since superseded by the Generative AI Framework for HMG. <https://www.gov.uk/government/publications/guidance-to-civil-servants-on-use-of-generative-ai/guidance-to-civil-servants-on-use-of-generative-ai>, retrieved 24 September 2026 through the GOV.UK Content API | Open Government Licence v3.0. Contains public sector information licensed under the Open Government Licence v3.0 |
| `inputs/wikipedia-bot-policy.txt` | "Wikipedia:Bot policy", English Wikipedia, revision 1371001773 of 24 August 2026, by Wikipedia contributors. <https://en.wikipedia.org/w/index.php?oldid=1371001773>, retrieved 24 September 2026 through the MediaWiki parse API | CC BY-SA 4.0 |
| `inputs/omb-m-25-21-section-3.txt` | Office of Management and Budget, Memorandum M-25-21, "Accelerating Federal Use of AI through Innovation, Governance, and Public Trust", 3 April 2025. <https://www.whitehouse.gov/wp-content/uploads/2025/02/M-25-21-Accelerating-Federal-Use-of-AI-through-Innovation-Governance-and-Public-Trust.pdf>, retrieved 24 September 2026 | Public domain, a work of the United States Government (17 U.S.C. 105) |

Changes, the same kind for all three: markup converted to plain text, one paragraph or list item
per line with a blank line between; a heading's level shown by leading `#` marks; omitted passages
marked `[...]` on a line of their own. Wording, spelling and errors are unchanged.

- **UK guidance.** The title line and the superseded notice, then the text from "This guidance
  outlines" to the end of "Practicalities of using generative AI in your role". Omitted: the
  introduction before that, the section on the government's approach and the annex of examples.
- **Wikipedia.** The page title, then the sections "Bot usage" to "Bot requirements", up to the
  subsection "Performance". Omitted: the shortcut boxes and every other section.
- **OMB M-25-21.** The PDF's text layer as extracted, with its OCR errors kept as printed
  («OFFlCEOFMANAGEMENTANDBUDGET», «0MB», «CAI Os», «govemmentwide», «11.» for ii.). The letterhead,
  date, number, addressee and subject lines of page 1; then section 3 to the end of 3(b)(v), then
  footnotes 20 to 23 as printed at the foot of those pages. Omitted: the FROM block, a signature
  image, and everything between the subject line and section 3. Page numbers and running heads are
  removed, wrapped lines joined, and the line-end hyphen in "high-impact" joined.

Example 2 in [`examples.md`](examples.md) quotes the Wikipedia text throughout and is licensed
CC BY-SA 4.0, like the text it quotes. Each file in `tests/fixtures/` is a copy of one worked
example with one defect planted, and carries that example's source and licence.

## Reference sources

| File | Source | Licence |
|---|---|---|
| `reference/sources/nist-ai-rmf-govern.txt` | NIST AI 100-1, Artificial Intelligence Risk Management Framework (AI RMF 1.0), January 2023, section 5.1 and Table 1. <https://doi.org/10.6028/NIST.AI.100-1> | Public domain, a work of the United States Government |
| `reference/sources/eu-ai-act-excerpts.txt` | Regulation (EU) 2024/1689 (Artificial Intelligence Act), OJ L, 12.7.2024, Articles 4, 9(1) to 9(2), 17(1), 26(1) to 26(2). <https://eur-lex.europa.eu/eli/reg/2024/1689/oj>. © European Union | Reuse under Commission Decision 2011/833/EU, source acknowledged |
| `reference/sources/rfc2119.txt` | S. Bradner, RFC 2119, "Key words for use in RFCs to Indicate Requirement Levels", March 1997. <https://www.rfc-editor.org/rfc/rfc2119.txt> | "Distribution of this memo is unlimited." Unmodified |

Changes to the first two: text extracted from the official PDF, lines unwrapped, end-of-line
hyphens removed, paragraph numbers restored to their paragraphs, page furniture removed. In the NIST
file Table 1's two columns are written as one line per category and subcategory. In the AI Act file
the points of Article 9(2) are omitted and marked `[...]`. Each file opens with a one-line header
and a rule; the wording below the rule is unchanged.

ISO/IEC 42001 is named in [`reference/register-schema.md`](reference/register-schema.md) by clause
number only. Its text is copyrighted and is not in this repository.
