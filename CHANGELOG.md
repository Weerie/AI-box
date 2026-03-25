## v0.1.8

### Added
- New **Settings Hub** page with square cards for:
  - Model/Provider Configuration
  - Agents
  - Advanced Settings (with existing confirmation popup)
- New **Your Characters** system (replacing User Settings):
  - Create/edit/delete multiple user characters
  - Only one active character at a time
  - Active character persists locally

### Changed
- Sidebar/navigation rework:
  - Settings is now a single entry point for config/admin pages
  - **Quick Start** moved to bottom section (above Logs)
  - **Logs** moved to bottom section
  - “User Settings” renamed to **Your Characters**
- Chat composer cleanup:
  - Prompt/Context + Input meters made compact
- New chat (Roleplay, You + AI):
  - Removed manual identity fields
  - Shows active character overview
  - Added note: *“Not who you want to be? change it in the character screen.”*

### Behavior Updates
- Added **“See advanced details”** toggle in chat header:
  - **OFF**: hides Prompt/Context meter, Input meter, and status row (“No chat selected | No agents selected”)
  - **ON**: shows them
- Removed outdated text: *“Create a new chat to choose mode and agents.”*

### Token Logic Simplification
- Removed per-agent `maxTokens` usage/settings
- All agents now use global max tokens from provider settings (with existing mode/provider caps)

### Repo Privacy
- Added ignore rules for local chat/log data and stopped tracking:
  - `server/data/conversations.json`
  - `server/data/history.json`
  - `server/data/request_logs.json`

### Validation
- Typecheck/build passed after changes (`tsc`, `vite build`)
