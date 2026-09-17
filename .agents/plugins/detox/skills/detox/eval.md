# Detox eval

Use this after the rewrite. Answer each check with pass or fail. If any check fails, fix the draft before returning it.

For detect requests, make sure the response names each pattern found with a quoted line and a short fix, without rewriting the draft.

## Editing principles

1. Does the edit preserve the user's point without adding claims, examples, stats, quotes, or opinions?
2. Does it preserve the writer's distinctive vocabulary, cadence, bluntness, humor, uncertainty, digressions, and level of polish?
3. Does it leave strong human sentences alone instead of rewriting them for consistency or making every paragraph equally tidy?
4. Is the amount of cutting proportional to the actual slop, with no aggressive compression that strips out character?
5. Does the draft lead with what the reader needs while keeping personal setup that adds context, tension, or character?
6. Are points front-loaded where that improves clarity without forcing every unit into the same structure?
7. Do sentences earn their place, with concrete facts, protected details, and direct verbs where the draft supports them?
8. Does every generic sentence pass the portability test, or was it cut or made specific to this subject?
9. Does the draft use active voice with human subjects where possible?
10. Does the edit keep useful edge and preserve structure unless the structure was hurting the piece?
11. Are genuinely tangled sentences fixed while clear spoken cadence, fragments, and changes in pace remain intact?
12. Was a voice fingerprint extracted before editing?
13. Does the "What changed" section include the fingerprint and note any drift?
14. If the user provided an allowlist, were those words preserved?

## Words to cut

1. Are banned words, filler phrases, often-empty adverbs, and inflated claims removed unless quoted as examples?

## Patterns to cut

1. Are binary contrasts, negative listings, rhetorical setups, and throat-clearing openers removed?
2. Are faux-insight setups, colon reveals, superficial analysis, fake-strong verbs, synonym cycling, dramatic fragments, and robotic rhythm fixed?
3. Are importance puffery and weasel attribution replaced with plain facts and named sources, or flagged for the user when no source exists?
4. Is interpretive metadiscourse removed, including authorial metacommentary, reader guidance, emphasis markers, and redundant glossing?
5. Are fake-profound kicker lines deleted instead of rewritten into better metaphors?
6. Are summary-recap endings cut so the piece ends on a concrete point, takeaway, or next action?
7. Is formatting slop removed: Emoji headings, decorative bold, bullets that should be prose, headers over tiny sections?
8. Are colons sentence case unless grammar, a proper noun, a title, or code requires otherwise?
9. Are em dashes used sparingly: Usually none in short copy, and only 1-2 in longer drafts when they clearly help?
10. Are all 🔴 Critical patterns removed without exception?
11. Are 🟡 Moderate patterns removed unless the writer's domain or voice justifies them, with justification noted in "What changed"?
12. Are 🟢 Contextual patterns flagged to the user rather than silently cut?

## Final read

1. Does the draft avoid robotic symmetry, repeated sentence shapes, and stacked punchy fragments?
2. Would the writer recognize the edited draft as their own voice?
3. Would the edited draft sound natural if read to a sharp colleague?
4. Does the final output include the full edited draft and a short **What changed** section?
5. For detect requests, does the response name each pattern with a quoted line and a short fix, without rewriting, scoring, or claiming AI authorship?
6. For detect requests, is the output a table with columns: Severity | Pattern | Quoted line | Fix? Does it include a Slop Score (0–10)?
7. For drafts over ~800 words, was a chunk-and-merge strategy used? Are there no flow breaks or new patterns at chunk boundaries?
8. Does the "What changed" section include a severity-tagged edit table?

## Adversarial check

1. Did the edit introduce any new AI patterns that were not in the original draft?
2. If new patterns were found, were they fixed before the final output?
3. For 🟢 Contextual patterns with strong voice signals, was the user asked interactively (max 3 prompts)?

## Language scope

1. If the draft contains non-English text, were those sections left untouched?
2. Was the user informed about which sections were skipped?

## Slop score

1. Does the output include a Slop Score (0–10) for the original draft?
