# Rules: how a policy becomes a register

_Last updated: 2026-09-24_

Seven steps, in this order. The contract they fill is
[`reference/register-schema.md`](reference/register-schema.md); the word lists are
[`reference/lexicon.md`](reference/lexicon.md). Read both before the first translation.

## 1. Number the lines

Count every line of the input from 1, blank lines included: a file's own lines, or pasted text as
pasted. Every quotation carries these numbers.

## 2. Source

Quote the title, the issuer and the date or version where the input prints them. A title, issuer or
date you know but the input does not print is `not in source`.

## 3. Cut the text into sentences

Cut where the text cuts. Where a scan has lost a full stop and a new sentence plainly begins
(«…covered AL Agencies must also…»), cut there and change no character.

- **A list under a lead-in.** A lead-in is a sentence that ends in a colon and introduces the items
  below it («Agency heads must:»). Each item is an entry of its own, quoted together with its
  lead-in, and with every lead-in above it in a nested list. The lead-in has no entry of its own.
  An item's run-in title («1. Chief AI Officers.») is its first sentence. Where an item holds
  several sentences, the lead-in joins the first; the others are entries of their own. A sentence
  ending in a colon over headed subsections, not items, is not a lead-in and is filed by its own
  force.
- **A sentence that runs through a list** and carries on after it («Because bots:» … «the community
  expects bots to meet high standards…») is one entry, quoted in parts joined by ` + `.
- Headings, title lines and the omission mark `[...]` are entries of their own. A heading that ends
  in a colon is still a heading.

## 4. File each sentence

Find its force terms in the lexicon. The strongest decides.

| Strongest term | Goes to |
|---|---|
| MUST, MUST NOT, WILL, WILL NOT, an instruction in the imperative | Register |
| SHOULD, SHOULD NOT | Not rules, `recommendation «term»` |
| MAY | Not rules, `optional «term»` |
| none, or one that does not bind here | Not rules, `statement` |

A sentence holding a forced term is a rule, whatever it reads like. An item quoted with its lead-in
is filed by the strongest term in both.

## 5. Fill the row

| Column | How |
|---|---|
| Force | The strongest term as printed, and its class from the lexicon |
| Addressee | The party the rule binds, as printed. A passive rule with no agent and an imperative name no one: `not in source` |
| Owner | The party the text makes answerable. Look in the rule and its lead-in first, then in a sentence that assigns responsibility for the same conduct, and cite that sentence's line. An addressee is the owner when it is a named office («the head of each agency»), not when it is a crowd («Civil servants»). The subject of «is responsible for» is the owner of that rule. A lead-in that names a party («Agency heads must:») makes it answerable for everything its item requires, the item's later sentences included. Flag `(collective)` by the lexicon |
| Evidence | A record or artefact named in the rule's own quotations, lead-in included. Never from another sentence |
| When | The frequency, date, deadline or triggering event in the rule's own quotations, lead-in included, kept as printed: «Within 60 days of the issuance of this memorandum» stays that. A condition of application («When using generative AI») is not a When. Flag `(unspecified)` by the lexicon |
| Status | `control` when Owner is named and not collective, Evidence is named, and When is named and not unspecified; otherwise `intention:` and what is missing |

## 6. Referred elsewhere

Quote every document the policy names by title or number, once, at its first mention.

## 7. Count, then check

Fill the tally from the rows. Then run
`python3 scripts/verify.py <register.md> --input <policy.txt>`. Without a shell, open every cited
line, find every quotation on it, and recount the tally.

## Never

- Name an agent for a passive rule. «will be deauthorized» names no one who deauthorizes.
- Make a crowd the owner because it is the one addressed.
- Expand an acronym, correct a spelling or repair OCR. «0MB», «CAI Os» and «govemmentwide» stay.
- Convert timing. «annually» is not "each January"; «after six months» is not a date.
- Move force. A «should» is not a «must», and a conditional «Should the operator return» is not a
  recommendation.
- Summarise, merge or skip a sentence.
- Say whether a rule is adequate, lawful or wise.
