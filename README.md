# Detox

Detox your writing. Remove 20+ patterns of AI slop without flattening your personal voice. Get a slop score, voice fingerprint, and structured edit diffs.

*Originally created by Peter Yang, modified and enhanced by Pratham Sharma.*

https://github.com/user-attachments/assets/f3055450-78eb-4672-880a-88a4fa54bde9

## Problem

AI makes it easy to generate clean writing that all sounds the same. Even the best models keep producing lines like:

- “It’s not X. It’s Y.”
- “What nobody tells you is…”
- “The future isn’t coming. It’s already here.”

When you use AI to edit, it can also smooth away the vocabulary, cadence, humor, and imperfections that make the writing sound like you.

## How to install Detox

The easiest way to install the skill is to paste this into ChatGPT, Claude Code, Codex, or your favorite coding agent:

```text
Install the /detox skill globally from https://github.com/petergyang/no-ai-slop
```

You can also install it with `npx`:

```sh
npx skills add petergyang/no-ai-slop --skill detox --global --yes
```

### For Google Antigravity

Detox is packaged as an Antigravity plugin:
- **Workspace level**: Include [`.agents/plugins/detox`](.agents/plugins/detox) in your repository root.
- **Global level**: Installed in `~/.gemini/config/plugins/detox-plugin/` for cross-workspace availability.

## How to use Detox

### Edit your writing

```text
/detox (your writing)
```

The skill removes the AI slop patterns, preserves your personal voice, and lists what it changed.

### Detect slop

```text
/detox is this slop? (your writing)
```

The skill quotes every slop pattern it found without guessing whether AI wrote the text.

### Override banned words

```text
/detox [allowlist: leverage, robust] (your writing)
```

Words in the allowlist won't be auto-flagged. Useful for technical writing, engineering specs, or formal reports.

### Generate slop for fun

```text
/detox generate slop about (topic)
```

Use it to generate the most cringe AI slop possible as satire.

### Platform-specific editing

```text
/detox --mode linkedin (your writing)
```

Available modes: `linkedin`, `email`, `essay`, `changelog`, `thread`. Each mode adjusts which patterns are prioritized and how aggressively Detox edits.

## The slop that Detox catches

Detox checks for 20+ patterns, including:

1. **Binary contrasts.** “It’s not X. It’s Y.”
2. **Throat-clearing openers.** “Here’s the thing,” “Let me be clear”
3. **Faux-insight setups.** “What nobody tells you,” “The part everyone misses”
4. **Colon reveals.** “The best part: it learns.”
5. **Dramatic fragments.** “That’s it. That’s the whole thing.”
6. **Superficial analysis.** “highlighting the team’s commitment to innovation”
7. **Importance puffery.** “marks a pivotal moment,” “a testament to”
8. **Weasel attribution.** “experts agree,” “studies show”
9. **Synonym cycling.** “The agent handles your email. The assistant drafts replies.”
10. **Fake-profound endings.** “The future isn’t coming. It’s already here.”

It also checks the fundamentals: Lead with the point when that helps, use active voice, untangle hard-to-follow sentences, and prefer concrete details over abstractions.

## What's New in Detox v2.0 (Enhanced & Modified)

Detox was evolved from the original *No AI Slop* project by Pratham Sharma with major architectural improvements and feature enhancements:

- **Severity-Tiered Pattern Engine**: Patterns are categorized into Critical (always kill), Moderate (usually cut/rewrite), and Contextual (genre-dependent), preventing over-editing and false positives.
- **Voice Fingerprint Analysis**: Extracts and locks the writer's sentence length variance, contraction rate, and tone before editing, ensuring the edited output sounds unmistakably like *you*.
- **Slop Score (0–10) & Structured Diagnostics**: Both detect and edit modes return a quantified Slop Score with structured findings tables (pattern name, quoted text, severity tier, rationale).
- **Interactive Review Mode**: Solicits user input for ambiguous cuts or edge cases rather than unilaterally discarding meaning (capped at 3 queries per draft).
- **Platform Modes**: Specialized presets for `--mode linkedin`, `email`, `essay`, `changelog`, and `thread` to adapt intensity and preserve context-appropriate formatting.
- **Context-Aware Word Allowlist**: Override banned-word warnings using `[allowlist: term1, term2]` for technical documentation and engineering specs.
- **Chunked Processing for Long Drafts**: Handles documents over 800 words with chunked processing to prevent context exhaustion and skipped text.
- **Adversarial Self-Check Eval**: An expanded 30+ check evaluation suite in `eval.md` to guarantee the editor doesn't introduce fresh AI cliches while rewriting.
- **Language Scope & Mixed-Language Support**: Explicit rules preventing accidental corruption or translation of code snippets, foreign terms, and proper nouns.

## What’s inside

- [`SKILL.md`](skills/detox/SKILL.md) contains the editing rules and workflow.
- [`eval.md`](skills/detox/eval.md) contains the checks the skill runs on its work.
- [`.codex-plugin/plugin.json`](.codex-plugin/plugin.json) contains the ChatGPT and Codex plugin metadata.
- [`build_plugin.py`](scripts/build_plugin.py) builds and validates the plugin package.
- [`.agents/plugins/detox/plugin.json`](.agents/plugins/detox/plugin.json) contains the Antigravity plugin manifest.
- [`CHANGELOG.md`](CHANGELOG.md) contains the full version history and release notes.

Detox is also available as a plugin in ChatGPT, Codex, and Google Antigravity.

## Want more great AI skills?

Check out [Behind the Craft](https://behindthecraft.com), my personal AI system with over a dozen other quality skills and courses.

Subscribe to my [YouTube channel](https://www.youtube.com/@PeterYangYT?sub_confirmation=1) and [newsletter](https://creatoreconomy.so) for practical AI tutorials and interviews.

## Credits & Attribution

- **Original Creator**: Peter Yang ([Behind the Craft](https://behindthecraft.com), [GitHub](https://github.com/petergyang/no-ai-slop))
- **Modified & Enhanced by**: Pratham Sharma

## License

MIT License — see [LICENSE](LICENSE) for details. Original work Copyright (c) 2026 Peter Yang; modified by Pratham Sharma.
