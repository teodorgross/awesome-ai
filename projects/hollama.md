---
title: "Hollama"
category: "Chat"
description: "Minimal LLM chat app that runs entirely in your browser with support for Ollama & OpenAI servers, vision models, and reasoning"
website: "https://github.com/fmaclen/hollama"
icon: ""
tags: ["ollama", "openai", "browser", "minimal", "vision-models"]
pricing: "Free"
---

# Hollama

Hollama is a minimal LLM chat application that runs entirely in your browser, offering a clean and efficient interface for interacting with both Ollama and OpenAI servers. Built with SvelteKit, it provides a lightweight yet feature-rich experience for AI conversations without requiring complex installations or cloud dependencies.

## Key Features

- 🌐 **Browser-Based**: Runs completely in your web browser - no installation required
- 🤖 **Multi-Server Support**: Compatible with both Ollama and OpenAI servers
- 👁️ **Vision Models**: Support for text and vision models including image analysis capabilities
- 🧠 **Reasoning Models**: Advanced support for reasoning models with visible reasoning chains
- 📝 **Rich Text Support**: Markdown rendering with syntax highlighting and KaTeX math notation
- 💾 **Local Data Storage**: All conversations stored locally in your browser for privacy
- 🎨 **Customizable Interface**: Light and dark themes with responsive design

## Advanced Capabilities

### Enhanced Editor Features
- Large prompt fields for complex queries
- Code editor functionality with syntax highlighting
- Copy code snippets, messages, or entire sessions
- Edit and retry messages for iterative conversations

### Model Management
- Download Ollama models directly from the UI
- Customizable system prompts and advanced Ollama parameters
- Multi-language interface support
- Import and export stored conversation data

### Privacy & Control
- No sign-up required for immediate use
- All processing happens locally or on your specified servers
- Complete data ownership with browser-based storage
- Self-hosting options available with Docker

## Use Cases

**Developers**: Perfect for testing and experimenting with local LLM models through Ollama while maintaining full control over data and processing. The browser-based approach eliminates deployment complexities.

**Privacy-Conscious Users**: Ideal for those who want AI assistance without sending data to external services. Run your own models locally and interact through a polished web interface.

**Researchers & Students**: Excellent for exploring different AI models, comparing responses, and experimenting with prompts in a clean, distraction-free environment.

**Teams**: Self-host for team collaboration while keeping sensitive conversations within your infrastructure.

## Technical Architecture

- **Frontend**: SvelteKit-based static site generation
- **Backend Compatibility**: Ollama API and OpenAI API compatible
- **Storage**: Browser localStorage for conversation persistence
- **Deployment**: Static hosting, Docker containers, or local development server
- **Models**: Support for text, vision, and reasoning model types

## Getting Started

### Live Demo
- Visit the live demo at [hollama.fernando.is](https://hollama.fernando.is)
- No registration required - start chatting immediately
- Connect to your local Ollama server or OpenAI API

### Desktop Applications
- Download native apps for macOS, Windows, and Linux
- Get the latest releases from the GitHub repository
- Enjoy native performance with the same browser-based features

### Self-Hosting
- Deploy using Docker for team or personal use
- Customize the interface and configuration
- Maintain complete control over your Chat environment

### Local Development
- Clone the repository and run with standard web development tools
- Built with modern web technologies for easy customization
- Contribute to the open-source project

Hollama strikes the perfect balance between simplicity and functionality, offering a premium Chat experience while respecting user privacy and maintaining complete transparency through its open-source nature.
