---
title: "MemGPT (Letta)"
category: "Agent"
description: "Stateful agents framework with memory, reasoning, and transparent long-term memory management"
website: "https://github.com/cpacker/MemGPT"
icon: "https://avatars.githubusercontent.com/u/177780362?s=48&v=4"
tags: ["memory", "stateful", "reasoning", "context-management", "persistent"]
pricing: "Freemium"
---

# MemGPT (Letta)

Letta (formerly MemGPT) is an open source framework for building stateful agents with advanced reasoning capabilities and transparent long-term memory. The framework is white box and model-agnostic.

**Key Features:**
- **Long-term Memory**: Persistent memory across conversations and sessions
- **Memory Management**: Intelligent memory tier management (vector DBs, SQL, documents)
- **Context Extension**: Extended context beyond LLM limitations
- **Model Agnostic**: Works with OpenAI, Anthropic, vLLM, Ollama, and local models
- **REST API**: Full API access with Python/TypeScript SDKs
- **Agent Development Environment**: Graphical interface for agent management
- **Database Persistence**: PostgreSQL support for production use

**Use Cases:**
- Long-term conversational AI assistants
- Research and knowledge management systems
- Personal AI companions with memory
- Customer service with context retention
- Educational tutoring with progress tracking
- Complex multi-session task completion

**Technical Requirements:**
- Python 3.9+
- Docker (recommended) or pip installation
- PostgreSQL (production) or SQLite (development)
- LLM API access (OpenAI, Anthropic, etc.)

**Installation:**
```bash
# Docker (recommended)
docker run \
  -v ~/.letta/.persist/pgdata:/var/lib/postgresql/data \
  -p 8283:8283 \
  -e OPENAI_API_KEY="your_key" \
  letta/letta:latest

# Pip installation
pip install -U letta
export OPENAI_API_KEY=sk-...
letta server
```

**Usage:**
```bash
# CLI interaction
letta run

# Start API server
letta server

# Access web interface at http://localhost:8283
# Connect to ADE at https://app.letta.com
```

**Agent Development Environment (ADE):**
- Web-based graphical interface
- Agent creation, testing, and debugging
- Real-time conversation monitoring
- Local and cloud server connectivity
- Visual agent workflow management

**Memory Architecture:**
- **Core Memory**: Essential persistent information
- **Archival Memory**: Long-term storage with search
- **Conversation History**: Recent interaction context
- **Memory Search**: Semantic and date-based retrieval

**Enterprise Features:**
- Password-protected servers
- Multi-user support
- Advanced observability
- Production-ready deployment
