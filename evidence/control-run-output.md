# Control register: Guidance to civil servants on use of generative AI

Source: `uk-civil-service-generative-ai-guidance.txt` (line numbers below refer to that file).
Prepared: 2026-09-24. Status: draft, needs owner names and confirmed evidence sources before use.

## Read this before using the register

1. **The source is superseded.** Line 3 says: "This page has been superseded by the Generative AI Framework for HMG". If you intend to follow current UK government guidance, the register should be built from that framework instead. I have not read it; it was not part of what I was given. If you are using this text as a model for your own policy, the register below is usable, but it reflects the old version.
2. **The supplied text is incomplete.** Line 5 is an elision ("[...]"). Line 25 promises examples of how to use and not use generative AI "below", and line 21 promises a section on "the government's wider approach"; neither is in the file. GAI-13 depends on those missing examples.
3. **The source names no control owners, specifies no evidence, and sets no review frequency** other than a one-off review of the guidance after six months (line 19). It assigns responsibility only to individual users (line 23). Everything marked **[P]** below is my proposal, not the policy's text. Fill in named people and confirm each evidence source actually exists in your organisation before you treat the register as ready.
4. **Most rules govern what individuals type into external web tools, which the organisation cannot observe by default.** The source says so itself: government "has no oversight over how data, which is entered into web-based generative AI tools, is then used" (line 43). Unless you run data loss prevention (DLP), a web proxy that logs uploads to AI services, or an enterprise AI tool with prompt logging, the available evidence is attestation, training records and self-reported incidents. That shows people were told the rule. It does not show they followed it. An ISO/IEC 42001 auditor is likely to raise this.

Legend: **[S]** = stated in the source. **[P]** = proposed here; your organisation must confirm it.

## Register

| ID | Rule | Source | Owner | Evidence | Review frequency | ISO/IEC 42001 Annex A (indicative) |
|---|---|---|---|---|---|---|
| GAI-01 | Do not enter personal data into generative AI tools. | L11, L15, L43 | Accountable: each user [S, L23]. Control owner: Data Protection Officer [P] | [P] Signed policy acknowledgement; training completion; DLP or proxy alerts for personal-data patterns sent to AI domains (if deployed); data protection incident log | [P] Alerts and incidents: monthly. Attestation: annual and on policy change | A.9 Use of AI systems; A.10 Third-party relationships |
| GAI-02 | Do not enter sensitive information into generative AI tools. | L11, L15, L43 | Accountable: each user [S]. Control owner: Information security lead [P] | [P] As GAI-01, with DLP rules keyed to your sensitivity labels | [P] As GAI-01 | A.9; A.10 |
| GAI-03 | Do not enter classified information into generative AI tools. | L15 | Accountable: each user [S]. Control owner: Information security lead [P] | [P] As GAI-01, with DLP rules keyed to classification markings; security incident log | [P] As GAI-01 | A.9; A.10 |
| GAI-04 | Do not enter information that reveals the intent of government and may not be in the public domain. | L15 | Accountable: each user [S]. Control owner: [P] to be named (policy or communications lead) | [P] Attestation and incident reports only; no realistic technical detection (no pattern to match) | [P] Attestation: annual. Incidents: on occurrence | A.9 |
| GAI-05 | Do not enter information that, if compromised or lost, could damage individuals, groups, an organisation or government. | L43 | Accountable: each user [S]. Control owner: Information security lead [P] | [P] No evidence beyond GAI-01 to GAI-04 unless users record a pre-use check | [P] Reviewed with GAI-01 to GAI-04 | A.9 |
| GAI-06 | Do not input work documents into generative AI tools. | L47 | Accountable: each user [S]. Control owner: Information security lead [P] | [P] DLP or proxy blocks/alerts on file uploads to AI domains (if deployed); attestation | [P] Alerts: monthly. Attestation: annual | A.9; A.10 |
| GAI-07 | Have regard to the principles of GDPR when using these tools. | L15, L23 | Accountable: each user [S]. Control owner: Data Protection Officer [P] | [P] Data protection assessment per AI tool in use; training completion | [P] Per tool: before approval and on material change. Training: annual | A.9; A.5 Assessing impacts |
| GAI-08 | Check outputs for bias and misinformation before use; apply the same rigour as to any other work; challenge outputs with your own judgement and knowledge. | L17, L49, L51 | Accountable: each user [S]. Control owner: line managers / document approvers [P] | [P] Sample review of documents disclosed as AI-assisted (via GAI-09) for a recorded check; approver sign-off | [P] Quarterly sample (size to set) | A.9 |
| GAI-09 | Where AI output is used verbatim or with minor alterations, make that clear to readers: cite the tool in a footnote with its URL and any sources used as inputs. | L17, L49, L55 | Accountable: each user [S]. Control owner: document approvers / records management [P] | [P] Footnotes present in a sample of published and internal documents | [P] Quarterly sample | A.8 Information for interested parties |
| GAI-10 | Before sharing information, know what information you have access to, the rights and restrictions that apply to it, and the conditions under which it may be shared. | L33 | Accountable: each user [S]. Control owner: information governance lead [P] | [P] Information asset register with handling conditions; training completion | [P] Annual | A.9 (and your existing information governance controls) |
| GAI-11 | Before entering information into any system, ask: does it need to be entered, what will be done with it, what rights are given away. | L35 | Accountable: each user [S]. Control owner for the tool-level questions: IT procurement / information security [P] | [P] Per-tool assessment of vendor terms (data use, retention, training on inputs, rights) | [P] Per tool: before approval and when vendor terms change | A.10 |
| GAI-12 | Users are responsible for their own actions when using these tools. | L23 | Each user [S]. Enforcement: HR [P] | [P] Signed acknowledgement of the policy | [P] Annual and on policy change | A.3 Internal organization |
| GAI-13 | Users may sign up to generative AI tools with their gov.uk email address for the appropriate uses described in the guidance, while being aware of what they enter. | L57 | IT / identity management [P] | [P] List of AI services with accounts under the organisation's email domain (SSO records or sign-up logs) | [P] Quarterly | A.4 Resources; A.10 |
| GAI-14 | Contact CDDO (cddo@digital.cabinet-office.gov.uk) about new tools with potential to improve government work. | L7 | AI policy owner, for your organisation's equivalent intake channel [P] | [P] Log of submissions | [P] Annual | none obvious |
| GAI-15 | Review the guidance after six months to address emerging practice and better understanding of use cases. | L19 | AI policy owner [P] | [P] Dated review record; version history of the policy | [S] Once, after six months. [P] Annual and on material change | A.2 Policies related to AI |

Annex A column: group level only, from the standard's structure as I know it; not checked against the standard text in this run. Verify against your copy before citing clause numbers.

## Open issues by row

- **GAI-02, GAI-05:** "Sensitive information" is not defined in the supplied text. Until it is tied to your classification or labelling scheme, neither rule can be tested and DLP rules cannot be written for it.
- **GAI-03:** Depends on a classification scheme the text does not describe.
- **GAI-04:** Specific to UK government. If you are not a UK government body, restate it (for example, as unannounced organisational decisions or plans) and name an owner.
- **GAI-05:** This is the umbrella test; GAI-01 to GAI-04 are specific cases of it. You may prefer to keep GAI-05 as the parent control and test through its children.
- **GAI-06:** Read literally, this bans entering any work document, which is broader than GAI-01 to GAI-05 and sits uneasily with line 41 ("We encourage you to explore this technology"). The register cannot resolve this; the policy owner has to decide whether the literal reading stands.
- **GAI-07:** "Have regard to" is not testable. The testable part is GAI-01. The text says "GDPR"; confirm which data protection regime applies to you.
- **GAI-08:** The source does not say what "checked" means or require any record of the check. Without a recording requirement there is no evidence to sample.
- **GAI-09:** Covers only verbatim or minor-alteration use; substantially reworked output is not covered. "Sources used as inputs" is ambiguous (prompts, uploaded documents, or both). Sampling finds only disclosed use; undisclosed use is invisible to this control.
- **GAI-10:** A general information-handling rule, not specific to AI. If you already have information governance controls, cross-reference them rather than duplicating.
- **GAI-11:** Asks each user to assess vendor terms. In practice this should be done once per tool by whoever approves tools; the user-level check then reduces to "is this an approved tool".
- **GAI-13:** "Appropriate uses described in this guidance" refers to examples missing from the supplied text, so the scope of this permission cannot be set. For a non-UK-government organisation, replace gov.uk with your own domain.
- **GAI-14:** Worded as an invitation ("please contact"), not a requirement. Keep it only if you want an intake channel for new tools.
- **GAI-15:** Line 3 shows the policy has already been superseded, so this review has in effect happened. ISO/IEC 42001 expects the AI policy to be reviewed at planned intervals, so a one-off review is not enough.

## Statements not carried into the register

These are exhortations or descriptions with no behaviour that could be checked:

- L13: be "cautious and circumspect".
- L29: be "inquisitive about new technologies"; "exercise caution".
- L39: description of the technology's evolution.
- L41: "explore this technology and consider the implications".
- L45 to L51, the "three Hows": awareness content. The actionable parts are covered by GAI-06, GAI-08 and GAI-09.

## Gaps an ISO/IEC 42001 auditor is likely to raise

The source does not contain any of the following. Each would be a new control written by your organisation, not something taken from this policy:

- No list of approved tools (ChatGPT and Bard are named only as examples, L39).
- No definition of sensitive information and no link to a classification scheme.
- No procedure for when someone has entered prohibited information (reporting, containment, notification).
- No training requirement.
- No technical enforcement or monitoring; compliance rests entirely on individual behaviour.
- No named policy owner.
- No requirement to assess impact per use case before use.
