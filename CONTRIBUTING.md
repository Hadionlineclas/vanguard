# Contributing to Vanguard

Thank you for your interest in contributing to Vanguard! Every contribution — whether it's code, docs, bug reports, or ideas — helps make AI-powered development accessible to everyone.

## Table of Contents

- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Project Structure](#project-structure)
- [Making Changes](#making-changes)
- [Pull Request Process](#pull-request-process)
- [Code Style](#code-style)
- [Reporting Bugs](#reporting-bugs)
- [Requesting Features](#requesting-features)

---

## Getting Started

1. **Fork** the repository on GitHub
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/vanguard.git
   cd vanguard
   ```
3. **Create a branch** for your changes:
   ```bash
   git checkout -b feat/your-feature-name
   ```

## Development Setup

### Prerequisites

- Node.js 20+ or Bun 1.1+
- Git
- A terminal you're comfortable with

### Install Dependencies

```bash
make setup
```

Or manually:

```bash
npm install
```

### Run in Development Mode

```bash
make dev
```

### Run Tests

```bash
make test
```

### Build

```bash
make build
```

## Project Structure

```
vanguard/
├── src/
│   ├── cli/          # CLI entry point and argument parsing
│   ├── core/         # Core engine — indexing, context, orchestration
│   ├── providers/    # AI provider integrations (OpenAI, Anthropic, Google, xAI, etc.)
│   ├── tools/        # File editing, testing, refactoring tools
│   └── utils/        # Shared utilities
├── tests/            # Test suites
├── docs/             # Documentation source
├── scripts/          # Build and release scripts
└── website/          # Project website (hadionlineclas.github.io/vanguard)
```

## Making Changes

1. Make sure your branch is up to date with `main`
2. Write your code and add tests
3. Ensure all tests pass: `make test`
4. Ensure the linter is happy: `make lint`
5. Commit your changes with a clear message (see below)

### Commit Message Format

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add support for xAI Grok 4.6 provider
fix: resolve context indexing issue on Windows
docs: update model list with Gemini 3.8
test: add integration tests for custom endpoints
chore: update dependencies
```

## Pull Request Process

1. Push your branch to your fork
2. Open a PR against `hadionlineclas/vanguard:main`
3. Fill out the PR template
4. Wait for CI to pass
5. A maintainer will review your PR

### PR Checklist

- [ ] Tests added/updated
- [ ] Docs updated (if applicable)
- [ ] Linter passes
- [ ] Commit messages follow Conventional Commits
- [ ] No breaking changes (or clearly documented)

## Code Style

- TypeScript with strict mode
- 2-space indentation
- No semicolons (we use the prettier default)
- Prefer `const` over `let`
- Use descriptive variable and function names
- Keep functions small and focused

Run the formatter before committing:

```bash
make format
```

## Reporting Bugs

Open an [issue](https://github.com/hadionlineclas/vanguard/issues/new?template=bug_report.md) with:

- Vanguard version (`vanguard --version`)
- OS and version
- Steps to reproduce
- Expected vs actual behavior
- Relevant logs or screenshots

## Requesting Features

Open an [issue](https://github.com/hadionlineclas/vanguard/issues/new?template=feature_request.md) with:

- A clear description of the feature
- Why it would be useful
- Any proposed implementation ideas

---

## Adding a New Provider

Want to add support for a new AI provider? Here's the quickstart:

1. Create a new file in `src/providers/`
2. Implement the `Provider` interface
3. Register it in `src/providers/index.ts`
4. Add tests in `tests/providers/`
5. Update the docs and README model tables

See existing providers (e.g., `src/providers/openai.ts`) as a reference.

---

Thank you for helping make Vanguard better for everyone!
