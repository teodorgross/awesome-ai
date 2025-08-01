---
title: "AgentGPT"
category: "Agent"
description: "Browser-based platform to assemble, configure, and deploy autonomous AI agents with goal-oriented task execution"
website: "https://github.com/reworkd/AgentGPT"
icon: "https://avatars.githubusercontent.com/u/120154269?s=48&v=4"
tags: ["autonomous-agents", "browser-based", "goal-oriented", "nextjs", "fastapi"]
pricing: "Free"
---

# AgentGPT

AgentGPT allows you to configure and deploy autonomous AI agents directly in your browser. Name your custom AI and have it embark on any goal imaginable by thinking of tasks, executing them, and learning from results.

## Key Features

**Browser-Based Deployment**: No complex setup required - run directly in web browser with automatic CLI setup bundled with the project.

**Goal-Oriented Execution**: Agents attempt to reach goals by dynamically thinking of tasks, executing them, and learning from results through iterative improvement.

**Responsive Design**: UI designed to match AgentGPT with responsive design supporting both light and dark modes across devices.

**Access Control**: Support for access code control ensuring only authorized users can utilize the deployed agents.

**Multi-API Support**: Integration with OpenAI API, Serper API for search, and Replicate API for additional capabilities.

## Technical Stack

- **Frontend**: Next.js 13 + TypeScript with TailwindCSS + HeadlessUI for styling
- **Backend**: FastAPI with SQLModel ORM and Prisma database management
- **Authentication**: Next-Auth.js for user authentication and session management
- **Database**: PlanetScale with MySQL for production deployments
- **Validation**: Zod + Pydantic for schema validation across frontend and backend
- **LLM Integration**: LangChain for comprehensive language model tooling

## Setup Options

1. **Automatic Setup**: Use bundled setup script that configures environment variables, database, backend, and frontend
2. **Manual Installation**: Clone repository, install dependencies, configure API keys, run setup scripts
3. **One-Click Deployment**: Direct deployment to cloud platforms with minimal configuration

## Requirements

- Node.js (latest LTS version)
- Git for repository management  
- Docker Desktop (recommended for containerized deployment)
- OpenAI API key (required)
- Serper API key (optional for web search)
- Replicate API token (optional for additional AI capabilities)
