# Changelog

## 2.0.0

### Added
- Severity-tiered pattern system (Critical / Moderate / Contextual)
- Voice fingerprint extraction before editing
- Structured detect output with findings table
- Slop Score (0–10) for both detect and edit modes
- Chunked processing for drafts over 800 words
- Before/after diff table in "What changed"
- Context-aware word allowlist syntax
- Platform modes: linkedin, email, essay, changelog, thread
- Adversarial eval pass to catch self-introduced patterns
- Interactive mode for ambiguous cuts (max 3 prompts per draft)
- Language scope declaration (English-only with mixed-language handling)

### Changed
- Patterns reorganized from flat list to three severity tiers
- "What changed" output now uses structured table format with voice fingerprint
- Eval checklist expanded from 18 to 30+ checks
- Workflow expanded from 6 to 8 steps
- Banned words list now supports user allowlist overrides

## 1.0.6

- Initial release as Detox (renamed from No AI Slop)
- 20+ AI slop patterns with edit and detect modes
- Voice-preserving editing principles
- Self-checking eval workflow
