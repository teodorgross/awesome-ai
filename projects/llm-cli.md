---
title: "LLM CLI"
category: "Code"
description: "Command-line tool and Python library for interacting with dozens of LLMs via APIs and local models"
website: "https://github.com/simonw/llm"
icon: ""
tags: ["cli", "python-library", "multi-llm", "embeddings", "sqlite"]
pricing: "Free"
---

# LLM CLI

A comprehensive CLI tool and Python library for interacting with Large Language Models from OpenAI, Anthropic, Google, Meta, and dozens of others. Supports both remote APIs and local models with advanced features like embeddings, structured extraction, and conversation logging.

## Key Features

- **Multi-Provider Support**: Access OpenAI, Anthropic Claude, Google Gemini, Meta Llama, and more
- **Local Model Integration**: Run models locally via plugins (Ollama, MLX, etc.)
- **SQLite Logging**: Store all prompts and responses in SQLite database
- **Embeddings Support**: Generate and store embeddings for semantic search
- **Structured Extraction**: Extract structured data from text and images
- **Tool Integration**: Grant models ability to execute custom tools
- **Plugin Ecosystem**: Extensible architecture with rich plugin system

## Installation Options

### Package Managers
```bash
# pip
pip install llm

# Homebrew
brew install llm

# pipx (isolated environment)
pipx install llm

# uv tool
uv tool install llm
```

## Quick Start Examples

### Basic Usage
```bash
# Set API key
llm keys set openai
# Paste your OpenAI API key

# Run a prompt
llm "Ten fun names for a pet pelican"

# Extract text from image
llm "extract text" -a scanned-document.jpg

# Use system prompt with file
cat myfile.py | llm -s "Explain this code"
```

### Multi-Provider Setup
```bash
# Google Gemini
llm install llm-gemini
llm keys set gemini
llm -m gemini-2.0-flash 'Tell me about Mountain View'

# Anthropic Claude
llm install llm-anthropic
llm keys set anthropic
llm -m claude-3-opus 'Facts about turnips'

# Local models via Ollama
llm install llm-ollama
ollama pull llama3.2:latest
llm -m llama3.2:latest 'What is the capital of France?'
```

## Advanced Features

### Interactive Chat
```bash
llm chat -m gpt-4.1
# Supports multi-line input, editing, and fragments
# Commands: !multi, !end, !edit, !fragment
```

### Embeddings & Semantic Search
```bash
# Generate embeddings
llm embed "Your text here"

# Create searchable collections
llm embed-multi documents/ -c my-docs

# Find similar content
llm similar "search query" -c my-docs
```

### Structured Data Extraction
```bash
# Define schema for extraction
llm "Extract names and dates" -s extraction-schema.json

# Extract from images with vision models
llm "What's in this image?" -a photo.jpg -m gpt-4-vision
```

## Plugin Ecosystem

### Official Plugins
- **llm-gemini**: Google Gemini models
- **llm-anthropic**: Anthropic Claude models
- **llm-ollama**: Local Ollama model integration
- **llm-mlx**: Apple Silicon optimized models
- **llm-clip**: Image search with CLIP embeddings

### Local Model Plugins
- **Ollama Integration**: Seamless local model hosting
- **MLX Support**: Apple Silicon optimization
- **GPT4All**: Cross-platform local models
- **Custom Models**: Plugin API for any model

## Data Management

### SQLite Integration
- **Automatic Logging**: All conversations stored in SQLite
- **Searchable History**: Full-text search across all interactions
- **Datasette Integration**: Web interface for browsing logs
- **Export Options**: JSON, CSV, and other formats

### Privacy & Security
- **Local Storage**: All data stored locally by default
- **API Key Management**: Secure key storage and rotation
- **Selective Logging**: Control what gets stored
- **Data Portability**: Easy backup and migration

## Python API

### Basic Usage
```python
import llm

# Simple prompt execution
model = llm.get_model("gpt-4o-mini")
response = model.prompt("Tell me a joke")
print(response.text())

# Async support
async def chat():
    async for chunk in model.prompt("Stream response", stream=True):
        print(chunk, end="")
```

### Advanced Features
```python
# Conversations with memory
conversation = model.conversation()
conversation.prompt("My name is Simon")
response = conversation.prompt("What's my name?")

# Custom tools
def get_weather(location):
    return f"Weather in {location}: Sunny, 22°C"

model.prompt("Weather in Paris", tools=[get_weather])
```

## Command Categories

### Core Commands
- **llm**: Main prompt execution
- **llm chat**: Interactive conversation mode
- **llm models**: List available models
- **llm keys**: API key management
- **llm logs**: View conversation history

### Advanced Commands
- **llm embed**: Generate embeddings
- **llm similar**: Semantic search
- **llm templates**: Prompt templates
- **llm schemas**: Structured extraction
- **llm tools**: Custom tool integration
- **llm fragments**: Long context management

### Plugin Management
- **llm install**: Install plugins
- **llm uninstall**: Remove plugins
- **llm plugins**: List installed plugins

## Use Cases

### Development Workflow
- **Code Explanation**: Understand complex codebases
- **Documentation**: Generate and improve documentation
- **Code Review**: Automated code analysis and suggestions
- **Debugging**: Analyze error logs and debug issues

### Data Processing
- **Text Analysis**: Process large text datasets
- **Information Extraction**: Structure unstructured data
- **Content Generation**: Create documentation and content
- **Translation**: Multi-language content processing

### Research & Analysis
- **Literature Review**: Analyze research papers
- **Data Exploration**: Understand datasets and patterns
- **Comparative Analysis**: Cross-reference multiple sources
- **Hypothesis Generation**: Brainstorm and test ideas

### Productivity
- **Meeting Notes**: Summarize and structure meetings
- **Email Processing**: Draft and analyze emails
- **Report Generation**: Create structured reports
- **Task Automation**: Automate repetitive text tasks

## Configuration & Customization

### Configuration Files
- **User Settings**: Customize default models and behavior
- **API Endpoints**: Configure custom API endpoints
- **Logging Preferences**: Control what gets logged
- **Plugin Settings**: Configure individual plugin behavior

### Templates & Aliases
- **Prompt Templates**: Reusable prompt structures
- **Command Aliases**: Custom shortcuts for common operations
- **System Prompts**: Predefined system prompts for different tasks
- **Workflow Automation**: Chain multiple operations

## Integration Capabilities

### Development Tools
- **CI/CD Integration**: Use in automated workflows
- **IDE Extensions**: Available for popular editors
- **Script Integration**: Easy integration with shell scripts
- **API Wrappers**: Use as library in larger applications

### Data Platforms
- **Datasette Integration**: Web interface for data exploration
- **SQLite Compatibility**: Works with existing SQLite tools
- **CSV/JSON Export**: Standard data format support
- **Database Connectors**: Connect to external databases

## Performance & Scalability

### Efficiency
