---
title: "Gollama"
category: "Code"
description: "Advanced TUI tool for managing Ollama models with vRAM estimation, LM Studio integration, and comprehensive model operations"
website: "https://github.com/sammcj/gollama"
icon: "https://raw.githubusercontent.com/sammcj/gollama/refs/heads/main/gollama-logo.png"
tags: ["ollama", "model-management", "TUI", "vram-estimation", "go"]
pricing: "Free"
---

# Gollama

**Gollama** is a sophisticated macOS/Linux tool that provides a comprehensive Text User Interface (TUI) for managing Ollama models. Originally starting as a rewrite of the llamalink project, it has evolved into a full-featured model management solution offering advanced capabilities like vRAM estimation, bidirectional LM Studio integration, and remote model distribution.

## Key Features

**Comprehensive Model Management**
- **Interactive TUI**: Intuitive terminal interface for all model operations
- **List & Inspect**: View detailed model metadata including size, quantization, family, and modification dates
- **Sort & Filter**: Multiple sorting options (name, size, date, quantization, family, parameters)
- **Search Functionality**: Advanced search with OR (`|`) and AND (`&`) operators
- **Bulk Operations**: Select and manage multiple models simultaneously

**Advanced Model Operations**
- **Run & Unload**: Start and stop models directly from the interface
- **Edit Modelfiles**: Modify model configurations with built-in or external editors
- **Copy & Rename**: Duplicate models with different names or configurations
- **Push to Registry**: Upload models to remote registries
- **Delete Management**: Safe model removal with confirmation

**LM Studio Integration**
- **Bidirectional Linking**: Sync models between Ollama and LM Studio
- **Automatic Modelfile Creation**: Generate LM Studio compatible configurations
- **Bulk Linking**: Link all models with a single command
- **Cross-Platform Support**: Works on macOS and Linux systems

**Revolutionary vRAM Estimation**
- **Comprehensive Analysis**: Calculate vRAM usage for Ollama and HuggingFace models
- **Context Length Optimization**: Determine maximum context for given memory constraints
- **Quantization Recommendations**: Find optimal quantization for memory/context requirements
- **Multiple Cache Options**: Support for fp16, q8_0, q4_0 K/V cache quantization
- **Hardware Detection**: Automatic CUDA vRAM detection (coming soon)

## Advanced Capabilities

**Remote Model Distribution (Spit)**
- **Model Copying**: Distribute models across multiple machines
- **Backup Creation**: Create model backups on remote hosts
- **Batch Operations**: Copy all models to remote instances
- **Network Sync**: Maintain model consistency across infrastructure

**Intelligent Search & Filtering**
```bash
# Basic search
gollama -s llama

# OR operator - match either term
gollama -s 'llama|gemma'

# AND operator - match both terms
gollama -s 'llama&instruct'
```

**Command Line Interface**
- **List Mode**: `gollama -l` for scriptable model listing
- **Edit Mode**: `gollama -e model-name` for direct Modelfile editing
- **Search Mode**: Advanced pattern matching for model discovery
- **Batch Operations**: Automate model management tasks

## Technical Architecture

**Built with Modern Go**
- **TUI Framework**: Charmbracelet Bubble Tea for interactive interface
- **Cross-Platform**: Native support for macOS and Linux
- **API Integration**: Direct Ollama API communication
- **Spitter Package**: Custom model copying functionality
- **JSON Configuration**: Flexible, user-customizable settings

**Performance Optimized**
- **Fast Startup**: Minimal resource usage for quick launches
- **Efficient Operations**: Optimized for handling large model collections
- **Memory Management**: Smart resource allocation for model operations
- **Concurrent Processing**: Parallel operations where applicable

## Installation & Setup

**Multiple Installation Methods**
```bash
# Go install (recommended)
go install github.com/sammcj/gollama@HEAD

# Binary download
# Download from releases page and extract to PATH

# Homebrew (coming soon)
brew install gollama

# Quick install script
curl -sL https://raw.githubusercontent.com/sammcj/gollama/main/scripts/install.sh | bash
```

**Configuration**
- **Location**: `~/.config/gollama/config.json`
- **Automatic Creation**: Default configuration generated on first run
- **Customizable Options**: Sorting, columns, API settings, themes
- **Editor Integration**: Support for external editors (VS Code, etc.)

## Advanced Features

**vRAM Estimation System**
```bash
# Estimate model memory usage
gollama --vram llama3.1:8b-instruct-q6_K

# Find best quantization for memory constraint
gollama --vram NousResearch/Hermes-2-Theta-Llama-3-8B --fits 6

# Context length optimization
gollama --vram model-name --context 32k
```

**Theme Customization**
- **Multiple Themes**: Default dark, light-neon, and custom themes
- **JSON Configuration**: Easy theme creation and modification
- **Color Support**: ANSI codes and hex values supported
- **Family Colors**: Different colors for model families (Llama, Alpaca, etc.)

**Hotkey Navigation**
- **Space**: Select models
- **Enter**: Run selected model
- **i**: Inspect model details
- **t**: Show running models (top)
- **D**: Delete selected models
- **e**: Edit Modelfile
- **c**: Copy model
- **p**: Pull new model
- **P**: Push model to registry
- **l/L**: Link to LM Studio (single/all)

## Use Cases

**Development & Research**
- **Model Experimentation**: Quickly switch between different models and configurations
- **Performance Analysis**: Use vRAM estimation to optimize model selection
- **Version Management**: Track model versions and modifications
- **Resource Planning**: Plan infrastructure requirements for model deployments

**Production Management**
- **Model Distribution**: Deploy models across multiple servers
- **Registry Management**: Maintain private model registries
- **Backup Solutions**: Create and manage model backups
- **Monitoring**: Track running models and resource usage

**Educational & Training**
- **Model Comparison**: Compare different quantizations and configurations
- **Learning Tool**: Understand model characteristics and requirements
- **Experimentation**: Safe environment for model testing
- **Documentation**: Track model changes and configurations

## Integration Ecosystem

**LM Studio Compatibility**
- **Seamless Sync**: Keep Ollama and LM Studio models synchronized
- **Configuration Transfer**: Automatically generate compatible Modelfiles
- **Bidirectional Support**: Import models from LM Studio to Ollama
- **Admin Privileges**: Automatic handling of Windows admin requirements

**Development Tools**
- **External Editors**: VS Code, Vim, and custom editor support
- **Logging System**: Comprehensive logging with configurable levels
- **API Integration**: Direct Ollama API communication
- **Docker Support**: Experimental container-based operations

**Extensibility**
- **Plugin Architecture**: Modular design for feature extensions
- **Configuration API**: JSON-based configuration system
- **Theme System**: Customizable visual appearance
- **Hotkey Mapping**: Configurable keyboard shortcuts

## Community & Support

**Open Source Development**
- **MIT Licensed**: Free and open source software
- **Active Development**: Regular updates and feature additions
- **Community Contributions**: Welcome pull requests and issue reports
- **Documentation**: Comprehensive guides and examples

**Related Projects**
- **Spitter**: Model copying functionality
- **Ingest**: Code-to-markdown conversion for LLMs
- **Llamalink**: Original project inspiration
- **Confuddlement**: Confluence to Markdown converter

## Advanced Configuration

**JSON Configuration Options**
```json
{
  "default_sort": "modified",
  "columns": ["Name", "Size", "Quant", "Family", "Modified", "ID"],
  "ollama_api_url": "http://localhost:11434",
  "strip_string": "my-registry.com/",
  "editor": "/usr/bin/code",
  "docker_container": "ollama-container",
  "theme": "dark-neon"
}
```

**Experimental Features**
- **Docker Integration**: Run operations inside containers
- **Custom Editors**: External editor integration for Modelfile editing
- **Registry Prefixes**: Strip common prefixes for cleaner display
- **Theme System**: Visual customization options

Gollama represents the most comprehensive tool available for Ollama model management, combining powerful features with an intuitive interface. Whether you're managing a few models for personal use or coordinating hundreds of models across an enterprise infrastructure, Gollama provides the tools and flexibility needed for efficient model lifecycle management.
