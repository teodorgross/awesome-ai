---
title: "Ollama Discord Bot"
category: "Chat"
description: "Discord bot with local AI via Ollama, SearxNG web search, document analysis, and website summarization capabilities"
website: "https://github.com/teodorgross/ollama_bot_discord"
icon: "https://github.com/teodorgross.png"
tags: ["discord-bot","ollama","searxng","document-analysis","web-search"]
pricing: "Free"
github: "https://github.com/teodorgross/ollama_bot_discord"
addedDate: 2025-08-04T12:04:02.009Z
submissionSource: "github-scanner-v2"
---
# Ollama Discord Bot

**Ollama Discord Bot** is a sophisticated Discord bot that combines local AI processing through Ollama with web search capabilities via SearxNG to provide comprehensive chat functionalities. This bot excels at answering questions with web context, summarizing websites, and analyzing uploaded documents directly within Discord servers.

## Key Features

**AI-Powered Chat with Web Context**
- **/ask Command**: Pose questions and receive AI-powered responses enhanced with real-time web search results
- **SearxNG Integration**: Privacy-focused metasearch engine for comprehensive web searches
- **Context-Aware Responses**: Combines AI knowledge with current web information
- **Local AI Processing**: Utilizes Ollama for private, cost-effective AI inference

**Advanced Document Analysis**
- **/doc Command**: Upload and analyze Word (.docx) or Excel (.xlsx) files with AI insights
- **Document Q&A**: Ask specific questions about uploaded document content
- **Text Extraction**: Converts documents to text using Mammoth (Word) and SheetJS (Excel)
- **Instant Analysis**: Quick overviews, summaries, and data interpretation within Discord

**Web Content Summarization**
- **/summary Command**: Analyze and summarize any website content
- **Content Scraping**: Intelligent web scraping with text extraction
- **AI Analysis**: Deep content analysis using local Ollama models
- **URL Processing**: Direct website analysis from shared links

**Privacy-Focused Architecture**
- **Local Processing**: All AI operations run locally via Ollama
- **SearxNG Privacy**: Privacy-respecting search without tracking
- **No External APIs**: Completely self-hosted solution
- **Data Control**: All conversations and analysis remain private

## Technical Architecture

**Core Components**
- **Node.js Backend**: Modern JavaScript runtime (v16.9+ required)
- **Discord.js Integration**: Full Discord API implementation with slash commands
- **Ollama API Client**: Direct communication with local Ollama instance
- **SearxNG Interface**: Web search integration for enhanced responses
- **Document Processing**: File analysis with specialized libraries

**Flexible Configuration**
- **config.json**: Centralized configuration for easy customization
- **Model Selection**: Choose from various Ollama models (Gemma2, Llama3, etc.)
- **Language Customization**: Configurable assistant personality and response language
- **Search Integration**: Optional SearxNG instance configuration
- **Guild-Specific Setup**: Per-server configuration options

## Installation & Setup

**Prerequisites**
- Node.js v16.9 or higher
- Running Ollama instance (default: localhost:11434)
- Optional: SearxNG instance for web searches (default: localhost:9090)
- Discord Bot Token and Client ID

**Quick Setup**
```bash
# Clone the repository
git clone https://github.com/teodorgross/ollama_bot_discord.git
cd ollama_bot_discord

# Install dependencies
npm install

# Configure the bot
# Edit config.json with your settings
{
  "token": "YOUR_DISCORD_BOT_TOKEN",
  "client_id": "YOUR_CLIENT_ID",
  "guild_id": "YOUR_GUILD_ID",
  "ollama_url": "http://localhost:11434/",
  "default_model": "gemma2:9b",
  "assistant_description": "Helpful assistant responding in German"
}

# Start the bot
node ./src/main.js
```

**Configuration Options**
- **Discord Integration**: Bot token, client ID, and guild configuration
- **Ollama Settings**: API URL and default model selection
- **Assistant Behavior**: Personality, language, and response style
- **Search Integration**: SearxNG instance URL and search parameters
- **File Processing**: Document analysis settings and limitations

## Use Cases

**Research & Information Gathering**
- **Academic Research**: Combine AI knowledge with current web information
- **Fact Checking**: Verify information using multiple search sources
- **Market Research**: Analyze current trends and gather competitive intelligence
- **News Analysis**: Summarize and analyze current events from multiple sources

**Document Management**
- **Contract Analysis**: Review and summarize legal documents
- **Report Processing**: Extract key insights from business reports
- **Data Analysis**: Process Excel spreadsheets with AI-powered insights
- **Content Review**: Quick analysis of proposals, presentations, and documents

**Web Content Processing**
- **Article Summarization**: Quickly digest long-form content
- **Website Analysis**: Evaluate competitor websites and content strategies
- **Research Compilation**: Gather information from multiple web sources
- **Content Curation**: Process and summarize content for team consumption

**Team Collaboration**
- **Knowledge Sharing**: Instant access to AI-powered insights within team channels
- **Decision Support**: Analyze information to support business decisions
- **Documentation**: Create summaries and analyses for team reference
- **Training Support**: Answer team questions with web-enhanced responses

## Advanced Features

**Intelligent Query Processing**
- **Context Awareness**: Understands conversation flow and context
- **Multi-Source Integration**: Combines AI knowledge with web search results
- **Relevance Filtering**: Prioritizes most relevant information for responses
- **Source Attribution**: Provides sources for web-based information

**Document Intelligence**
- **Multi-Format Support**: Handles various document types with appropriate parsers
- **Content Extraction**: Intelligent text extraction preserving document structure
- **Metadata Analysis**: Processes document properties and metadata
- **Question-Answer Matching**: Links specific questions to relevant document sections

**Web Search Enhancement**
- **Query Optimization**: Transforms user questions into effective search queries
- **Result Aggregation**: Combines information from multiple search sources
- **Content Filtering**: Removes irrelevant or low-quality search results
- **Real-Time Processing**: Fresh information from current web sources

## Security & Privacy

**Data Protection**
- **Local Processing**: All AI inference happens locally
- **Privacy-First Search**: SearxNG ensures anonymous web searches
- **No Data Collection**: Conversations and documents remain private
- **Secure Configuration**: Environment-based configuration for sensitive data

**Access Control**
- **Guild-Specific Operation**: Configurable per Discord server
- **Permission Management**: Discord-native permission system
- **Admin Controls**: Administrative functions for bot management
- **Usage Monitoring**: Track and control bot usage patterns

## Community & Support

**Open Source Development**
- **MIT Licensed**: Free and open source software
- **Community Contributions**: Welcome improvements and feature additions
- **Documentation**: Comprehensive setup and usage guides
- **Issue Tracking**: GitHub-based issue reporting and resolution

**Integration Ecosystem**
- **Ollama Compatibility**: Works with any Ollama-supported model
- **SearxNG Integration**: Compatible with standard SearxNG instances
- **Discord.js Framework**: Built on robust Discord integration library
- **Extensible Architecture**: Easy to extend with additional features

This Discord bot represents an excellent solution for teams and communities wanting advanced AI capabilities without compromising privacy or incurring ongoing API costs. By combining local AI processing with web search and document analysis, it provides a comprehensive information processing tool directly within Discord environments.
