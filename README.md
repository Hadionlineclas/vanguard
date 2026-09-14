<div align="center">

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/VANGUARD-AI_Coding_Harness-a855f7?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMzYgMzYiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTE4IDNMM M gMjhIM0wxOCAzWiIgc3Ryb2tlPSIjYTg1NWY3IiBzdHJva2Utd2lkdGg9IjIuNSIgZmlsbD0ibm9uZSIvPjxjaXJjbGUgY3g9IjE4IiBjeT0iMjAiIHI9IjUiIGZpbGw9IiNhODU1ZjciIG9wYWNpdHk9IjAuOCIvPjwvc3ZnPg==">
  <img alt="Vanguard" src="https://img.shields.io/badge/VANGUARD-AI_Coding_Harness-a855f7?style=for-the-badge">
</picture>

### Free, open-source AI coding harness.
### Bring your own models — use free models out of the box or plug in your API keys.

[![MIT License](https://img.shields.io/badge/License-MIT-22c55e?style=flat-square)](LICENSE)
[![macOS](https://img.shields.io/badge/macOS-supported-a855f7?style=flat-square&logo=apple&logoColor=white)](#installation)
[![Linux](https://img.shields.io/badge/Linux-supported-a855f7?style=flat-square&logo=linux&logoColor=white)](#installation)
[![Windows](https://img.shields.io/badge/Windows-supported-a855f7?style=flat-square&logo=windows&logoColor=white)](#installation)

[Website](https://hadionlineclas.github.io/vanguard) &bull; [Documentation](#quick-start) &bull; [Discord](#community) &bull; [Contributing](#contributing)

<br>

</div>

---

## Why Vanguard?

AI coding tools shouldn't lock you into a single provider or cost $20/month. Vanguard is **100% free**, runs in your terminal, and works with **any model** — from free APIs to your own local setup.

- **Free forever** — No subscriptions, no credit card, no limits
- **Bring your own model** — 7+ free models pre-configured, or plug in any API key
- **Full codebase context** — Indexes your entire project so suggestions are architecturally aware
- **Multi-file editing** — Generate, refactor, and modify across files in a single operation
- **Built-in testing** — Auto-generates and runs tests after changes
- **Terminal-first** — Runs alongside your editor with zero friction
- **Open source** — MIT licensed, fully auditable, community-driven

---

## Installation

**macOS**
```bash
brew install vanguard
```

**Linux**
```bash
curl -fsSL https://get.vanguard.dev | sh
```

**Windows**
```bash
winget install vanguard
```

**npm (All Platforms)**
```bash
npm install -g @vanguard/cli
```

**From Source**
```bash
git clone https://github.com/Hadionlineclas/vanguard && cd vanguard && make install
```

Verify your installation:
```bash
vanguard --version
```

---

## Quick Start

**1. Initialize with a free model (no API key needed for some)**
```bash
vanguard init --provider google --model gemini-2.5-flash
```

**2. Start coding**
```bash
cd my-project && vanguard
```

That's it. Vanguard indexes your project and you can start asking it to write, refactor, debug, and test your code.

---

## Supported Models

### Free Models (no cost)

| Provider | Model | Best For |
|---|---|---|
| Google AI Studio | **Gemini 2.5 Flash** | Code gen, multi-file edits |
| Google AI Studio | **Gemini 2.0 Flash** | Quick completions, code review |
| Groq | **Llama 4 Maverick** | Reasoning, code quality |
| Groq | **Llama 4 Scout** | Everyday coding tasks |
| Groq | **Llama 3.3 70B** | Refactoring, debugging |
| Groq | **DeepSeek R1** | Complex multi-step problems |
| GitHub | **Copilot Models** | Seamless GitHub integration |

### Premium BYOK (bring your own API key)

| Provider | Models |
|---|---|
| OpenAI | GPT-4.1, GPT-4o, O3, O4-mini |
| Anthropic | Claude 4 Opus, Claude 4 Sonnet, Claude 3.5 Sonnet |
| Google | Gemini 2.5 Pro |
| Azure OpenAI | GPT-4.1, GPT-4o |
| AWS Bedrock | Claude, Llama, Titan |
| OpenRouter | 100+ models |

### Custom Endpoints

Any OpenAI-compatible or Anthropic-compatible API works — **Ollama**, **LM Studio**, **vLLM**, **text-generation-webui**, or your own server.

```bash
vanguard config set provider custom
vanguard config set base-url http://localhost:11434/v1
vanguard config set model llama3.3:70b
```

---

## Configuration

```jsonc
// vanguard.config.json
{
  "provider": "google",
  "model": "gemini-2.5-flash",
  "apiKey": "env:GOOGLE_API_KEY",
  "context": {
    "include": ["src/**", "docs/**"],
    "exclude": ["node_modules", ".git"]
  },
  "tests": {
    "auto": true,
    "framework": "vitest"
  }
}
```

---

## How It Compares

| Feature | Vanguard | GitHub Copilot | Cursor | ChatGPT |
|---|:---:|:---:|:---:|:---:|
| Full codebase context | :white_check_mark: | :large_orange_diamond: | :white_check_mark: | :x: |
| Multi-file editing | :white_check_mark: | :x: | :white_check_mark: | :x: |
| Free forever | :white_check_mark: | :x: | :x: | :large_orange_diamond: |
| Bring your own model | :white_check_mark: | :x: | :white_check_mark: | :x: |
| Terminal-native | :white_check_mark: | :x: | :x: | :x: |
| Open source | :white_check_mark: | :x: | :x: | :x: |
| Auto-generated tests | :white_check_mark: | :x: | :large_orange_diamond: | :large_orange_diamond: |

---

## Contributing

Contributions are welcome! Whether it's bug reports, feature requests, or pull requests — every contribution helps.

```bash
# Fork the repo, then:
git clone https://github.com/YOUR_USERNAME/vanguard
cd vanguard
make dev
```

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

## Community

- **Discord** — Get help, share ideas, connect with contributors
- **GitHub Issues** — Report bugs or request features
- **Discussions** — Ask questions, share your workflows

---

## License

MIT License. See [LICENSE](LICENSE) for details.

<div align="center">
<br>
<sub>Built with :purple_heart: by the Vanguard community</sub>
<br><br>
</div>
