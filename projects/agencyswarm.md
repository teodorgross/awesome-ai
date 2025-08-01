---
title: "Agency Swarm"
category: "Agent"
description: "Agent orchestration framework for creating collaborative swarms with distinct roles and capabilities"
website: "https://github.com/VRSEN/agency-swarm"
icon: "https://camo.githubusercontent.com/2c692ca284211e0f1c9d6429752240810b349046cdde9d06f28a4af0302a9302/68747470733a2f2f666972656261736573746f726167652e676f6f676c65617069732e636f6d2f76302f622f767273656e2d61692f6f2f7075626c69632532466769746875622532464c4f474f5f42475f6c617267655f626f6c645f736861646f772532302831292e6a70673f616c743d6d6564696126746f6b656e3d38633638313333312d326137612d346136392d623231622d336162316639626631613233"
tags: ["orchestration", "collaborative", "roles", "openai-assistants", "production"]
pricing: "Free"
---

# Agency Swarm

Agent orchestration framework enabling the creation of a collaborative swarm of agents (Agencies), each with distinct roles and capabilities. Built on top of OpenAI Assistants API for reliability and production readiness.

**Key Features:**
- **Customizable Agent Roles**: Define CEO, developer, assistant roles with specialized functions
- **Full Prompt Control**: Complete customization without pre-defined restrictions
- **Type-Safe Tools**: Automatic validation and error correction
- **Efficient Communication**: Specialized messaging between agents
- **State Management**: Persistent assistant state on OpenAI platform
- **Production Ready**: Built for reliability and easy deployment

**Use Cases:**
- AI agency automation and management
- Software development teams with specialized roles
- Customer service orchestration
- Content creation workflows
- Business process automation
- Educational system management

**Technical Requirements:**
- Python 3.8+
- OpenAI API key with Assistants API access
- Pydantic for type validation

**Installation:**
```bash
pip install -U agency-swarm

# Set OpenAI key
from agency_swarm import set_openai_key
set_openai_key("YOUR_API_KEY")
```

**Basic Usage:**
```python
from agency_swarm import Agent, Agency

# Define agents with roles
ceo = Agent(
    name="CEO",
    description="Responsible for client communication, task planning and management.",
    instructions="You must converse with other agents to ensure complete task execution.",
    tools=[MyCustomTool],
    temperature=0.3
)

# Create agency with communication flows
agency = Agency([
    ceo,  # Entry point for user communication
    [ceo, dev],  # CEO can initiate communication with Developer
    [ceo, va],   # CEO can initiate communication with Virtual Assistant
    [dev, va]    # Developer can initiate communication with Virtual Assistant
])

# Run the agency
agency.demo_gradio()  # Web interface
agency.run_demo()     # Terminal version
completion = agency.get_completion("Create a website for our client")
```

**Tool Creation:**
```python
from agency_swarm.tools import BaseTool
from pydantic import Field

class MyCustomTool(BaseTool):
    """
    A custom tool for specific functionality.
    Clear description helps agents determine when to use this tool.
    """
    example_field: str = Field(
        ..., description="Description of the field for the Agent"
    )
    
    def run(self):
        # Tool implementation
        return f"Result: {self.example_field}"
```

**CLI Commands:**
```bash
# Start genesis agency for creating new agencies
agency-swarm genesis --openai_key "YOUR_API_KEY"

# Import existing agents
agency-swarm import-agent --name "Devid" --destination "./"

# Create agent template
agency-swarm create-agent-template --name "AgentName" --description "Agent Description"
```

**Communication Flows:**
- **Directional**: Communication flows from left to right in agency chart
- **Hierarchical**: Clear authority and responsibility chains
- **Collaborative**: Agents can work together on complex tasks
- **Efficient**: Optimized message routing between relevant agents

**Available Pre-built Agents:**
- **Devid**: Software Developer agent
- **BrowsingAgent**: Web browsing and research agent

**Agent Structure:**
```
AgentName/
├── files/              # Files uploaded to OpenAI
├── schemas/            # OpenAPI schemas for tool conversion
├── tools/              # Custom tools directory
├── AgentName.py        # Main agent class
├── instructions.md     # Agent instructions
└── tools.py           # Agent-specific tools
```

**Advanced Features:**
- **OpenAPI Schema Integration**: Convert API schemas to tools automatically
- **File Management**: Upload and manage agent-specific files
- **Shared Instructions**: Agency-wide guidelines and principles
- **Temperature Control**: Fine-tune agent response creativity
- **Token Management**: Control conversation history length

**Production Deployment:**
- Built on reliable OpenAI Assistants API
- State persistence and management
- Error handling and recovery
- Scalable architecture
- Professional consulting available
