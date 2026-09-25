# Control run: the same policy, without the folder

_Last updated: 2026-09-25_

**Method.** A fresh general-purpose Claude Code session, model `claude-opus-5-5`, read
`inputs/uk-civil-service-generative-ai-guidance.txt` and nothing else in this repository, and got
the request a compliance lead would make: "We need to turn this AI policy into a control register
for our ISO 42001 work. One row per rule: the rule, who owns it, what evidence shows it is being
followed, and how often it is reviewed. Please make it complete and ready to use." One attempt, run
on 24 September 2026. Nothing in this repository was in its context but the input. Its output is [control-run-output.md](control-run-output.md), unedited.

**What it did well.** It said the policy names no control owner and no evidence, and it marked every
addition as its own: `[P]` for proposed, `[S]` for stated. It noticed the superseded notice and the
missing examples. As advice to a compliance lead, much of it is sound.

**What it did to the policy**, set against [Example 1](../examples.md):

| | Without the folder | With the folder |
|---|---|---|
| Rule text | Rephrased in every row; no rule is quoted | Quoted with its line |
| Owner, evidence, review | All 45 cells hold proposed content. The policy's own words appear in 12 owner cells (the collective "each user") and 1 frequency cell | Stated and quoted, or `not in source` |
| Force | Six rows built only from "should" sentences come back as commands: GAI-03, GAI-04, GAI-05, GAI-07, GAI-10, GAI-11 | Each sentence keeps its own force |
| Sentences | GAI-01 merges L11's «Never put…» with the «should never» sentences at L15 and L43 | Filed separately, by their own words |
| An invitation | «please contact» (L7) becomes rule GAI-14 | A statement |
| Every sentence accounted for | No. A closing list names some of what was left out | Yes, and `verify.py` fails a register that drops one |
| ISO/IEC 42001 Annex A | A mapping column written "from the standard's structure as I know it; not checked against the standard text" | Clause numbers only, as pointers, in the schema |

**What it shows.** The session without the folder is not careless; it labels its guesses. Its
register is still one in which no cell can be checked against the policy without rereading the
policy, and in which a recommendation and a command look the same. The folder's register is
sparser, and every cell in it is the policy's.
