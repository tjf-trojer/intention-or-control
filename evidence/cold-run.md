# Cold runs: a fresh session, the folder, an input it has never seen

_Last updated: 2026-09-25_

**Method.** A fresh general-purpose Claude Code session, model `claude-opus-5-5`, was given `identity.md`, `rules.md`,
`examples.md` and `reference/`, and nothing else: no scripts, no README, no conversation. It
translated `inputs/omb-m-25-21-section-3.txt`, which no worked example uses, and listed every place
the rules left it unsure. The OMB text is the hardest of the three inputs: an OCR'd PDF text layer
with nested lists, run-in headings and a lost full stop. Both runs took place on 24 September 2026,
one attempt each. Neither saw a register of this input: Example 3 was made from run 2's output
afterwards.

## Run 1, under the first rules

Output: [cold-run-1-output.md](cold-run-1-output.md), unedited. Every quotation in it sat on its
line: it kept «0MB», «CAI Os», «govemmentwide» and «OFFlCEOFMANAGEMENTANDBUDGET» as the input has them. Its
list of doubts found five defects in the rules, and each one changed the folder:

| What the session met | What it did | What changed |
|---|---|---|
| The collective test flagged «the head of each agency», the rules' own example of a named office, because it ends in "agency" | Followed the lexicon | The test reads the head word: «the head of each agency» cuts to «the head» |
| «Agency heads must:» followed by items with their own force | Made the lead-in an empty rule; agency heads owned nothing | Every list item is quoted with its lead-in; a lead-in has no entry of its own |
| «so long as they do not conflict», a "do not" that commands nothing | Set the term aside by judgment | "never", "do not", "don't" and "always" count only where they open a sentence or main clause |
| «Agencies are responsible for ensuring that agency AI governance boards:» | Filed as a statement: the lexicon had no term for it | «is responsible for» and «are responsible for» are force terms, and their subject is the owner |
| Evidence and timing in a neighbouring sentence | Took only the owner from elsewhere, as the rules implied | Written down: only the owner may come from another sentence. Example 1 had taken a footnote from another sentence as evidence and was corrected |

It also asked how to cut a sentence whose full stop the scan lost («…covered AL Agencies must
also…»). The rule now says: cut there, change no character.

## Run 2, under the revised rules

Output: [cold-run-2-output.md](cold-run-2-output.md), unedited. The session checked its own
quotations against the input with a short script, since it was not given `verify.py`, and every one
sat on its line. Its doubts were narrower than run 1's and produced three sentences in `rules.md`:
a sentence ending in a colon over headed subsections is not a lead-in; an item's run-in title
(«11. Develop Compliance Plans.») is its first sentence; a lead-in that names a party makes it
answerable for everything its item requires, the item's later sentences included.

The session had read the last point narrowly, so owners named in a lead-in did not reach the
sentences under it. [Example 3](../examples.md) is its register with the six owner cells that the
written rule changes, and the statuses and counts that follow from them:

| Row | Owner in run 2 | Owner in Example 3 | Status in Example 3 |
|---|---|---|---|
| R10 | not in source | «agency heads» L22 | intention: evidence |
| R34 | not in source | «Agency heads» L68 | intention: evidence, when |
| R36 | not in source | «Agency heads» L68 | control |
| R37 | not in source | «Agency heads» L68 | intention: when |
| R40 | not in source | «Agency heads» L68 | control |
| R43 | not in source | «Agency heads» L68 | control |

Every other cell of Example 3 is the session's.

## Run 3, under the rules split into `rules/`

Model `claude-opus-5-5`, 25 September 2026, one attempt, in Claude Code with `verify.py` allowed.
Input: the "Governance" section of the Generative AI Framework for HMG
(`inputs/uk-generative-ai-framework-governance.txt`), a document no example uses and the one that
superseded Example 1. Output: [cold-run-3-output.md](cold-run-3-output.md), unedited. It passed all
eight checks on its first run of `verify.py`, and it found no owner and no fixed moment in the
section: every rule it holds is an intention.

One of its doubts was a defect the checks let through. Under «The inventory should be regularly kept
up to date with the following details:» (L39) it filed the items «Describe…», «Include…» and
«Employ…» as commands of class MUST, which turns a «should» into a «must». The rules now say that an
item whose opening verb finishes its lead-in takes the lead-in's force, and `verify.py` fails such a
row. [cold-run-3-register.md](cold-run-3-register.md) is its register with those three rows refiled
as recommendations and the counts that follow; every other cell is the session's. The fix has not
yet been through a fresh session of its own.

The run also shows what the rules do with a section headed "Practical recommendations" that is
written in the imperative («Set up an AI governance Board…»): each sentence is filed by its own
words, so those are rules. A reader who takes the heading as governing them reads the section
differently; the register quotes both, and the difference is visible.
