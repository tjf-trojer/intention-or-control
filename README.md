# Intention or Control

**Which rules in this AI policy does anyone answer for?**

_Last updated: 2026-09-24_

Give it an AI policy. It gives back a control register: every rule the policy states, quoted with
its line, and for each rule the owner, the evidence and the moment the policy itself names, or
`not in source`. A rule with all three is a **control**. A rule missing one is an **intention**.

It converts and nothing else. It never proposes an owner, never guesses a review date, and never
says whether a rule is any good.

## Use it

**In a Claude project.** Add `identity.md`, `rules.md`, `examples.md`,
`reference/register-schema.md` and `reference/lexicon.md` to the project knowledge. Set the project
instructions to:

> You are the translator in identity.md. Follow rules.md step by step and produce one register as
> defined in reference/register-schema.md. Every value is a quotation with its line, or
> "not in source".

Paste the policy's text and say **"Translate this policy."** Any AI policy, usage guideline or
directive in English works; [`inputs/`](inputs/) holds three real ones to try.

**In Claude Code.** Clone the repository, open the folder ([`CLAUDE.md`](CLAUDE.md) routes), save
the policy as a text file and say "Translate `<file>`". Then check the result:

```bash
git clone https://github.com/tjf-trojer/intention-or-control
python3 scripts/verify.py my-register.md --input my-policy.txt
```

## What comes back

A register in five sections, the same every time, defined in
[`reference/register-schema.md`](reference/register-schema.md). Three rows from
[Example 2](examples.md), Wikipedia's bot policy, with the Force and Addressee columns left out:

| ID | Rule | Owner | Evidence | When | Status |
|---|---|---|---|---|---|
| R3 | «Bots must edit only while logged into their account.» L19 | «its operator» L21 | not in source | not in source | intention: evidence, when |
| R7 | «Bot accounts will be marked by a bureaucrat as being in the "bot" user group upon BAG request.» L27 | «a bureaucrat» L27 | «the "bot" user group» L27 | «upon BAG request» L27 | control |
| R8 | «Bot accounts that have had no logged actions or edits for two years, where the listed operator has also had no logged actions or edits for two years, will be deauthorized.» L31 | not in source | not in source | «for two years» L31 | intention: owner, evidence |

R8 is written in the passive: it says what happens and names no one who does it, so the register
names no one either. The full register also records each rule's force and whom it binds, files every
other sentence as a recommendation, an option, a statement or a heading, lists the documents the
policy points to, and ends in a tally.

| You see | It means |
|---|---|
| `control` | The policy names an owner who is not a crowd, a record, and a moment someone could check |
| `intention: owner, evidence, when` | What the policy leaves open for this rule |
| `(collective)` | The owner is a crowd («users», «Agencies»): named, but no one in particular answers |
| `(unspecified)` | The moment fixes nothing («regularly», «on an ongoing basis») |
| `not in source` | The policy does not say. Nothing was filled in |

## Check it

**One row by hand.** R7 above cites line 27. Open
[`inputs/wikipedia-bot-policy.txt`](inputs/wikipedia-bot-policy.txt) at line 27: "Bot accounts
will be marked by a bureaucrat as being in the "bot" user group upon BAG request." Owner, record and
moment are all in that sentence. Every cell of every register has the same two halves: the words,
and the line they stand on.

**Every register at once:**

```bash
python3 scripts/verify.py                                  # every register here, then the fixtures
python3 scripts/verify.py my-register.md --input my-policy.txt
```

Python 3.9 or later, standard library, no network. The checker reads its word lists from
[`reference/lexicon.md`](reference/lexicon.md), so the contract and the check cannot drift apart.
It fails a register when:

- a quotation is not on the line it cites, down to spelling, capitals and OCR errors;
- a cell holds anything but a quotation, `not in source`, or one of the fixed values above;
- an addressee, a record or a moment comes from outside the rule's own sentence (only the owner may);
- a sentence of the input is missing, or filed both as a rule and as not a rule;
- a sentence holding "must", "shall", "is prohibited" or an opening "Never" is filed as advice, or
  a rule is filed weaker than its own words;
- a flag, a status or a count does not follow from the rows and the lexicon.

Each file in [`tests/fixtures/`](tests/fixtures/) plants one such defect in a worked register: an
invented owner, an invented annual review, a title spelled the usual way instead of as printed, a
judgement slipped into a cell. The default run fails unless each is caught by the check it names.

**What it cannot check** is reading: whether a named office really answers for that rule, whether
a "will" binds or describes, whether a sentence is an instruction. Those calls are the
translator's, and each one sits in a cell that quotes the words it rests on.

## Why owner, evidence and when

| Attribute | Asked for by |
|---|---|
| Owner | [NIST AI RMF, GOVERN 2.1](reference/sources/nist-ai-rmf-govern.txt#L25); [EU AI Act, Art. 17(1)(m)](reference/sources/eu-ai-act-excerpts.txt#L25) and [26(2)](reference/sources/eu-ai-act-excerpts.txt#L29) |
| Evidence | [EU AI Act, Art. 17(1)](reference/sources/eu-ai-act-excerpts.txt#L12) and [17(1)(k)](reference/sources/eu-ai-act-excerpts.txt#L23) |
| When | [NIST AI RMF, GOVERN 1.5](reference/sources/nist-ai-rmf-govern.txt#L21): "determining the frequency of periodic review"; [EU AI Act, Art. 17(1)(d)](reference/sources/eu-ai-act-excerpts.txt#L16) |

ISO/IEC 42001 asks for the same three in clauses 5.3, 7.5 and 9; its text is copyrighted, so only
the clause numbers appear. The provisions define the attributes. A register never says the
translated policy is bound by them.

**Who does this by hand today:** AI officers, compliance and ISMS leads and internal auditors,
whenever a policy has to become the control register an ISO/IEC 42001 management system, an audit
or a board asks for. The usual shortcut is to fill the empty cells with plausible owners, which
produces a register the policy never said.

## Evidence

- [`evidence/control-run.md`](evidence/control-run.md): the same UK policy, given to a session
  without this folder and asked for a register "complete and ready to use". It labelled its
  guesses, and every owner, evidence and review cell it returned holds content the policy does not
  state.
- [`evidence/cold-run.md`](evidence/cold-run.md): a fresh session with only the folder translated
  the OCR'd OMB memo it had never seen, twice. What it found unclear became the rules as they stand;
  its second register, with six owner cells corrected and listed, is Example 3.

## Limits

- **English only.** The lexicon is English.
- **It reports the policy, not the organisation.** An owner named in a separate procedure is
  `not in source` until that procedure is translated too.
- **The word lists are choices**, written down in [`reference/lexicon.md`](reference/lexicon.md)
  where they can be argued with.
- **Not an audit and not legal advice.**

## Licence

This repository's own files are MIT ([`LICENSE`](LICENSE)). The inputs and reference sources keep
their own licences; Example 2 is CC BY-SA 4.0 like the Wikipedia text it quotes. Sources and
changes: [`NOTICES.md`](NOTICES.md).
