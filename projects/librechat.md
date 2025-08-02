---
title: "LibreChat"
category: "Chat"
description: "Enhanced ChatGPT clone with multi-AI provider support, agents, code interpreter, artifacts, and enterprise-grade multi-user authentication"
website: "https://www.librechat.ai"
icon: "https://raw.githubusercontent.com/danny-avila/LibreChat/refs/heads/main/client/public/assets/logo.svg"
tags: ["multi-provider", "self-hosted", "enterprise", "agents", "multimodal"]
pricing: "Free"
---

# LibreChat

LibreChat is the ultimate open-source Chat platform that combines the familiar ChatGPT interface with enhanced features and support for multiple AI providers. Designed for both individual users and enterprise deployments, it offers comprehensive customization, security, and scalability while maintaining complete control over your AI conversations.

## Key Features

- 🤖 **Universal AI Integration**: Support for 20+ AI providers including OpenAI, Anthropic, AWS Bedrock, Google Vertex AI, Azure, Groq, Mistral, OpenRouter, DeepSeek, and local models via Ollama
- 🛠️ **Advanced Agent System**: No-code custom assistants with MCP (Model Context Protocol) server integration for extensible tool capabilities
- 💻 **Secure Code Interpreter**: Sandboxed code execution in Python, Node.js, Go, C/C++, Java, PHP, Rust, and Fortran with full file handling
- 🪄 **Generative UI Artifacts**: Create React components, HTML pages, and Mermaid diagrams directly in chat conversations
- 🔍 **Intelligent Web Search**: Enhanced search with content scraping and result reranking for comprehensive information retrieval

## Enterprise-Grade Capabilities

### Multi-User Architecture
- **Secure Authentication**: OAuth2, LDAP, and email login support with role-based access control
- **User Management**: Built-in moderation tools, token spend tracking, and unlimited user support
- **Privacy Controls**: Temporary chat modes, conversation isolation, and comprehensive data export options

### Advanced Conversation Management
- **Message Branching**: Fork conversations to explore multiple discussion paths
- **Context Control**: Edit, resubmit, and continue messages with intelligent conversation threading
- **Search & Discovery**: Full-text search across all messages and conversations with Meilisearch integration
- **Preset System**: Create, save, and share custom AI configurations and switch providers mid-conversation

### Multimodal Excellence
- **File Interactions**: Upload and analyze documents, images, and multimedia content
- **Vision Capabilities**: Image analysis with Claude 3, GPT-4.5, GPT-4o, Llama-Vision, and Gemini
- **Audio Features**: Speech-to-text and text-to-speech with OpenAI, Azure, and ElevenLabs integration
- **Image Generation**: DALL-E 3/2, Stable Diffusion, Flux, and GPT-Image-1 support with editing capabilities

## Developer-Friendly Architecture

### Deployment Flexibility
- **Self-Hosting**: Complete control with Docker, Docker Compose, and Kubernetes support
- **Cloud Integration**: Deploy on AWS, Azure, GCP, or any cloud provider
- **Proxy Configuration**: Advanced routing with reverse proxy and load balancing support
- **Scalable Infrastructure**: Production-ready architecture for enterprise deployments

### Customization & Integration
- **API Compatibility**: OpenAI-compatible API endpoints for seamless integration
- **Custom Endpoints**: Connect any OpenAI-compatible service without proxies
- **Plugin Ecosystem**: Extensive plugin support including web browsing and specialized tools
- **MCP Protocol**: Universal tool integration standard for enhanced AI capabilities

## Advanced Features

### Reasoning & Analysis
- **Dynamic Reasoning UI**: Specialized interface for chain-of-thought models like DeepSeek-R1
- **Mathematical Support**: LaTeX rendering and KaTeX math notation
- **Code Highlighting**: Syntax highlighting with copy functionality for code snippets

### Collaboration & Productivity
- **Team Presets**: Share configurations across teams and organizations
- **Import/Export**: Migrate conversations from ChatGPT, Chatbot UI, and other platforms
- **Multiple Formats**: Export to screenshots, Markdown, text, and JSON
- **Bookmarking**: Save and organize important conversations

### Global Accessibility
- **20+ Languages**: Comprehensive multilingual interface including RTL language support
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Dark Mode**: Eye-strain reduction with elegant dark theme
- **Accessibility**: Full keyboard navigation and screen reader compatibility

## Use Cases

**Enterprise Teams**: Deploy secure, private Chat infrastructure with comprehensive user management, cost tracking, and compliance features. Ideal for organizations requiring data sovereignty and custom AI integrations.

**Developers**: Build and prototype AI applications with extensive API support, custom endpoints, and code execution capabilities. Perfect for integrating AI into existing workflows and applications.

**Researchers**: Leverage multiple AI models simultaneously for comparative analysis, with advanced conversation branching and context management for complex research workflows.

**Educational Institutions**: Provide students and faculty with unrestricted access to diverse AI models while maintaining security, user management, and content moderation.

## Getting Started

### Quick Deployment
1. **Docker Setup**: Single command deployment with Docker Compose
2. **Configuration**: Simple YAML-based configuration for all AI providers
3. **Authentication**: Set up OAuth2, LDAP, or email-based user authentication
4. **Customization**: Configure UI themes, language preferences, and feature sets

### Production Deployment
- **Load Balancing**: Multi-instance deployment with session persistence
- **Database Options**: PostgreSQL, MongoDB, or MySQL support
- **Monitoring**: Comprehensive logging and analytics integration
- **Backup & Recovery**: Automated data backup and disaster recovery options

LibreChat represents the future of open-source AI platforms, combining the best aspects of commercial AI services with the freedom, security, and customization that only open-source solutions can provide. Whether you're an individual user seeking privacy, a developer building AI applications, or an enterprise requiring robust AI infrastructure, LibreChat delivers unmatched flexibility and capability.
