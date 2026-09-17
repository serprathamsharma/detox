# Detox plugin submission

## Positioning

Detox removes 20+ patterns that make AI-assisted writing sound generic without flattening the writer's voice.

Peter uses it during the middle 50% of his writing process to improve spelling, grammar, and clarity. He writes the first draft himself and does the final line-by-line pass himself.

## Starter prompts

1. @Detox (text)
2. @Detox is this slop? (text)
3. @Detox --mode linkedin (text)

## Positive test cases

1. Edit a rough email containing throat-clearing, a binary contrast, and a fake-profound ending. Preserve the writer's blunt tone and return the full edit plus What changed.
2. Audit a LinkedIn post without rewriting it. Name each pattern, quote the affected line, and suggest a short fix.
3. Edit a personal essay with humor and digressions. Remove only the real slop and keep the personality.
4. Edit a product update containing concrete numbers. Preserve every supported fact and make the verbs more direct.
5. Edit a long spoken draft. Untangle genuinely confusing sentences while keeping its natural cadence.
6. Edit a draft using `--mode linkedin`. Verify the edit is aggressive on puffery but preserves professional tone.
7. Detect slop in a long post (1500+ words). Verify chunked processing produces a complete findings table with Slop Score.
8. Edit a draft with `[allowlist: leverage, robust]`. Verify those words are preserved.
9. Edit a mixed English/Spanish draft. Verify Spanish sections are untouched and noted in "What changed".

## Negative test cases

1. The user asks a factual question without sharing writing. Do not trigger the editing workflow.
2. The user asks whether AI wrote a passage. Do not guess authorship; offer a pattern audit instead.
3. The user asks the plugin to invent supporting facts or sources. Do not invent them; ask for evidence or keep the claim out.
4. The user pastes a draft in Japanese only. Do not apply English patterns; inform the user about the language scope.

## Release notes

Version 2.0.0 adds severity-tiered patterns (Critical/Moderate/Contextual), voice fingerprinting, structured detect output with Slop Score, chunked processing for long drafts, word allowlists, platform modes (linkedin/email/essay/changelog/thread), adversarial eval pass, interactive mode for ambiguous cuts, and English language scope declaration. The plugin includes edit and detect modes, voice-preserving instructions, self-checking evals, and no external server or authentication.
