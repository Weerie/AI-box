# Weerie’s AI Box

Local-first LLM playground for roleplay, character simulation, and multi-agent conversations.

## Download

Download the latest Windows installer from **Releases**:  
https://github.com/<your-username>/<your-repo>/releases/latest

## What It Does

- Runs with local model providers (Ollama + OpenAI-compatible APIs)
- Supports **You + AI** and **AI + AI** conversation modes
- Includes **Agent Mode** and **Roleplay Mode** presets
- Lets you create/manage custom agents and character profiles
- Stores chats/settings locally
- Includes request/error logs and conversation repair tools
- Exports chats to Markdown and agents to JSON

## System Requirements

- Windows 10/11 (x64)
- Local model runtime (recommended: Ollama)
- Enough VRAM/RAM for your selected model

## Quick Start

1. Install Ollama: https://ollama.com/download
2. Pull a model (example):
   ```bash
   ollama pull qwen2.5:7b
   ```
3. Start Ollama:
   ```bash
   ollama serve
   ```
4. Launch Weerie’s AI Box
5. Open Settings and set your provider/model
6. Start a new chat and choose mode + agents

## Privacy
All conversation data and runtime settings are stored locally on your machine.

## Troubleshooting
- Backend offline: restart app, verify local provider is running
- No model output: check Logs tab for request/model errors
- Wrong model behavior: confirm model name and provider URL in Settings

## Contributing
This project is distributed as a binary release.
Contribution and feedback are handled via Discord: COMING SOON

## License
Proprietary / All Rights Reserved.
No modification or redistribution rights are granted without explicit written permission.
