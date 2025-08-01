---
title: "ScreenPipe"
category: "Code"
description: "AI app store powered by 24/7 desktop history with screen and mic recording, 100% local and developer friendly"
website: "https://github.com/mediar-ai/screenpipe"
icon: "https://avatars.githubusercontent.com/u/179202840?s=48&v=4"
tags: ["screen-recording", "local-ai", "app-store", "automation", "privacy"]
pricing: "Free"
---

# ScreenPipe

AI app store powered by 24/7 desktop history recording. ScreenPipe continuously captures screen and microphone activity locally, indexes everything into a searchable API, and enables developers to build AI applications with full user context.

## Key Features

- **24/7 Recording**: Continuous screen and microphone capture
- **100% Local**: All processing happens on your device
- **Low Resource Usage**: 10% CPU, 4GB RAM, 15GB/month storage
- **Developer Friendly**: API and plugin system for building AI apps
- **Privacy First**: No data leaves your computer
- **Cross-Platform**: macOS, Windows, and Linux support

## Core Capabilities

### Continuous Recording
- **Screen Capture**: 24/7 screen recording with native OCR
- **Audio Recording**: Microphone input with speech-to-text
- **Efficient Storage**: Optimized compression and indexing
- **Selective Recording**: Control what gets recorded and when

### AI-Powered Indexing
- **OCR Integration**: Apple & Windows Native OCR for text extraction
- **Speech Recognition**: Convert audio to searchable text
- **Content Analysis**: AI-powered content understanding and tagging
- **Fast Search**: Instant search across all recorded content

### Plugin Ecosystem ("Pipes")
- **Next.js Integration**: Build desktop apps using web technologies
- **Sandboxed Environment**: Secure plugin execution within Rust core
- **Store Integration**: Publish and monetize plugins through the pipe store
- **Template System**: Ready-to-use templates for common use cases

## Development Platform

### Plugin Creation
```bash
# Create new plugin
bunx --bun @screenpipe/dev@latest pipe create

# Register plugin
bunx --bun @screenpipe/dev@latest pipe register --name foo [--paid --price 50]

# Publish to store
bun run build
bunx --bun @screenpipe/dev@latest pipe publish --name foo
```

### Native App Templates
- **Tauri Template**: Desktop native apps with Rust backend
- **Electron Template**: Cross-platform desktop applications
- **Next.js Integration**: Web-based plugins with native performance

### API Access
- **RESTful API**: Query recorded data programmatically
- **Real-time Streams**: Live access to ongoing recordings
- **Search Endpoints**: Full-text search across all content
- **Context Retrieval**: Get relevant context for AI applications

## Use Cases

### Productivity & Automation
- **Meeting Assistant**: Automatic meeting notes and summaries
- **Activity Tracking**: Understand how you spend your time
- **Context Recovery**: Never lose important information
- **Workflow Automation**: Automate repetitive desktop tasks

### AI Applications
- **Personal Assistant**: AI with full context of your activities
- **Content Generation**: Create content based on your screen history
- **Decision Support**: AI recommendations based on your patterns
- **Research Helper**: Find and organize information from your activities

### Business Intelligence
- **Team Productivity**: Analyze team workflow patterns
- **Training Material**: Create tutorials from recorded actions
- **Compliance**: Record activities for audit purposes
- **Knowledge Base**: Build searchable knowledge from activities

## Technical Architecture

### Core Engine
- **Rust Backend**: High-performance core for recording and indexing
- **Native OCR**: Platform-specific text recognition
- **Audio Processing**: Real-time speech-to-text conversion
- **Storage Engine**: Efficient data compression and retrieval

### Plugin System
- **Sandboxed Execution**: Secure plugin runtime environment
- **Web Technologies**: Use HTML, CSS, JavaScript for UI
- **Native Bridges**: Access to system APIs through secure bridges
- **Hot Reload**: Development-friendly plugin reloading

## Privacy & Security

### Local Processing
- **No Cloud**: All data stays on your device
- **Offline Capable**: Works without internet connection
- **Encrypted Storage**: Local data encryption
- **Permission Control**: Granular control over what gets recorded

### Data Management
- **Selective Recording**: Choose which apps and activities to record
- **Automatic Cleanup**: Configurable data retention policies
- **Export Control**: Control over data export and sharing
- **Audit Trail**: Track all access to recorded data

## Installation & Setup

### Quick Install
```bash
# macOS/Linux
curl -fsSL get.screenpi.pe/cli | sh

# Windows
iwr get.screenpi.pe/cli.ps1 | iex

# Start recording
screenpipe
```

### Permission Setup
- **macOS**: Grant screen recording and microphone permissions
- **Windows**: Configure privacy settings for screen capture
- **Linux**: Set up appropriate system permissions

## Monetization & Store

### Pipe Store
- **Developer Revenue**: Make money from published plugins
- **Subscription Model**: Recurring revenue for premium features
- **One-time Purchases**: Simple licensing for utility tools
- **Stripe Integration**: Seamless payment processing

### Available Plugins
- **Reddit Agent**: Automated Reddit interactions
- **LinkedIn Agent**: Professional networking automation
- **Timeline Tools**: Advanced timeline visualization
- **Meeting Assistant**: Enhanced meeting productivity
- **Financial Automations**: Screen-based financial tracking

## Community & Ecosystem

### Development Community
- **Open Source**: Full source code available on GitHub
- **Hackathons**: Regular community hackathons with cash prizes
- **Bounty Program**: Get paid for contributions
- **Template Gallery**: Community-contributed templates

### Partnerships
- **Different AI**: Financial automations and file organization
- **Founders Inc**: Backed by prominent investors
- **Community Projects**: Sprint.dev hackathon projects

## Performance Specifications

### Resource Usage
- **CPU**: ~10% usage during active recording
- **Memory**: ~4GB RAM for typical usage
- **Storage**: ~15GB per month of recordings
- **Battery**: Optimized for laptop usage

### Platform Support
- **macOS**: Full native support with Metal acceleration
- **Windows**: Native OCR and audio processing
- **Linux**: Complete functionality with system integration
- **Cross-Platform**: Consistent API across all platforms

## Advanced Features

### ScreenPipe Terminator
- **Desktop Automation**: Playwright-like automation for desktop
- **OS API Based**: 100x faster than vision-based automation
- **Reliable Control**: Direct system API integration
- **Developer SDK**: Easy-to-use automation framework

### Integration Options
- **Obsidian**: Drop-in replacement for Granola note-taking
- **File Organization**: AI-powered file management
- **Workflow Tools**: Integration with popular productivity apps
- **Custom Integrations**: Build your own integrations with the API

## Future Development

### Roadmap
- **Enhanced AI**: Better content understanding and analysis
- **More Platforms**: Mobile and web platform support
- **Advanced Analytics**: Deeper insights into usage patterns
- **Enterprise Features**: Team collaboration and management tools

### Community Growth
- **Developer Ecosystem**: Growing library of plugins and tools
- **Use Case Expansion**: New applications and integrations
- **Performance Improvements**: Continuous optimization
- **Security Enhancements**: Advanced privacy and security features
