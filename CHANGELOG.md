# Changelog

All notable changes to Vanguard are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/).

---

## [2.4.0] - 2026-09-10

### Added
- **xAI Grok 4.6** support — full provider integration with streaming
- **Google Gemini 3.8 Flash** and **Gemini 3.8 Pro** as default free/premium models
- **OpenAI GPT-6 Astra** and **GPT-6 Mini** provider support
- **Anthropic Claude Fable 5.1** and **Claude Opus 5** support
- **Meta Llama 5 Scout** via Groq free tier
- **DeepSeek R2 Distill** via Groq
- **Mistral Large 3** free-tier support
- Expanded custom endpoint validation
- New `maxTokens` and `temperature` config options

### Changed
- Improved codebase indexing speed by 3x on large repositories
- Better multi-file diff output with inline explanations
- Updated comparison table on website

### Fixed
- Context window overflow on projects with 500+ files
- Windows path handling for nested directories
- Groq API rate limit retry logic

---

## [2.3.0] - 2026-07-15

### Added
- **OpenRouter** provider — access 200+ models with one API key
- **AWS Bedrock** provider support
- Automatic test generation with framework detection
- `vanguard init` interactive setup wizard

### Changed
- Refactored provider system for easier third-party extensions
- Faster startup time (cold start reduced by 40%)

### Fixed
- Claude streaming response parsing edge case
- `.gitignore` patterns not respected in context indexing

---

## [2.2.0] - 2026-05-20

### Added
- **Azure OpenAI** provider support
- Multi-file rollback on failed edits
- `context.exclude` glob pattern support

### Changed
- Migrated to streaming-first architecture for all providers
- Improved error messages for invalid API keys

### Fixed
- Memory leak on long-running sessions
- Test runner hanging on Windows with Jest

---

## [2.1.0] - 2026-03-10

### Added
- **Groq** provider with Llama 4 Maverick and Scout
- Copy-to-clipboard for generated code blocks
- `vanguard config` CLI for managing settings

### Changed
- Unified config format (`vanguard.config.json`)

### Fixed
- Anthropic streaming timeout on large responses

---

## [2.0.0] - 2026-01-15

### Added
- Complete rewrite with new core engine
- Multi-file editing support
- Full codebase context indexing
- Built-in test generation and execution
- Provider-agnostic architecture
- Google AI Studio (Gemini 2.5 Flash) as default free model
- OpenAI and Anthropic BYOK support
- Custom OpenAI-compatible endpoint support
- Terminal-first UI with rich output

---

[2.4.0]: https://github.com/hadionlineclas/vanguard/releases/tag/v2.4.0
[2.3.0]: https://github.com/hadionlineclas/vanguard/releases/tag/v2.3.0
[2.2.0]: https://github.com/hadionlineclas/vanguard/releases/tag/v2.2.0
[2.1.0]: https://github.com/hadionlineclas/vanguard/releases/tag/v2.1.0
[2.0.0]: https://github.com/hadionlineclas/vanguard/releases/tag/v2.0.0
