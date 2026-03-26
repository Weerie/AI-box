# Weerie’s AI Box

Local-first LLM playground for roleplay, character simulation, and multi-agent conversations.

Specifically made to be beginner friendly, and easy to understand!

<img width="250" height="250" alt="favicon" src="https://github.com/user-attachments/assets/5e81d21a-8f93-4943-888a-6557c4a9b796" />

## Download

Download the latest Windows installer from **Releases**:  
[Latest Release](https://github.com/Weerie/AI-box/releases/tag/v0.1.9)

## Updating the app

You can find the instructions [here](https://github.com/Weerie/AI-box/blob/main/HOWTO_UPDATE.md)!

## What It Does

- Runs with local model providers (Ollama + OpenAI-compatible APIs)
- Supports **You + AI** for user interactive chatting, and **AI + AI** to let your LLM talk to itself!
- Includes **Agent Mode** for simple texting, and **Roleplay Mode** for increased freedom and creativity.
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

**Important Note:** The app might ask for network access. This is because a backend is bundled with the app that starts a server to send API requests to your local model.

## Integrity Verification
Each release includes SHA256SUMS.txt.

To verify on Windows:
```Powershell
certutil -hashfile .\Weerie_AI_box_Setup.exe SHA256
```
Compare the output hash with the matching line in SHA256SUMS.txt.

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
