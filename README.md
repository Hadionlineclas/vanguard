<div align="center">

<br>

# <img src="https://img.shields.io/badge/▲-a855f7?style=for-the-badge" height="30"> VANGUARD

### The free, open-source AI coding harness.
### Bring your own models — use free models out of the box or plug in your API keys.

[![MIT License](https://img.shields.io/badge/License-MIT-22c55e?style=flat-square)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/hadionlineclas/vanguard?style=flat-square&color=a855f7)](https://github.com/hadionlineclas/vanguard/stargazers)
[![macOS](https://img.shields.io/badge/macOS-supported-a855f7?style=flat-square&logo=apple&logoColor=white)](#installation)
[![Linux](https://img.shields.io/badge/Linux-supported-a855f7?style=flat-square&logo=linux&logoColor=white)](#installation)
[![Windows](https://img.shields.io/badge/Windows-supported-a855f7?style=flat-square&logo=windows&logoColor=white)](#installation)

[Website](https://hadionlineclas.github.io/vanguard) &bull; [Documentation](#quick-start) &bull; [Discord](#community) &bull; [Contributing](CONTRIBUTING.md)

<br>

<img src="https://img.shields.io/badge/Claude_Fable_5.1-Anthropic-d946ef?style=flat-square" alt="Claude">
<img src="https://img.shields.io/badge/GPT--6_Astra-OpenAI-10a37f?style=flat-square" alt="GPT-6">
<img src="https://img.shields.io/badge/Gemini_3.8-Google-4285f4?style=flat-square" alt="Gemini">
<img src="https://img.shields.io/badge/Grok_4.6-xAI-1d9bf0?style=flat-square" alt="Grok">
<img src="https://img.shields.io/badge/Llama_5-Meta-0467df?style=flat-square" alt="Llama">
<img src="https://img.shields.io/badge/DeepSeek_R2-DeepSeek-6366f1?style=flat-square" alt="DeepSeek">

</div>

---

## Why Vanguard?

AI coding tools shouldn't lock you into a single provider or cost $20/month. Vanguard is **100% free**, runs in your terminal, and works with **any model** — from free APIs to your own local setup.

- **Free forever** — No subscriptions, no credit card, no limits
- **Bring your own model** — 10+ free models pre-configured, or plug in any API key
- **Full codebase context** — Indexes your entire project so suggestions are architecturally aware
- **Multi-file editing** — Generate, refactor, and modify across files in a single operation
- **Built-in testing** — Auto-generates and runs tests after changes
- **Terminal-first** — Runs alongside your editor with zero friction
- **Open source** — MIT licensed, fully auditable, community-driven

---

## Demo

```
$ vanguard

  ▲ Vanguard v2.4.0
  Provider: Google (gemini-3.8-flash)
  Project: my-app (47 files indexed)

  > Add authentication with JWT tokens, bcrypt hashing,
    and a protected /dashboard route

  ✓ Created src/lib/auth.ts
  ✓ Created src/middleware/protect.ts
  ✓ Modified src/routes/index.ts
  ✓ Created src/routes/dashboard.ts
  ✓ Created tests/auth.test.ts
  ✓ All 12 tests passing

  5 files changed · 247 lines added · 0 errors
```

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
git clone https://github.com/hadionlineclas/vanguard && cd vanguard && make install
```

Verify your installation:
```bash
vanguard --version
```

---

## Quick Start

**1. Initialize with a free model**
```bash
vanguard init --provider google --model gemini-3.8-flash
```

**2. Start coding**
```bash
cd my-project && vanguard
```

That's it. Vanguard indexes your project and you can start asking it to write, refactor, debug, and test your code.

---

## Supported Models

### Free Models (zero cost)

| Provider | Model | Best For |
|---|---|---|
| Google AI Studio | **Gemini 3.8 Flash** | Ultra-fast code gen, multi-file edits |
| Google AI Studio | **Gemini 2.5 Flash** | Quick completions, code review |
| Groq | **Llama 5 Scout** | Reasoning, high-quality code |
| Groq | **Llama 4 Maverick** | Everyday coding, refactoring |
| Groq | **DeepSeek R2 Distill** | Complex multi-step problems |
| xAI | **Grok 4.6 Mini** | Fast inference, debugging |
| GitHub | **Copilot Models** | Seamless GitHub integration |
| Mistral | **Mistral Large 3** | Multilingual code, large context |

### Premium BYOK (bring your own API key)

| Provider | Models | Get API Key |
|---|---|---|
| **OpenAI** | GPT-6 Astra, GPT-6 Mini, O5-pro, O4-mini | [platform.openai.com](https://platform.openai.com) |
| **Anthropic** | Claude Fable 5.1, Claude Opus 5, Claude Sonnet 5 | [console.anthropic.com](https://console.anthropic.com) |
| **Google** | Gemini 3.8 Pro, Gemini 2.5 Pro | [aistudio.google.com](https://aistudio.google.com) |
| **xAI** | Grok 4.6, Grok 4.6 Vision | [console.x.ai](https://console.x.ai) |
| **Azure OpenAI** | GPT-6 Astra, GPT-6 Mini | [azure.microsoft.com](https://azure.microsoft.com) |
| **AWS Bedrock** | Claude, Llama, Titan | [aws.amazon.com](https://aws.amazon.com) |
| **OpenRouter** | 200+ models | [openrouter.ai](https://openrouter.ai) |

### Custom Endpoints

Any OpenAI-compatible or Anthropic-compatible API works — **Ollama**, **LM Studio**, **vLLM**, **text-generation-webui**, or your own server.

```bash
vanguard config set provider custom
vanguard config set base-url http://localhost:11434/v1
vanguard config set model llama5:70b
```

---

## Configuration

```jsonc
// vanguard.config.json
{
  "provider": "google",
  "model": "gemini-3.8-flash",
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

<details>
<summary><b>All configuration options</b></summary>

| Key | Type | Description |
|---|---|---|
| `provider` | string | AI provider (`google`, `openai`, `anthropic`, `xai`, `groq`, `mistral`, `custom`) |
| `model` | string | Model name/ID |
| `apiKey` | string | API key or `env:VAR_NAME` to read from environment |
| `baseUrl` | string | Custom API endpoint URL |
| `context.include` | string[] | Glob patterns for files to index |
| `context.exclude` | string[] | Glob patterns for files to skip |
| `tests.auto` | boolean | Auto-run tests after code changes |
| `tests.framework` | string | Test framework (`vitest`, `jest`, `pytest`, `go`, etc.) |
| `maxTokens` | number | Max tokens per response |
| `temperature` | number | Model temperature (0-2) |

</details>

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
| Custom endpoints | :white_check_mark: | :x: | :white_check_mark: | :x: |

---

## Contributing

Contributions are welcome! Whether it's bug reports, feature requests, or pull requests — every contribution helps make Vanguard better.

```bash
git clone https://github.com/hadionlineclas/vanguard
cd vanguard
make dev
```

Please read our [Contributing Guide](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md) before getting started.

---

## Community

- [**Discord**](#) — Get help, share ideas, connect with contributors
- [**GitHub Issues**](https://github.com/hadionlineclas/vanguard/issues) — Report bugs or request features
- [**GitHub Discussions**](https://github.com/hadionlineclas/vanguard/discussions) — Ask questions, share workflows

---

## Sponsors

Vanguard is community-funded. If you find it useful, consider supporting the project.

<a href="https://github.com/sponsors/hadionlineclas">
  <img src="https://img.shields.io/badge/Sponsor_Vanguard-a855f7?style=for-the-badge&logo=githubsponsors&logoColor=white" alt="Sponsor">
</a>

---

## License

MIT License. See [LICENSE](LICENSE) for details.

<div align="center">
<br>
<sub>Built with :purple_heart: by <a href="https://github.com/hadionlineclas">hadionlineclas</a> and the Vanguard community</sub>
<br><br>
</div>
