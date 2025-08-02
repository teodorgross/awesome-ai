---
title: "AIChat"
category: "Chat"
description: "All-in-one LLM CLI tool with Shell Assistant, Chat-REPL, RAG, AI Tools & Agents supporting 20+ providers"
website: "https://github.com/sigoden/aichat"
icon: ""
tags: ["cli", "repl", "rag", "agents", "multi-provider"]
pricing: "Free"
---

# AIChat

A comprehensive all-in-one LLM CLI tool built in Rust, featuring Shell Assistant, Chat-REPL, RAG, AI Tools & Agents, and built-in HTTP server. AIChat provides a unified interface to over 20 leading LLM providers with advanced features for productivity and automation.

## Key Features

- **20+ LLM Providers**: Unified interface to major AI services
- **Shell Assistant**: Natural language to shell command conversion
- **Interactive REPL**: Feature-rich chat interface with autocompletion
- **RAG Integration**: Document-aware conversations
- **AI Tools & Agents**: Function calling and external tool integration
- **Built-in HTTP Server**: API endpoints and web interfaces

## Installation Options

### Package Managers
```bash
# Rust developers
cargo install aichat

# Homebrew/Linuxbrew
brew install aichat

# Arch Linux
pacman -S aichat

# Windows Scoop
scoop install aichat

# Android Termux
pkg install aichat
```

### Binary Downloads
Download pre-built binaries for macOS, Linux, and Windows from GitHub Releases.

## Supported LLM Providers

### Major API Providers
- **OpenAI**: GPT models including GPT-4o, o1, and more
- **Anthropic Claude**: Claude 3 family models
- **Google**: Gemini models via Google AI Studio
- **Groq**: High-speed inference for supported models
- **Azure OpenAI**: Enterprise OpenAI deployment
- **AWS Bedrock**: Amazon's managed AI service

### Specialized Providers
- **Ollama**: Local model hosting and management
- **GitHub Models**: GitHub's model marketplace
- **Mistral**: European AI company's models
- **DeepSeek**: Advanced reasoning models
- **XAI Grok**: Elon Musk's AI assistant
- **Cohere**: Enterprise NLP platform
- **Perplexity**: Search-augmented AI

### Regional & Emerging
- **Ernie (Baidu)**: Chinese language models
- **Qianwen (Alibaba)**: Multilingual capabilities
- **Moonshot**: Long context models
- **ZhipuAI**: GLM model family
- **MiniMax**: Conversational AI
- **Deepinfra**: Cost-effective model hosting

## Command Line Interface

### Basic Usage
```bash
# Simple prompt
aichat "Hello, how are you?"

# File input
aichat -f image.png "Describe this image"
aichat -f data.txt "Summarize this document"

# Directory analysis
aichat -f src/ "Explain this codebase structure"

# Remote URLs
aichat -f https://example.com "Analyze this webpage"

# Combined inputs
aichat -f dir/ -f data.txt "Compare the code with documentation"
```

### Shell Assistant
```bash
# Natural language to shell commands
aichat --shell "find all Python files larger than 1MB"
aichat --shell "compress all images in current directory"
aichat --shell "show disk usage of largest directories"

# OS and shell aware
# Automatically adapts to your operating system and shell environment
```

## Interactive REPL Mode

### Advanced Features
- **Tab Autocompletion**: Command and parameter completion
- **Multi-line Input**: Support for complex prompts
- **History Search**: Navigate through command history
- **Configurable Keybindings**: Customize keyboard shortcuts
- **Custom Prompts**: Personalize REPL appearance

### REPL Commands
```bash
# Start REPL
aichat

# REPL-specific commands
.file image.png data.txt    # Load files
.file dir/                  # Load directory
.file `git diff`           # Execute command and use output
.file %%                   # Use last reply as input
```

## Roles & Customization

### Custom Roles
- **Tailored Behavior**: Customize LLM responses for specific tasks
- **Prompt Templates**: Predefined interaction patterns
- **Model Configuration**: Role-specific model settings
- **Productivity Enhancement**: Streamline repetitive tasks

### Role Examples
```bash
# Create role for code review
aichat --role code-reviewer "Review this Python function"

# Technical documentation role
aichat --role tech-writer "Document this API endpoint"

# Data analysis role
aichat --role data-analyst "Analyze this CSV dataset"
```

## Session Management

### Context-Aware Conversations
- **Persistent Memory**: Maintain conversation context
- **Session Continuity**: Resume conversations across sessions
- **Multi-turn Dialogues**: Complex, contextual interactions
- **Session Organization**: Manage multiple conversation threads

### Session Operations
```bash
# Start named session
aichat --session project-planning "Let's plan our next feature"

# Continue session
aichat --session project-planning "What were we discussing?"

# List sessions
aichat --list-sessions
```

## RAG (Retrieval-Augmented Generation)

### Document Integration
- **External Documents**: Integrate PDFs, text files, web pages
- **Contextual Responses**: More accurate, document-aware answers
- **Multiple Sources**: Combine information from various documents
- **Real-time Updates**: Dynamic document loading and processing

### RAG Workflow
```bash
# Load documents into conversation
aichat -f manual.pdf -f wiki.md "Explain the installation process"

# Directory-based RAG
aichat -f docs/ "What are the best practices mentioned?"

# Remote document integration
aichat -f https://api-docs.com "How do I authenticate?"
```

## Function Calling & Tools

### AI Tools Integration
- **External Tool Access**: Connect LLMs to external systems
- **Task Automation**: Automate complex workflows
- **Data Retrieval**: Access live data and APIs
- **Action Execution**: Perform actions based on AI decisions

### LLM Functions Repository
Dedicated repository at `github.com/sigoden/llm-functions` provides:
- Pre-built functions for common tasks
- Custom function development guides
- Community-contributed tools
- Integration examples

## AI Agents

### Agent Architecture
**AI Agent = Instructions (Prompt) + Tools (Function Calls) + Documents (RAG)**

### Agent Capabilities
- **Autonomous Task Execution**: Independent problem-solving
- **Multi-step Workflows**: Complex task decomposition
- **Tool Orchestration**: Coordinate multiple external tools
- **Decision Making**: Intelligent action selection

## Built-in HTTP Server

### Server Features
```bash
# Start HTTP server
aichat --serve
```

### Available Endpoints
- **Chat Completions API**: `http://127.0.0.1:8000/v1/chat/completions`
- **Embeddings API**: `http://127.0.0.1:8000/v1/embeddings`
- **Rerank API**: `http://127.0.0.1:8000/v1/rerank`
- **LLM Playground**: `http://127.0.0.1:8000/playground`
- **LLM Arena**: `http://127.0.0.1:8000/arena?num=2`

### API Usage
```bash
# Test with curl
curl -X POST -H "Content-Type: application/json" -d '{
  "model":"claude:claude-3-5-sonnet-20240620",
  "messages":[{"role":"user","content":"hello"}],
  "stream":true
}' http://127.0.0.1:8000/v1/chat/completions
```

## Web Interfaces

### LLM Playground
- **Interactive Testing**: Test different models and parameters
- **Prompt Experimentation**: Refine prompts in real-time
- **Model Comparison**: Compare responses across providers
- **Parameter Tuning**: Adjust temperature, top-p, and other settings

### LLM Arena
- **Side-by-Side Comparison**: Compare multiple LLMs simultaneously
- **Blind Testing**: Unbiased model evaluation
- **Performance Analysis**: Evaluate model strengths and weaknesses
- **Benchmarking**: Systematic model comparison

## Macro System

### Automation Features
- **Command Sequences**: Combine multiple REPL commands
- **Repetitive Task Automation**: Streamline common workflows
- **Custom Scripts**: Create reusable automation scripts
- **Workflow Optimization**: Reduce manual intervention

### Macro Examples
```bash
# Create macro for code review workflow
.macro code-review ".file %1 -- Review this code for bugs and improvements"

# Data analysis macro
.macro analyze-data ".file %1 -- Analyze this dataset and provide insights"
```

## Customization Options

### Themes & Appearance
- **Dark and Light Themes**: Customizable color schemes
- **Syntax Highlighting**: Enhanced code block rendering
- **Response Formatting**: Structured output presentation
- **Custom Styling**: Personalized interface appearance

### Configuration
- **Environment Variables**: Flexible configuration options
- **Config Files**: Persistent settings management
- **Custom Keybindings**: Personalized keyboard shortcuts
- **REPL Customization**: Tailored interactive experience

## Advanced Input Handling

### Input Sources
| Input Type | CMD Mode | REPL Mode |
|------------|----------|-----------|
| Direct | `aichat hello` | `hello` |
| STDIN | `cat data.txt | aichat` | Pipe support |
| Files | `aichat -f file.txt` | `.file file.txt` |
| Directories | `aichat -f dir/` | `.file dir/` |
| URLs | `aichat -f https://url` | `.file https://url` |
| Commands | `aichat -f '`cmd`'` | `.file `cmd`` |

### Flexible Data Handling
- **Multiple Formats**: Text, images, documents, URLs
- **Command Output**: Use shell command output as input
- **Batch Processing**: Handle multiple files simultaneously
- **Real-time Streaming**: Process data as it arrives

## Use Cases

### Development Workflow
- **Code Review**: Automated code analysis and suggestions
- **Documentation**: Generate and maintain project documentation
- **Debugging**: Analyze error logs and suggest solutions
- **API Testing**: Test and validate API endpoints

### System Administration
- **Command Generation**: Natural language to shell commands
- **Log Analysis**: Automated log parsing and issue identification
- **Automation Scripts**: Generate maintenance and deployment scripts
- **Performance Monitoring**: Analyze system metrics and performance

### Content & Research
- **Document Analysis**: Process and summarize large documents
- **Research Assistance**: Gather and synthesize information
- **Content Creation**: Generate articles, reports, and presentations
- **Data Analysis**: Process and interpret datasets

## Performance & Architecture

### Rust Foundation
- **High Performance**: Fast execution and low resource usage
- **Memory Safety**: Reliable operation without crashes
- **Concurrent Processing**: Efficient handling of multiple operations
- **Cross-Platform**: Consistent behavior across operating systems

### Scalability Features
- **Streaming Responses**: Real-time output for long responses
- **Efficient Caching**: Reduce API calls and improve response times
- **Batch Operations**: Process multiple requests efficiently
- **Resource Management**: Optimal memory and CPU usage

## Documentation & Support

### Comprehensive Guides
- **Chat-REPL Guide**: Interactive mode documentation
- **Command-Line Guide**: CLI usage and examples
- **Role Guide**: Custom role creation and management
- **RAG Guide**: Document integration and retrieval
- **Configuration Guide**: Setup and customization options

### Community Resources
- **Wiki Documentation**: Detailed feature explanations
- **FAQ Section**: Common questions and solutions
- **GitHub Issues**: Bug reports and feature requests
- **Community Contributions**: User-generated content and tools
