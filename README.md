# Rust Agent

Next Generation AI Agent Framework for Web3.

## ✨ Features

- 🐠 ReAct (Reasoning and Acting).
- 💾 Retrievable memory and document store, Create truly stateful agents with both short-term working memory for ongoing reasoning and long-term persistent memory across sessions.
- ♾️ Durable execution, Build agents that persist through failures and can run for extended periods, automatically resuming from exactly where they left off.
- 💬 Human-in-the-loop, Seamlessly incorporate human oversight by inspecting and modifying agent state at any point during execution.
- 🔗 Support for every model (Llama, Grok, OpenAI, Anthropic, Gemini, Qwen, etc.)
- 🛠️ Native MCP integration support, adapted to more tools (search, data services, etc.), as well as more clients (Telegram, X, WeChat, Discord, etc.)
- 👥 Multi-agent and group support with intuitive management.
- 📚 Easily ingest and interact with your documents.
- 📦 Just works!

## 🎯 Use Cases

- 🤖 Next Chatbots

## 🚀 Quick Start

### Prerequisites

- rustc 1.88.0
- cargo 1.88.0

Note for Windows Users: WSL 2 is required.

### Use the CLI (Recommended)

### Interact via Browser

## Git Hooks

This project uses git hooks to ensure code quality:

- pre-commit: Automatically formats staged files using Prettier before committing

To run the pre-commit hook manually:

```bash
bun run pre-commit
```

## 📂 Repository Structure

- / (Root):

- /core/: Core components of the Rust-Agent framework:

This architecture enables modular development, clear separation of concerns, and scalable feature implementation across the Rust-Agent ecosystem.

## Tauri Application CI/CD and Signing

The Rust-Agent application, built with Tauri and located in packages/app, is configured for cross-platform continuous integration and deployment. This setup automates the building and releasing of the application for various operating systems.

### Overview

The Tauri application is designed to be built for:

- Desktop: Linux, macOS, and Windows.

- Mobile: Android and iOS.

### CI/CD Workflows

Two main GitHub Actions workflows handle the CI/CD process for the Tauri application:

### Mobile Application Backend

### Application Signing (Important for Releases)

#### iOS Signing Secrets:

### Artifacts

Upon successful completion of the `tauri-release.yml` workflow (triggered by a new tag/release), all compiled application installers and mobile packages will be available as downloadable artifacts on the GitHub Releases page for that specific tag. This includes:

- Linux: `.AppImage` and `.deb` files.
- macOS: `.dmg` file.
- Windows: `.exe` NSIS installer.
- Android: `.apk` file.
- iOS: `.ipa` file.