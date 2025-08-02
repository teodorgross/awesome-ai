---
title: "Discord AI Bot"
category: "Chat"
description: "Discord chatbot integrating Ollama LLMs and Stable Diffusion for text generation and image creation in Discord servers"
website: "https://github.com/238SAMIxD/discord-ai-bot"
icon: ""
tags: ["discord-bot", "ollama", "discord", "chatbot", "self-hosted"]
pricing: "Free"
---

# Discord AI Bot

**Discord AI Bot** is an open-source chatbot that seamlessly integrates Ollama's local language models with AUTOMATIC1111's Stable Diffusion to provide both conversational AI and image generation capabilities directly within Discord servers. Currently in maintenance mode with a TypeScript rewrite in progress, this project offers a self-hosted solution for communities wanting AI-powered interactions.

## Key Features

**Dual AI Capabilities**
- **Text Generation**: Powered by Ollama with support for multiple local LLM models (Llama2, Orca, Mistral, etc.)
- **Image Generation**: Integration with AUTOMATIC1111 Stable Diffusion WebUI for AI-generated artwork
- **Local Processing**: All AI operations run locally, ensuring privacy and control
- **No API Costs**: Completely self-hosted solution without recurring API fees

**Discord Integration**
- **Mention-Based Interaction**: Users interact with the bot by @mentioning it
- **Channel-Specific Operation**: Configurable to work in specific Discord channels
- **Message History**: Reads message history for context-aware conversations
- **User Recognition**: Handles user mentions and replaces them with usernames for better context

**Multi-Server Support**
- **Multiple Ollama Instances**: Can connect to multiple Ollama servers simultaneously
- **Load Distribution**: Separate URLs with commas for distributed processing
- **Scalable Architecture**: Designed to handle multiple Discord servers and channels
- **Flexible Configuration**: Easy setup for different deployment scenarios

## Technical Architecture

**Core Components**
- **Node.js Backend**: Built with modern JavaScript (v14+ required)
- **Discord.js Integration**: Full Discord API integration with proper permissions handling
- **Ollama API Client**: Direct communication with local Ollama instances
- **Stable Diffusion API**: REST API integration with AUTOMATIC1111 WebUI
- **Docker Support**: Containerized deployment with Docker Compose

**Configuration Management**
- **Environment Variables**: Secure configuration through .env files
- **Custom System Messages**: Configurable bot personality and behavior
- **Channel Management**: Specific channel targeting with ID-based configuration
- **Model Selection**: Easy switching between different Ollama models

## Installation & Setup

**Prerequisites**
- Node.js v14+ installed
- Ollama installed and running (`ollama serve`)
- AUTOMATIC1111 Stable Diffusion WebUI (optional, for image generation)
- Discord Bot Token from Discord Developer Portal

**Quick Setup**
```bash
# Clone the repository
git clone https://github.com/238SAMIxD/discord-ai-bot.git
cd discord-ai-bot

# Install dependencies
npm install

# Configure environment
cp .env.example .env
# Edit .env with your Discord token and settings

# Start the bot
npm start
```

**Docker Deployment**
```bash
# Using Make (if available)
make compose-up

# Or directly with Docker Compose
docker compose -p discord-ai up
```

**Configuration Steps**
1. **Discord Bot Setup**: Create application and bot in Discord Developer Portal
2. **Permissions**: Enable Message Content Intent and Server Members Intent
3. **Model Preparation**: Pull desired Ollama models (`ollama pull llama2`)
4. **Channel Configuration**: Set specific Discord channel IDs for bot operation
5. **Optional Stable Diffusion**: Configure WebUI with `--api --listen` flags

## Use Cases

**Community Engagement**
- **Interactive Conversations**: Natural language discussions with community members
- **Creative Assistance**: Help with writing, brainstorming, and creative projects
- **Technical Support**: Answer questions and provide information on various topics
- **Entertainment**: Engaging conversations and creative interactions

**Content Creation**
- **AI-Generated Art**: Create custom images based on text prompts
- **Story Writing**: Collaborative storytelling with AI assistance
- **Meme Generation**: Create humorous content for community entertainment
- **Educational Content**: Generate explanations and learning materials

**Server Management**
- **Automated Responses**: Handle common questions and provide consistent information
- **Moderation Assistance**: Help with community guidelines and information
- **Welcome Messages**: Personalized greetings for new server members
- **Activity Engagement**: Keep communities active with interactive AI responses

## Advanced Features

**Multi-Model Support**
- **Local LLMs**: Support for various Ollama models (Llama2, Orca, Mistral, Neural-Chat)
- **Model Switching**: Easy configuration to switch between different language models
- **Performance Optimization**: Local processing for faster response times
- **Resource Management**: Efficient handling of multiple concurrent requests

**Customization Options**
- **System Prompts**: Customizable personality and behavior instructions
- **Response Filtering**: Configure appropriate responses for community standards
- **Channel Restrictions**: Limit bot operation to specific channels
- **User Interaction**: Handle mentions, direct messages, and group conversations

**Development Features**
- **TypeScript Migration**: Active rewrite to TypeScript for better maintainability
- **Docker Integration**: Containerized deployment for easy scaling
- **API Integration**: Well-structured API calls to external services
- **Error Handling**: Robust error management and logging

## Deployment Options

**Self-Hosted Setup**
- **Local Deployment**: Run on personal servers or development machines
- **Privacy Control**: Complete data control with local processing
- **Cost-Effective**: No ongoing API costs after initial setup
- **Customizable**: Full control over models and configurations

**Docker Deployment**
- **Containerized Environment**: Consistent deployment across different systems
- **Easy Scaling**: Simple horizontal scaling with multiple containers
- **Version Management**: Easy updates and rollbacks
- **Isolation**: Secure, isolated execution environment

**Cloud Deployment**
- **VPS Hosting**: Deploy on cloud virtual private servers
- **GPU Integration**: Utilize cloud GPU instances for better performance
- **Load Balancing**: Distribute load across multiple instances
- **Monitoring**: Cloud-based monitoring and logging solutions

## Community & Development

**Project Status**
- **Maintenance Mode**: Currently in maintenance with active TypeScript rewrite
- **Open Source**: MIT-licensed with community contributions welcome
- **Active Development**: Regular updates and improvements
- **Community Support**: GitHub issues and community discussions

**Contributing**
- **TypeScript Branch**: Active development on TypeScript rewrite
- **Issue Reporting**: Bug reports and feature requests welcome
- **Code Contributions**: Pull requests accepted for improvements
- **Documentation**: Help with setup guides and troubleshooting

**Related Projects**
- **Similar Implementations**: Various Discord-Ollama integrations available
- **Educational Value**: Featured in academic projects and case studies
- **Community Adoption**: Multiple forks and derivative projects

This Discord AI Bot represents an excellent entry point into self-hosted AI for Discord communities, offering both conversational AI and image generation capabilities while maintaining complete privacy and control over data and costs. Whether you're running a gaming server, educational community, or creative group, this bot provides powerful AI features without the ongoing expenses of commercial AI services.
