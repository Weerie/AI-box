# Changelog

## v0.2.2 - 2026-03-26

### Changed
- Reworked response pacing to feel less "same-sized" and more natural across turns.
- Updated runtime response rules to use adaptive length behavior (short for quick beats, longer for major scene moments).
- Relaxed rigid output sizing in default roleplay templates while keeping structure and continuity guidance.
- Reworked AI agent generation templates for more specific, roleplay-ready character drafts.
- Updated Quick Start step 4 to use the Ollama app settings flow for model location changes, replacing old `OLLAMA_MODELS` terminal-env guidance.

### Improved
- Better roleplay flow for smaller 7B-8B models by reducing overly strict guard-rail behavior.
- More dynamic scene rhythm in both story-style and discussion-style turns.
- Improved generated agent quality with stronger role inference, richer hooks, and better fallback drafting when model output is weak.

## v0.2.1 - 2026-03-26

### Changed
- Updated default advanced system prompts for stronger steering on 7B-8B roleplay models.
- Tightened participant/controller/continuity instructions for better consistency across different local models.
- Added stricter story/discussion output rules to reduce bland or generic replies and improve roleplay formatting quality.
