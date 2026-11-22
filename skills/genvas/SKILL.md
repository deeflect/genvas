---
name: genvas
description: Build, dry-run price, and execute AI image, video, voiceover, music, SFX, and 3D node graphs in the local Genvas desktop app over MCP using your own API keys. Use when generating or chaining AI media assets via Genvas.
metadata:
  version: 1.4.1
  author: deeflect
  source: https://genvas.app
---

# Genvas

Genvas is a native desktop node canvas (Mac, Windows, Linux) for AI images, video, voiceovers, music, and 3D models using your own provider API keys (OpenAI, Gemini, ElevenLabs, Fal, Kie, OpenRouter, xAI, Fish Audio, Higgsfield).

## Install and connect

1. Download the signed beta installer from https://github.com/deeflect/genvas/releases/latest and add your provider API keys in Genvas settings.
2. Genvas sets up Claude Code and Codex MCP automatically on install. To connect manually on macOS:

```bash
# Claude Code
claude mcp add --scope user genvas -- /Applications/Genvas.app/Contents/Resources/server/mcp/run

# Codex
codex mcp add genvas -- /Applications/Genvas.app/Contents/Resources/server/mcp/run
```

## Workflow

1. Discover available models and schemas (`list_models`, `inspect_model`, `read_guide`).
2. Create or update a workflow board (`create_workflow`, `add_model_node`, `add_generate_node`, `update_workflow`).
3. Always dry-run pricing before spending (`estimate`) and validate connections (`lint_workflow`).
4. Run the workflow (`run_workflow`, `run_status`) and inspect saved local outputs (`list_gallery`, `inspect_node`).
