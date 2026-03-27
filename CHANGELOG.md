# Changelog

## v0.2.4 - 2026-03-27

### Added
- Modular backend architecture under `server/routes`, `server/services`, and `server/validation`.
- Central request validation middleware with Zod schemas for chat, agents, settings, conversations, and repair flows.
- Real upstream streaming adapters for both OpenAI-compatible SSE and Ollama JSON-line streams.

### Changed
- Uninstaller flow now uses a single clear data-retention choice: **Save local chats / agents (recommended)**.
- `/api/chat/stream` now emits true live token deltas from provider streams instead of simulated chunking.
- Frontend build strategy now uses vendor chunk splitting and lazy-loaded heavy screens for faster initial load.
- Packaging rules now explicitly include backend route/service/validation modules and exclude non-runtime source/build files.
- Web icon/meta references now point to `.ico` assets to reduce oversized static web output.

### Fixed
- Fixed premature SSE cancellation caused by request-close handling, which could cut streams early.
- Fixed stream-side response assembly error path in chat streaming (`Cannot read properties of undefined (reading 'id')`).
- Preserved fallback behavior to non-stream chat path when upstream streaming is unavailable.

### Improved
- API robustness with consistent `400` validation responses in the shape `{ error, code, details }`.
- Better deploy consistency for packaged desktop builds with updated backend resource inclusion.
- Reduced installer footprint significantly (current setup artifact ~86 MB).

## v0.2.3 - 2026-03-26

### Added
- Uninstaller option: **Save local chats / agents (recommended)** so users can keep local data during uninstall.
- New **Local Chat Storage** section in Personal Settings showing the exact storage folder and managed files.
- Personal Settings actions to quickly **Open Folder** (desktop app) and **Copy Path** for storage location.

### Changed
- Installer behavior now defaults to preserving AppData on uninstall unless the user explicitly chooses to remove it.

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
