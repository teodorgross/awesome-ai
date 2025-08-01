---
title: "AutoAgents"
category: "Agent"
description: "Generate different roles for GPTs to form a collaborative entity for complex tasks"
website: "https://github.com/Link-AGI/AutoAgents"
icon: "https://github.com/Link-AGI/AutoAgents/raw/main/docs/resources/logo-autoagents.jpg"
tags: ["role-generation", "collaborative", "multi-agent", "automatic", "ijcai"]
pricing: "Free"
---

# AutoAgents

Generate different roles for GPTs to form a collaborative entity for complex tasks. AutoAgents is an experimental open-source application that autonomously generates multi-agents to achieve whatever goal you set.

**Key Features:**
- **Automatic Role Generation**: AI-driven creation of expert role agents
- **Collaborative Planning**: Multi-agent coordination and task distribution
- **AgentBank**: Custom agent collection for reusable expert roles
- **Dynamic Execution**: Adaptive plan execution with real-time adjustments
- **Reflection System**: Built-in observers for quality assurance
- **Tool Integration**: Support for external tools and search capabilities

**Use Cases:**
- Complex research and analysis projects
- Rumor verification and fact-checking
- Educational content creation
- Game development and interactive applications
- Market research and competitive analysis
- Multi-perspective problem solving

**Technical Requirements:**
- Python 3.8+
- OpenAI API key
- Optional: SerpAPI key for web search
- Docker support available

**Installation:**
```bash
git clone https://github.com/LinkSoul-AI/AutoAgents
cd AutoAgents
python setup.py install

# Configure API keys in config/key.yaml
cp config/config.yaml config/key.yaml
# Edit config/key.yaml with your keys
```

**Usage:**
```bash
# Command line mode
python main.py --mode commandline \
               --llm_api_key YOUR_OPENAI_API_KEY \
               --serpapi_key YOUR_SERPAPI_KEY \
               --idea "Is LK-99 really a room temperature superconducting material?"

# WebSocket service mode
python main.py --mode service --host "127.0.0.1" --port 9000

# Docker deployment
docker build -f docker/Dockerfile -t "autoagents:1.0" .
docker run -it --rm -p 7860:7860 "autoagents:1.0"
```

**System Components:**
- **Planner**: Determines expert roles and execution plans
- **Tools**: Set of available tools (currently search-focused)
- **Observers**: Reflection mechanisms for Agents, Plans, and Actions
- **Agents**: Generated expert role agents with specialized knowledge
- **Plan**: Structured execution plan with role assignments
- **Actions**: Specific agent actions including tool calls and outputs

**Example Applications:**
- **Rumor Verification**: Multi-agent fact-checking system
- **Game Development**: Collaborative game creation (e.g., Snake game)
- **Research Analysis**: Complex topic investigation with multiple perspectives
- **Content Creation**: Collaborative writing and content development

**Research Foundation:**
- Published at IJCAI 2024
- Built on MetaGPT framework
- Active research and development community
