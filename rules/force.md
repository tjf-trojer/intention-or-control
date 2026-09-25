# Force: filing each entry

_Last updated: 2026-09-25_

Step 4. Find the entry's force terms in [`reference/lexicon.md`](../reference/lexicon.md). The
strongest decides where it goes.

| Strongest term | Goes to |
|---|---|
| MUST, MUST NOT, WILL, WILL NOT, an instruction in the imperative | Register |
| SHOULD, SHOULD NOT | Not rules, `recommendation «term»` |
| MAY | Not rules, `optional «term»` |
| none, or one that does not bind here | Not rules, `statement` |

A sentence holding a forced term is a rule, whatever it reads like. An item quoted with its lead-in
is filed by the strongest term in both. The Force cell quotes the lexicon term as written
(«Never», «must»), or, for an imperative outside the lexicon, its opening verb phrase («be aware»).

| Case | Rule | In the examples |
|---|---|---|
| One rule at two forces | Each sentence is filed by its own words; the register does not reconcile them | Example 1: R1 «Never put…» L11 is a rule; «You should never put…» L43 is a recommendation |
| A conditional "should" | «Should the operator return» sets a condition; the sentence is filed by its «must» | Example 2, R10 |
| A "will" that commits | Is a rule | Example 1, R3 «This guidance will be subject to a review…»; Example 3, R38 «0MB will provide templates…» |
| A "will" that describes | Is a statement | Example 1, «A generative AI tool, such as a LLM, will answer your question…» L51 |
| A "may" of possibility | Is a statement; a "may" that permits is optional | Example 2: «…stronger methods of verification may be required.» L39 is a statement; «Bot operators may wish to redirect…» L23 is optional |
| An imperative opening a main clause | Counts as an instruction | Example 1, R6 «…, do not input…»; R8 «Therefore, be aware…» |
| An item that completes its lead-in | An item whose opening verb finishes the lead-in's sentence takes the lead-in's force; the verb is no imperative of its own. «never», «do not» and «always» keep their force | `inputs/uk-generative-ai-framework-governance.txt` L39 + L41: «The inventory should be regularly kept up to date with the following details:» + «Describe each system’s purpose…» is a recommendation ([cold run 3](../evidence/cold-run.md)) |
| "do not" inside a clause | Is an ordinary word | Example 3, footnote 23 «…so long as they do not conflict…», a recommendation by its «encouraged» |
| A verb that points or asks | «Note that», «See», «please contact» give no instruction | Example 2, «Note that high-speed…» L15; Example 1, «…please contact…» L7 |
| A responsibility sentence | «is responsible for» is a force term, and its subject is the owner | Example 2, R5; Example 1, R4 |
| A normative phrase the lexicon lacks | «it is important to» holds no force term; the sentence is a statement until the lexicon changes | Example 1, «References: … it is important to make clear…» L55 |
| A question | Is never forced | Example 1, «Does that information need to be entered in that system?» L35 |
