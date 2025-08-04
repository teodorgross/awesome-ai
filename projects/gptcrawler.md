---
title: "GPT Crawler"
category: "Research"
description: "A web crawler that generates knowledge files from websites to create custom GPTs and AI assistants from one or multiple URLs."
website: "https://github.com/BuilderIO/gpt-crawler"
icon: "https://avatars.githubusercontent.com/u/35700027?s=48&v=4"
tags: ["web-crawling", "custom-gpt", "knowledge-extraction", "ai-training", "data-collection"]
pricing: "Free"
---

# GPT Crawler

GPT Crawler is an open-source tool that crawls websites to generate knowledge files suitable for creating custom GPTs and AI assistants. The platform enables users to transform any website or documentation into structured knowledge that can be uploaded to OpenAI's custom GPT platform or used with AI assistants.

## Key Features

**Website Knowledge Extraction**
Crawls websites systematically to extract and structure content into knowledge files that can be used to train custom AI models and assistants.

**Custom GPT Creation**
Generates properly formatted files that can be directly uploaded to OpenAI's custom GPT platform to create specialized AI assistants.

**Configurable Crawling**
Highly configurable crawling parameters including URL patterns, content selectors, page limits, and file size constraints.

**Multiple Output Formats**
Supports various output formats and configurations suitable for different AI platforms and use cases.

## Target Users

**Primary Users**
- Developers creating custom GPT assistants
- Content creators building AI knowledge bases
- Documentation teams automating AI assistant creation
- Businesses wanting custom AI support tools

**Secondary Users**
- Researchers collecting web-based knowledge
- Educational institutions creating AI tutors
- Support teams building automated help systems
- Consultants developing client-specific AI tools

## Use Cases

- Creating custom GPTs from company documentation
- Building AI assistants for product support
- Extracting knowledge from educational resources
- Automating FAQ and help system creation
- Converting website content into AI training data

## Key Benefits

**Automated Knowledge Extraction**
Eliminates manual content preparation by automatically extracting and formatting website content for AI training.

**Time Efficiency**
Dramatically reduces time needed to create custom AI assistants from existing documentation.

**Customizable Processing**
Flexible configuration options allow fine-tuning of crawling behavior for specific website structures.

**Direct Integration**
Generated files are ready for immediate upload to OpenAI's platform without additional processing.

## Configuration Options

**Basic Configuration**
- **URL**: Starting point for crawling with sitemap support
- **Match Pattern**: URL pattern matching for selective crawling
- **Selector**: CSS selector for content extraction
- **Max Pages**: Limit on number of pages to crawl
- **Output Filename**: Custom naming for generated files

**Advanced Settings**
- **Resource Exclusions**: Filter out unwanted file types (images, videos, etc.)
- **Max File Size**: Control output file size in megabytes
- **Max Tokens**: Limit token count for AI model compatibility
- **Custom Selectors**: Target specific content areas

## Technical Features

**Intelligent Crawling**
- Respects robots.txt and sitemap protocols
- Handles dynamic content and JavaScript-rendered pages
- Supports various content selectors and extraction rules
- Manages crawl depth and breadth efficiently

**Output Optimization**
- Generates clean, structured JSON output
- Optimizes content for AI model consumption
- Handles large datasets with file splitting capabilities
- Provides tokenization options for size management

**Container Support**
- Docker containerization for consistent execution
- API server mode for programmatic access
- Express.js-based server with REST endpoints
- Swagger documentation for API usage

## Installation and Setup

**Requirements**
- Node.js version 16 or higher
- Git for repository cloning
- Optional: Docker for containerized execution

**Quick Start**
```bash
git clone https://github.com/builderio/gpt-crawler
npm install
# Edit config.ts with your target website
npm start
```

**Example Configuration**
```typescript
export const defaultConfig: Config = {
  url: "https://docs.example.com",
  match: "https://docs.example.com/**",
  selector: ".main-content",
  maxPagesToCrawl: 50,
  outputFileName: "knowledge.json",
};
```

## Integration Options

**Custom GPT Creation**
Upload generated files directly to OpenAI's custom GPT platform through ChatGPT interface.

**API Integration**
Use OpenAI's Assistants API to create programmatic AI assistants with the extracted knowledge.

**Server Mode**
Run as an API server with `/crawl` endpoint for automated knowledge extraction workflows.

## Example Use Case

The project includes a real example of a Builder.io assistant created by crawling their documentation, demonstrating how website content can be transformed into a functional AI assistant capable of answering questions about integration and usage.

## Pricing

Completely free and open-source software. Users only need compatible hardware and may require paid OpenAI plans for custom GPT creation and usage.
