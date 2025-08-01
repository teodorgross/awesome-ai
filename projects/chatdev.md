---
title: "ChatDev"
category: "Agent"
description: "Virtual software company with AI agents in different roles - develop custom software using natural language"
website: "https://github.com/openbmb/chatdev"
icon: "https://github.com/OpenBMB/ChatDev/raw/main/misc/logo1.png"
tags: ["software-company", "multi-agent", "roles", "development", "collaboration"]
pricing: "Free"
---

# ChatDev

ChatDev stands as a virtual software company that operates through various intelligent agents holding different roles, including Chief Executive Officer, Chief Product Officer, Chief Technology Officer, Programmer, Reviewer, Tester, and Art Designer.

**Key Features:**
- **Multi-Agent Organization**: Complete software company simulation with specialized roles
- **Natural Language Development**: Describe software requirements in plain English
- **Complete Development Lifecycle**: Design, coding, testing, and documentation
- **Specialized Seminars**: Agents collaborate through functional meetings
- **Incremental Development**: Build upon existing codebases
- **Human-Agent Interaction**: Users can participate as reviewers
- **Art Mode**: Generate images and visual elements for software
- **Git Integration**: Automatic version control management

**Use Cases:**
- Rapid software prototyping and development
- Educational software development training
- Collaborative AI development teams
- Game development (e.g., 2048, Gomoku)
- Web application creation
- Mobile app development
- Documentation generation

**Technical Requirements:**
- Python 3.9+
- OpenAI API key
- Conda environment (recommended)
- Git for version control

**Installation:**
```bash
# Clone repository
git clone https://github.com/OpenBMB/ChatDev.git

# Set up environment
conda create -n ChatDev_conda_env python=3.9 -y
conda activate ChatDev_conda_env

# Install dependencies
cd ChatDev
pip3 install -r requirements.txt

# Set API key
export OPENAI_API_KEY="your_OpenAI_API_key"
```

**Usage:**
```bash
# Basic development
python3 run.py --task "design a 2048 game" --name "2048"

# With specific configuration
python3 run.py --task "[description]" --name "[project_name]" --config "Art"

# Human interaction mode
python3 run.py --task "[description]" --config "Human"

# Incremental development
python3 run.py --config "incremental" --path "[source_code_directory]"
```

**Agent Roles:**
- **CEO**: Strategic oversight and decision making
- **CPO**: Product requirements and user experience
- **CTO**: Technical architecture and system design
- **Programmer**: Code implementation and development
- **Reviewer**: Code review and quality assurance
- **Tester**: Testing and bug identification
- **Art Designer**: Visual elements and UI design

**Advanced Features:**
- **Experiential Co-Learning**: Agents learn from previous experiences
- **MacNet Support**: Directed acyclic graphs for complex collaboration
- **Docker Support**: Safe execution environment
- **Web Visualizer**: Real-time development process visualization
