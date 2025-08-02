---
title: "Perplexica"
category: "Chat"
description: "Open-source AI-powered search engine that provides privacy-focused, real-time answers with sources. Alternative to Perplexity AI"
website: "https://github.com/ItzCrazyKns/Perplexica"
icon: "https://raw.githubusercontent.com/ItzCrazyKns/Perplexica/refs/heads/master/src/app/favicon.ico"
tags: ["search-engine", "privacy-focused", "real-time", "open-source", "SearxNG"]
pricing: "Free"
---

# Perplexica

**Perplexica** is an open-source AI-powered search engine that goes deep into the internet to find comprehensive answers. Inspired by Perplexity AI, it serves as a privacy-focused alternative that not only searches the web but truly understands your questions, using advanced machine learning algorithms like similarity searching and embeddings to deliver refined results with clear answers and cited sources.

## Key Features

**Privacy-First Architecture**
- Fully open-source with transparent codebase
- Uses SearxNG metasearch engine for privacy-respecting searches
- No user tracking or search history storage
- Local data processing with self-hosted capabilities
- Complete control over your search data

**Advanced AI Search Modes**
- **Normal Mode**: Processes queries and performs comprehensive web search
- **Copilot Mode**: (In development) Generates multiple queries to find more relevant sources by visiting top matches directly
- **All Mode**: Searches the entire web for comprehensive results
- **Writing Assistant Mode**: Specialized for writing tasks without web search
- **Academic Search Mode**: Finds academic articles and papers for research
- **YouTube Search Mode**: Discovers relevant YouTube videos
- **Wolfram Alpha Mode**: Handles calculations and data analysis queries
- **Reddit Search Mode**: Searches Reddit discussions and community opinions

**Multi-Model LLM Support**
- Local LLM compatibility with Ollama (Llama3, Mixtral, Gemma2)
- OpenAI GPT models integration
- Anthropic Claude support
- Google Gemini compatibility
- Groq API support
- DeepSeek and AI/ML API integration
- Flexible model switching during conversations

**Real-Time Information Access**
- SearxNG integration ensures current, up-to-date results
- Eliminates outdated information from static indexes
- Live web crawling and source ranking
- Dynamic content analysis and verification
- No daily data update overhead

## Technical Architecture

**Core Components**
- **User Interface**: Next.js-based web interface supporting images, videos, and multimedia search
- **Agent/Chains**: Intelligent components that predict actions, understand queries, and determine search necessity
- **SearxNG Integration**: Metasearch engine that aggregates results from 70+ search engines
- **LLMs**: Process content understanding, response generation, and source citation
- **Embedding Models**: Advanced similarity search using cosine similarity and dot product distance for result re-ranking

**Advanced Features**
- Multimodal capabilities with image and video search
- File upload and analysis (documents, images, PDFs)
- API integration for developers
- Docker and non-Docker installation options
- Network exposure capabilities for team access

## Installation & Deployment

**Docker Installation (Recommended)**
```bash
git clone https://github.com/ItzCrazyKns/Perplexica.git
cd Perplexica
# Configure config.toml with API keys
docker compose up -d
# Access at http://localhost:3000
```

**Manual Installation**
- SearxNG setup with JSON format enabled
- Node.js environment with npm dependencies
- Configuration file setup for API integrations
- Build and start processes

**Browser Integration**
- Custom search engine setup in browser settings
- Quick access shortcut: `http://localhost:3000/?q=%s`
- Network exposure for team collaboration

## Use Cases

**Research & Academia**
- Academic paper discovery and analysis
- Real-time fact-checking with source verification
- Multi-source information aggregation
- Citation-ready research with proper sourcing

**Content Creation**
- Writing assistance with factual backing
- Social media content research
- Blog post fact-checking and source gathering
- Creative project research and inspiration

**Professional Applications**
- Market research and competitive analysis
- Technical documentation research
- Business intelligence gathering
- Customer support knowledge base

**Personal Productivity**
- Daily information queries with privacy
- Learning and educational research
- Shopping and product research
- Travel and lifestyle planning

## Developer Integration

**API Capabilities**
- RESTful API for application integration
- Multiple model switching support
- Custom query processing
- JSON response formatting
- Network accessibility options

**Customization Options**
- Custom embedding model integration
- Similarity measure configuration
- Search result ranking algorithms
- Focus mode customization
- Interface theming and branding

## Privacy & Security

**Data Protection**
- No search query logging or storage
- Local processing with self-hosted LLMs
- Open-source transparency for security auditing
- SearxNG privacy-preserving search aggregation
- User data remains on local devices

**Deployment Flexibility**
- Self-hosted infrastructure control
- Docker containerization for isolation
- Local network deployment options
- Cloud deployment with privacy controls

## Community & Support

**Development Community**
- Active GitHub repository with regular updates
- Discord community for user support and feedback
- Comprehensive documentation and guides
- Open-source contribution opportunities

**Upcoming Features**
- Enhanced Copilot Mode completion
- Advanced settings page
- History saving capabilities
- Discover mode for content exploration
- API enhancements and integrations

Perplexica represents the future of privacy-conscious AI search, combining the power of modern language models with the transparency and control of open-source software. Whether you're a researcher, content creator, developer, or privacy-conscious user, Perplexica offers a compelling alternative to commercial AI search engines without compromising on functionality or accuracy.
