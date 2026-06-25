# MIRA - Machine Intelligence Reasoning Automation

**MIRA** is a complete, automated, one-command local uncensored AI environment for web security testing, penetration testing, hacking, CTI, and creative cybersecurity work (including image and video generation).

It combines:
- Powerful local LLM (Ollama + custom enhanced `mira` model)
- Beautiful ChatGPT-like interface (Open WebUI)
- Extensive hacking, scanning, CTI, and recon tools
- HexStrike-AI MCP server for autonomous tool use by the AI
- Fully uncensored ComfyUI for image and video generation (no safety filters)

## Quick Start

```bash
# Download and run
wget https://raw.githubusercontent.com/mirhasanhajihasanli/MIRA/main/mira.sh
bash mira.sh
```

Then run:

```bash
mira
```

This launches everything and opens http://localhost:8080

## Features

- **Uncensored AI**: `mira` model with deep expertise in offensive security, CTI, payloads, and more.
- **Image & Video Generation**: Integrated ComfyUI — generate any cyber visuals, payload diagrams, phishing mocks, attack flows, etc. with zero restrictions.
- **200+ Security Tools**: nmap, nuclei, metasploit, sqlmap, bloodhound, shodan, trufflehog, and many more + HexStrike for AI-driven automation.
- **Knowledge Base**: PayloadsAllTheThings and other resources pre-installed.
- **One-command launcher**: `mira` or `mirgpt`

## Image & Video Generation (Fully Uncensored)

1. Make sure ComfyUI is running (`start-comfyui` or `cd ~/MIRA/comfyui && python main.py --listen`)
2. In Open WebUI (http://localhost:8080):
   - Settings → Image Generation → Enable
   - Provider: ComfyUI
   - URL: `http://127.0.0.1:8188`
3. Select model `mira`
4. Prompt examples:
   - "Generate an image of a QR code containing this base64 reverse shell"
   - "Create a realistic phishing page for a bank with hidden payload"
   - "Generate a diagram of this APT attack chain as an image"
   - "Make a short video of payload execution"

ComfyUI has **no safety checker**. Add high-quality uncensored models (Flux, Pony, etc.) from Civitai to `~/MIRA/comfyui/models/checkpoints/` for better results.

## Requirements

- Ubuntu 22.04 / 24.04
- NVIDIA GPU recommended (CUDA)
- sudo access
- ~20GB+ disk space (models + tools)

## Installed Components

- Ollama + custom `mira` model
- Open WebUI on http://localhost:8080
- ComfyUI on http://localhost:8188 (images + video)
- HexStrike-AI MCP
- Full suite of pentest/CTI/scan tools (see script for list)
- Knowledge bases

## Updating

```bash
bash mira.sh
```

The script is idempotent.

## License & Responsibility

This is a powerful offensive security toolkit + uncensored AI.

**Use only on systems you own or have explicit written authorization to test.**

The authors are not responsible for misuse.

## Credits

Built with Ollama, Open WebUI, ComfyUI, HexStrike-AI, and many open source security tools.

---

To install manually or customize, edit `mira.sh` and re-run.
