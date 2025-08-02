---
title: "Nosia"
category: "Chat"
description: "Easy-to-install RAG platform that allows you to run AI models on your own private data with Ollama integration"
website: "https://github.com/nosia-ai/nosia"
icon: "https://avatars.githubusercontent.com/u/172981152?s=48&v=4"
tags: ["RAG", "private-data", "ollama", "self-hosted", "docker"]
pricing: "Free"
---

# Nosia

**Nosia** is a user-friendly platform designed to help you run AI models on your own private data through Retrieval-Augmented Generation (RAG). Built for simplicity and ease of use, Nosia provides a complete solution for creating private AI assistants that can answer questions based on your documents and knowledge base while keeping everything local and secure.

## Key Features

**Simple One-Command Installation**
- **Automated Setup**: Single command installs Docker, Ollama, and Nosia
- **Cross-Platform Support**: Works on macOS, Debian, and Ubuntu systems
- **Zero Configuration**: Get started immediately with sensible defaults
- **Local Access**: Available at `https://nosia.localhost` after installation

**Private RAG Platform**
- **Document Intelligence**: Upload and analyze your own documents and data
- **Knowledge Base**: Build comprehensive knowledge repositories from your files
- **Private Processing**: All data processing happens locally on your infrastructure
- **Secure Architecture**: No data leaves your environment during processing

**Ollama Integration**
- **Local LLM Support**: Leverages Ollama for completely private AI processing
- **Multiple Models**: Support for various models including Mistral, Qwen, and more
- **Remote Ollama**: Can connect to remote Ollama instances for distributed setups
- **Model Flexibility**: Easy switching between different language models

**OpenAI-Compatible API**
- **Standard Interface**: Provides OpenAI-compatible chat completion API
- **Easy Integration**: Use existing OpenAI client libraries and tools
- **Token Authentication**: Secure API access with user-generated tokens
- **Seamless Migration**: Drop-in replacement for OpenAI API workflows

## Technical Architecture

**Modern Tech Stack**
- **Ruby on Rails**: Robust backend framework for reliable operation
- **Docker Integration**: Containerized deployment for consistency
- **Vector Database**: Built-in vector storage for efficient document retrieval
- **Embedding Models**: Uses nomic-embed-text for document vectorization

**Default Model Configuration**
- **Completion Model**: mistral-small3.2 (high-quality, efficient responses)
- **Embeddings Model**: nomic-embed-text (required for document processing)
- **Checking Model**: bespoke-minicheck (content validation and quality)
- **Configurable**: Easy model switching through environment variables

## Installation & Setup

**One-Command Installation**
```bash
# Basic installation (local Ollama)
curl -fsSL https://raw.githubusercontent.com/nosia-ai/nosia-install/main/nosia-install.sh | sh

# Output:
# [x] Setting up environment
# [x] Setting up Docker
# [x] Setting up Ollama
# [x] Starting Ollama
# [x] Starting Nosia
# 
# You can now access Nosia at https://nosia.localhost
```

**Remote Ollama Setup**
```bash
# Connect to remote Ollama instance
curl -fsSL https://raw.githubusercontent.com/nosia-ai/nosia-install/main/nosia-install.sh \
| OLLAMA_BASE_URL=http://YOUR_OLLAMA_HOST:11434 sh
```

**Custom Model Configuration**
```bash
# Use different completion model
curl -fsSL https://raw.githubusercontent.com/nosia-ai/nosia-install/main/nosia-install.sh \
| LLM_MODEL=mistral sh
```

**Distributed Setup (Ollama Host + Nosia Client)**
```bash
# On host machine (macOS)
brew install ollama
ollama pull mistral-small3.2
ollama pull bespoke-minicheck  
ollama pull nomic-embed-text
OLLAMA_MAX_LOADED_MODELS=3 ollama serve

# On client machine (Debian/Ubuntu)
curl -fsSL https://raw.githubusercontent.com/nosia-ai/nosia-install/main/nosia-install.sh \
| OLLAMA_BASE_URL=http://HOST_IP:11434 sh
```

## Usage & Integration

**Web Interface**
- **Document Upload**: Drag and drop files for processing
- **Chat Interface**: Ask questions about your uploaded documents
- **Knowledge Management**: Organize and manage your document collections
- **Real-time Processing**: Immediate responses with document context

**API Integration**
1. **Generate API Token**: Visit `https://nosia.localhost/api_tokens` as logged-in user
2. **Copy Token**: Generate and copy your authentication token
3. **Configure Client**: Set API base to `https://nosia.localhost/v1` with your token
4. **Start Querying**: Use any OpenAI-compatible client library

**Example API Usage**
```python
import openai

client = openai.OpenAI(
    base_url="https://nosia.localhost/v1",
    api_key="your-nosia-token"
)

response = client.chat.completions.create(
    model="mistral-small3.2",
    messages=[
        {"role": "user", "content": "What does my document say about...?"}
    ]
)
```

## Use Cases

**Enterprise Knowledge Management**
- **Internal Documentation**: Create searchable knowledge bases from company documents
- **Policy Management**: Make corporate policies and procedures easily queryable
- **Training Materials**: Transform training content into interactive AI assistants
- **Institutional Knowledge**: Preserve and make accessible organizational expertise

**Research & Development**
- **Literature Review**: Analyze research papers and academic documents
- **Patent Analysis**: Search and analyze patent databases and technical documents
- **Regulatory Compliance**: Query compliance documents and regulatory requirements
- **Technical Documentation**: Make complex technical manuals conversational

**Legal & Professional Services**
- **Contract Analysis**: Query legal documents and contract terms
- **Case Research**: Search through legal precedents and case files
- **Regulatory Research**: Navigate complex regulatory frameworks
- **Due Diligence**: Analyze documents during M&A and investment processes

**Personal Productivity**
- **Document Analysis**: Get insights from personal document collections
- **Research Assistant**: Create AI assistants for personal research projects
- **Learning Aid**: Transform textbooks and learning materials into interactive tutors
- **Information Organization**: Make personal knowledge bases easily searchable

## Management & Operations

**Service Management**
```bash
# Upgrade services
./script/upgrade

# Start services
./script/start

# Stop services  
./script/stop
```

**Troubleshooting & Monitoring**
- **Installation Logs**: Check `./log/production.log` for setup issues
- **Job Monitoring**: Monitor AI processing at `http://IP:3000/jobs`
- **Service Logs**: `docker compose logs -f` for runtime issues
- **Ollama Logs**: `~/.ollama/logs/server.log` for model server issues

**Configuration Management**
- **Environment Variables**: Configure models, endpoints, and behavior
- **Database Migrations**: Handle embedding model changes and updates
- **Vector Re-indexing**: Re-process documents when changing embedding models
- **Model Management**: Easy switching between different AI models

## Advanced Configuration

**Custom Embedding Models**
```bash
# Change embedding dimensions
EMBEDDING_DIMENSIONS=new_value

# Re-run vector database migration
bin/rails db:migrate:redo:primary VERSION=20241216213448

# Re-vectorize existing documents
bin/rails c
Document.find_each(&:vectorize!)
```

**Network Configuration**
- **Port Forwarding**: Access from host machine via SSH tunneling
- **SSL Configuration**: HTTPS access with self-signed certificates
- **Multi-user Access**: Support for multiple users with individual API tokens
- **Remote Access**: Configure for team access across network

**Performance Optimization**
- **Model Loading**: Configure maximum loaded models for memory management
- **Batch Processing**: Optimize document processing for large collections
- **Vector Search**: Tune vector similarity search parameters
- **Caching**: Optimize response caching for frequently accessed content

## Privacy & Security

**Data Privacy**
- **Local Processing**: All data remains on your infrastructure
- **No External Calls**: No data sent to external AI services
- **Secure Storage**: Documents and vectors stored locally
- **Access Control**: User-based authentication and API tokens

**Security Features**
- **HTTPS by Default**: Encrypted communication to web interface
- **Token-Based Auth**: Secure API access with generated tokens
- **Isolated Environment**: Docker containerization for security
- **Local Network**: Default configuration restricts to local access

## Community & Support

**Documentation & Guides**
- **Nosia Guides**: Comprehensive documentation at guides.nosia.ai
- **Installation Videos**: Step-by-step video tutorials
- **API Documentation**: Complete API reference and examples
- **Troubleshooting**: Common issues and solutions guide

**Open Source Development**
- **MIT Licensed**: Free and open source software
- **Community Contributions**: Welcome improvements and feature requests
- **Issue Tracking**: GitHub Issues for bug reports and support
- **Active Development**: Regular updates and feature additions

Nosia represents the ideal balance between powerful AI capabilities and privacy protection, offering organizations and individuals a way to leverage advanced AI for their private data without compromising security or control. Whether you're building enterprise knowledge systems or personal AI assistants, Nosia provides the tools and simplicity needed to get started quickly while maintaining complete data sovereignty.
