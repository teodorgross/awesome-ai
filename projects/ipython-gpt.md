---
title: "IPython-GPT"
category: "Code"
description: "ChatGPT integration for Jupyter Notebooks and IPython Shell with conversation context and data science focus"
website: "https://github.com/santiagobasulto/ipython-gpt"
icon: ""
tags: ["jupyter", "ipython", "chatgpt", "data-science", "notebook"]
pricing: "Free"
---

# IPython-GPT

A standalone ChatGPT integration extension for Jupyter Notebooks and IPython Shell that allows direct interaction with OpenAI's GPT models from within your development environment.

## Key Features

**Seamless Integration**
- Direct ChatGPT access from Jupyter Notebooks
- IPython shell compatibility
- No external dependencies required
- Magic command interface (`%%chat`)

**Conversation Management**
- Preserves conversation context like ChatGPT
- Reset conversation functionality
- Configurable system messages
- Chat history tracking

**Data Science Focus**
- Default role: "Python data science coding assistant"
- Specialized for data science workflows
- Code generation and debugging assistance
- Pandas and scientific computing support

**Flexible Configuration**
- Multiple API key setup methods
- Model selection (gpt-3.5-turbo, etc.)
- Temperature and token limits control
- Custom system messages

## Technical Specifications

- **Platform**: Jupyter Notebooks, IPython Shell, Google Colab
- **Installation**: pip install ipython-gpt
- **API**: OpenChatGPT API
- **Requirements**: OpenAI API key
- **Magic Commands**: `%%chat`, `%chat_config`, `%chat_models`, `%chat_help`

## Usage Examples

**Basic Chat**
```python
%load_ext ipython_gpt
%%chat --max-tokens=25
What's the purpose of life?
```

**Data Science Assistance**
```python
%%chat --reset-conversation
How can I avoid pandas using scientific notation in outputs globally?
```

**Custom System Message**
```python
%%chat --system-message="You're an R Data Science assistant"
Your message...
```

## Configuration Options

**Environment Variables**
- `OPENAI_API_KEY`: Primary method for API key setup

**Magic Commands**
- `%chat_config`: Set default configuration
- `%chat_models`: List available models
- `%chat_help`: Display usage information
- `%reload_ext ipython_gpt`: Reload extension

**Parameters**
- `--reset-conversation`: Start fresh conversation
- `--system-message`: Custom assistant role
- `--model`: Choose GPT model
- `--temperature`: Control response randomness
- `--max-tokens`: Limit response length

## Use Cases

- Interactive data science assistance
- Code debugging and optimization
- Pandas operations and data manipulation
- Statistical analysis guidance
- Machine learning implementation help
- Quick coding questions during development
- Educational data science learning

## Setup Instructions

1. Install via pip: `pip install ipython-gpt`
2. Get OpenAI API key from platform.openai.com
3. Set environment variable: `OPENAI_API_KEY=your-key`
4. Load extension: `%load_ext ipython_gpt`
5. Start chatting: `%%chat Your question here`

## Development Status

This is an early-stage project with active development planned. The author has noted areas for improvement in code quality and additional functionality development.
