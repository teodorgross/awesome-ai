---
title: "OpenHands"
category: "Code"
description: "An AI-powered platform for software development agents that can modify code, run commands, browse the web, call APIs, and perform any task a human developer can do."
website: "https://github.com/All-Hands-AI/OpenHands"
icon: "https://raw.githubusercontent.com/All-Hands-AI/OpenHands/refs/heads/main/docs/static/img/logo.png"
tags: ["ai-agents", "software-development", "code-automation", "developer-tools", "ai-coding"]
pricing: "Freemium"
---

# OpenHands

OpenHands (formerly OpenDevin) is a revolutionary AI-powered platform for software development agents that can perform any task a human developer can do. The platform enables AI agents to modify code, run commands, browse the web, call APIs, and even copy code snippets from StackOverflow, making it a comprehensive solution for automated software development.

## Key Features

**Comprehensive Development Capabilities**
AI agents can perform the full spectrum of development tasks including code modification, command execution, web browsing, API calls, and research - essentially anything a human developer can do.

**Multiple Deployment Options**
Available both as a cloud service (OpenHands Cloud) and for local deployment using Docker, providing flexibility for different use cases and security requirements.

**LLM Provider Flexibility**
Supports multiple large language model providers with Anthropic's Claude Sonnet 4 recommended for optimal performance, but offering many alternatives.

**Advanced Integration Features**
Connects to local filesystem, supports headless mode for scripting, offers CLI interaction, and includes GitHub Action integration for automated issue handling.

## Target Users

**Primary Users**
- Software developers seeking AI-powered coding assistance
- Development teams looking to automate routine tasks
- Individual programmers wanting to accelerate development workflows
- Startups and companies needing rapid prototyping capabilities

**Secondary Users**
- DevOps engineers automating deployment processes
- Technical leads managing development workflows
- Open source maintainers handling issue management
- Educational institutions teaching software development

## Use Cases

- Automated code generation and modification
- Bug fixing and code refactoring assistance
- API integration and testing automation
- Documentation generation and maintenance
- GitHub issue resolution and management

## Key Benefits

**Complete Development Automation**
Provides end-to-end development capabilities that mirror human developer workflows without requiring manual intervention.

**Flexible Deployment**
Offers both cloud and local deployment options to meet different security, privacy, and performance requirements.

**Research and Development Integration**
Can browse the web and access external resources, enabling comprehensive research-driven development.

**Workflow Integration**
Seamlessly integrates with existing development workflows through GitHub Actions, CLI tools, and API access.

## Deployment Options

**OpenHands Cloud**
- Managed cloud service with $20 in free credits for new users
- No local setup required
- Immediate access to full capabilities
- Commercial features and priority support available

**Local Docker Deployment**
- Complete local control and privacy
- Docker-based installation and management
- Customizable security configurations
- Filesystem integration capabilities

**Enterprise Solutions**
- Source-available commercially-licensed Helm Chart for multi-tenant deployments
- Design Partner program for commercial users
- Advanced security and scalability features

## Technical Architecture

**Container-Based Runtime**
Uses Docker containers for isolated and secure execution environments with comprehensive sandboxing.

**Multi-Modal Agent Capabilities**
- Code analysis and modification
- Command line interface interaction
- Web browsing and research
- API integration and testing
- File system manipulation

**LLM Integration**
- Support for multiple LLM providers
- Optimized for Claude Sonnet 4
- Flexible API key management
- Provider-specific optimizations

## Advanced Features

**Headless Mode**
Scriptable operation mode for automated workflows and batch processing without user interface.

**CLI Interface**
Command-line interface for power users and integration with existing development toolchains.

**GitHub Integration**
Native GitHub Action support for automated issue handling and repository management.

**Filesystem Connectivity**
Direct connection to local filesystem for seamless file manipulation and project management.

## Security Considerations

**Single-User Architecture**
Designed for individual developer use on local workstations with no built-in multi-tenant support.

**Hardened Installation Options**
Provides security guides for public network deployments with network binding restrictions and additional security measures.

**Docker Isolation**
Uses containerization for secure execution environments and resource isolation.

## Community and Support

**Open Source Community**
- Active Slack workspace for research and development discussions
- Discord server for community support and feedback
- GitHub Issues for bug reports and feature requests

**Documentation and Resources**
- Comprehensive documentation at docs.all-hands.dev
- Troubleshooting guides and setup instructions
- LLM provider configuration guides

**Development Participation**
- MIT License for open contribution
- Community-driven development process
- Monthly roadmap updates and maintainer meetings

## Getting Started

**Quick Start with Cloud**
1. Sign up at app.all-hands.dev
2. Receive $20 in free credits
3. Choose LLM provider and add API key
4. Start developing with AI assistance

**Local Installation**
```bash
docker pull docker.all-hands.dev/all-hands-ai/runtime:0.50-nikolaik
docker run -it --rm --pull=always \
-e SANDBOX_RUNTIME_CONTAINER_IMAGE=docker.all-hands.dev/all-hands-ai/runtime:0.50-nikolaik \
-v /var/run/docker.sock:/var/run/docker.sock \
-p 3000:3000 \
docker.all-hands.dev/all-hands-ai/openhands:0.50
```

## Pricing

**Cloud Service**: Freemium model with $20 free credits for new users, then usage-based pricing
**Local Deployment**: Free and open-source under MIT License
**Enterprise**: Commercial licensing available for multi-tenant and advanced enterprise features
