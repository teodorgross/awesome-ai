---
title: "Shell GPT"
category: "Code"
description: "Command-line productivity tool powered by AI for generating shell commands, code snippets, and documentation"
website: "https://github.com/TheR1D/shell_gpt"
icon: ""
tags: ["cli", "shell", "productivity", "code-generation", "automation"]
pricing: "Free"
---

# Shell GPT

A powerful command-line productivity tool powered by AI large language models like GPT-4. Shell GPT streamlines the generation of shell commands, code snippets, and documentation, eliminating the need for external resources like Google search. Compatible with all major shells and operating systems.

## Key Features

- **Shell Command Generation**: Generate OS-specific shell commands from natural language
- **Code Generation**: Create code snippets in various programming languages
- **Interactive Execution**: Execute generated commands with confirmation prompts
- **Conversation Memory**: Maintain context across multiple interactions
- **Shell Integration**: Hotkey integration with Bash and ZSH shells
- **Function Calls**: Execute custom functions and system operations

## Installation

```bash
pip install shell-gpt
```

## Quick Start

### Basic Usage
```bash
# Set up API key (prompted on first use)
sgpt "What is the fibonacci sequence"

# Generate shell commands
sgpt --shell "find all json files in current folder"
# -> find . -type f -name "*.json"
# -> [E]xecute, [D]escribe, [A]bort: e

# Generate code
sgpt --code "solve fizz buzz problem using python"
```

### Input Methods
```bash
# Command line argument
sgpt "Generate git commit message for my changes"

# Pipe input
git diff | sgpt "Generate git commit message, for my changes"

# Analyze logs
docker logs -n 20 my_app | sgpt "check logs, find errors, provide possible solutions"

# File redirection
sgpt "summarise" < document.txt
sgpt <<< "What is the best way to learn shell redirects?"
```

## Advanced Features

### Shell Command Generation
- **OS-Aware**: Generates commands specific to your operating system
- **Context-Aware**: Understands your current shell environment
- **Interactive Mode**: Allows execution, description, or cancellation
- **Complex Operations**: Handles multi-step operations and file manipulations

```bash
# macOS system update
sgpt -s "update my system"
# -> sudo softwareupdate -i -a

# Ubuntu system update (same prompt, different OS)
sgpt -s "update my system"
# -> sudo apt update && sudo apt upgrade -y

# Docker operations
sgpt -s "start nginx container, mount ./index.html"
# -> docker run -d -p 80:80 -v $(pwd)/index.html:/usr/share/nginx/html/index.html nginx
```

### Shell Integration
- **Hotkey Support**: Ctrl+L (configurable) to invoke ShellGPT
- **Buffer Integration**: Suggestions appear directly in terminal input line
- **Immediate Editing**: Edit suggestions before execution
- **Installation**: `sgpt --install-integration`

### Code Generation
```bash
# Pure code output
sgpt --code "solve fizz buzz problem using python" > fizz_buzz.py

# Add comments to existing code
cat fizz_buzz.py | sgpt --code "Generate comments for each line of my code"

# Multiple programming languages supported
sgpt --code "HTTP server in Go"
sgpt --code "React component for user profile"
```

## Conversation Management

### Chat Sessions
```bash
# Start persistent conversation
sgpt --chat conversation_1 "please remember my favorite number: 4"
sgpt --chat conversation_1 "what would be my favorite number + 4?"

# Iterative code improvement
sgpt --chat dev_session --code "make a request to localhost using python"
sgpt --chat dev_session --code "add caching"
sgpt --chat dev_session --code "add error handling"

# Shell command evolution
sgpt --chat ops_session --shell "what is in current folder"
sgpt --chat ops_session "Sort by name"
sgpt --chat ops_session "Concatenate them using FFMPEG"
```

### REPL Mode
```bash
# Interactive REPL session
sgpt --repl temp
>>> What is REPL?
>>> How can I use Python with REPL?

# Shell REPL mode
sgpt --repl temp --shell
>>> What is in current folder?
>>> Show file sizes
>>> Sort them by file sizes
>>> e  # Execute the last command

# Code REPL mode
sgpt --repl dev --code
>>> Create a Python class for user management
>>> Add validation methods
>>> Add database integration
```

### Session Management
```bash
# List all chat sessions
sgpt --list-chats

# Show conversation history
sgpt --show-chat conversation_1

# Continue conversation in REPL
sgpt --repl conversation_1
```

## Function Calls & Custom Functions

### Built-in Functions
```bash
# Install default functions
sgpt --install-functions

# Functions are automatically used when appropriate
sgpt "What are the files in /tmp folder?"
# -> @FunctionCall execute_shell_command(shell_command="ls /tmp")

# Chain multiple function calls
sgpt "Play music and open hacker news"
# -> @FunctionCall play_music()
# -> @FunctionCall open_url(url="https://news.ycombinator.com")
```

### Custom Function Creation
Create custom functions in `~/.config/shell_gpt/functions/`:

```python
# execute_shell_command.py
import subprocess
from pydantic import Field
from instructor import OpenAISchema

class Function(OpenAISchema):
    """
    Executes a shell command and returns the output (result).
    """
    shell_command: str = Field(..., example="ls -la", description="Shell command to execute.")
    
    class Config:
        title = "execute_shell_command"
    
    @classmethod
    def execute(cls, shell_command: str) -> str:
        result = subprocess.run(shell_command.split(), capture_output=True, text=True)
        return f"Exit code: {result.returncode}, Output:\n{result.stdout}"
```

## Role System

### Custom Roles
```bash
# Create custom role
sgpt --create-role json_generator
# Enter role description: Provide only valid json as response.

# Use custom role
sgpt --role json_generator "random: user, password, email, address"
# -> {"user": "JohnDoe", "password": "p@ssw0rd", ...}

# List and manage roles
sgpt --list-roles
sgpt --show-role json_generator
```

### Built-in Roles
- **default**: General purpose responses
- **shell**: Shell command generation
- **code**: Code generation focus
- **Custom roles**: User-defined specialized roles

## Configuration

### Runtime Configuration (`~/.config/shell_gpt/.sgptrc`)
```bash
# API Configuration
OPENAI_API_KEY=your_api_key
API_BASE_URL=default
DEFAULT_MODEL=gpt-4o

# Cache Settings
CHAT_CACHE_LENGTH=100
CACHE_LENGTH=100
REQUEST_TIMEOUT=60

# UI Settings
DEFAULT_COLOR=magenta
CODE_THEME=default
DISABLE_STREAMING=false

# Function Settings
OPENAI_USE_FUNCTIONS=true
SHOW_FUNCTIONS_OUTPUT=false
```

### Local Model Support
```bash
# Use with Ollama (requires setup)
# Set USE_LITELLM=true in config
# Configure API_BASE_URL to point to local server
```

## Advanced Use Cases

### DevOps & System Administration
```bash
# System monitoring
sgpt -s "show disk usage of top 10 largest directories"
sgpt -s "kill all processes using port 8080"
sgpt -s "backup database with timestamp"

# Log analysis
journalctl -f | sgpt "monitor for errors and alert on critical issues"
```

### Development Workflow
```bash
# Git operations
git status | sgpt -s "stage only the modified files"
git log --oneline -10 | sgpt "create release notes from commits"

# Code review
git diff | sgpt --code "review this code and suggest improvements"

# Documentation
sgpt --code "generate README.md for a Python project with these features" < features.txt
```

### Data Processing
```bash
# File operations
sgpt -s "convert all PNG files to JPEG with 80% quality"
sgpt -s "merge all CSV files in current directory"

# Text processing
cat data.json | sgpt "extract email addresses and save to emails.txt"
```

## Docker Support

### Basic Usage
```bash
# Run with Docker
docker run --rm \
  --env OPENAI_API_KEY=api_key \
  --env OS_NAME=$(uname -s) \
  --env SHELL_NAME=$(echo $SHELL) \
  --volume gpt-cache:/tmp/shell_gpt \
  ghcr.io/ther1d/shell_gpt -s "update my system"

# Create alias for convenience
alias sgpt="docker run --rm --volume gpt-cache:/tmp/shell_gpt --env OPENAI_API_KEY ghcr.io/ther1d/shell_gpt"
```

### Custom Docker Build
```dockerfile
FROM python:3-slim
ENV DEFAULT_MODEL=ollama/mistral:7b-instruct-v0.2-q4_K_M
ENV API_BASE_URL=http://10.10.10.10:11434
ENV USE_LITELLM=true
WORKDIR /app
COPY . /app
RUN pip install --no-cache /app[litellm]
ENTRYPOINT ["sgpt"]
```

## Command Line Options

### Core Options
- `--model`: Specify LLM model (default: gpt-4o)
- `--temperature`: Control randomness (0.0-2.0)
- `--top-p`: Limit highest probable tokens (0.0-1.0)
- `--cache/--no-cache`: Control response caching

### Generation Modes
- `--shell/-s`: Generate shell commands
- `--code/-c`: Generate code only
- `--describe-shell/-d`: Describe shell commands
- `--interaction/--no-interaction`: Control interactive mode

### Chat & Roles
- `--chat`: Start/continue conversation with ID
- `--repl`: Start REPL session
- `--role`: Use specific role
- `--create-role`: Create new role

### Function & Integration
- `--functions/--no-functions`: Enable/disable function calls
- `--install-integration`: Install shell integration
- `--install-functions`: Install default functions

## Platform Compatibility

### Operating Systems
- **Linux**: Full support with all distributions
- **macOS**: Native support with shell integration
- **Windows**: PowerShell, CMD, and WSL support

### Shell Compatibility
- **Bash**: Full integration with hotkeys
- **Zsh**: Complete shell integration
- **Fish**: Basic compatibility
- **PowerShell**: Windows native support
- **CMD**: Windows command prompt support

## Performance & Efficiency

### Caching System
- **Request Caching**: Identical requests served from cache
- **Chat Caching**: Conversation context preserved
- **Configurable Limits**: Control cache size and duration

### Optimization Features
- **Streaming Responses**: Real-time output for long responses
- **Context Awareness**: Efficient token usage
- **Batch Processing**: Handle multiple operations efficiently
- **Local Model Support**: Reduce API costs with local models

## Use Cases & Examples

### System Administration
- Generate complex command pipelines
- Automate routine maintenance tasks
- Analyze system logs and performance
- Create backup and deployment scripts

### Software Development
- Generate boilerplate code quickly
- Debug and troubleshoot issues
- Create documentation and comments
- Convert between programming languages

### Data Analysis
- Process and transform data files
- Generate analysis scripts
- Create visualization commands
- Automate data pipeline tasks

### Learning & Exploration
- Understand complex command syntax
- Learn new programming concepts
- Explore system capabilities
- Practice with safe command generation
