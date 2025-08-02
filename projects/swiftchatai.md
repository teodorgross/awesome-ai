---
title: "SwiftChat"
category: "Chat"
description: "Lightning-fast cross-platform Chat app with React Native, powered by Amazon Bedrock with multimodal support"
website: "https://github.com/aws-samples/swift-chat"
icon: ""
tags: ["react-native", "amazon-bedrock", "cross-platform", "multimodal", "aws"]
pricing: "Free"
---

# SwiftChat

SwiftChat is a lightning-fast, cross-platform Chat application built with React Native and powered by Amazon Bedrock. With its minimalist design philosophy and robust privacy protection, it delivers real-time streaming conversations, AI image generation, and voice conversation capabilities across Android, iOS, and macOS platforms.

## Key Features

- 🚀 **Cross-Platform Support**: Native performance on Android, iOS, and macOS with React Native
- 🤖 **Multiple AI Providers**: Amazon Bedrock, OpenAI, DeepSeek, Ollama, and OpenAI-compatible models
- 🎨 **AI Image Generation**: Powered by Amazon Nova Lite with natural language prompts
- 🎙️ **Speech-to-Speech**: Amazon Nova Sonic integration for voice conversations on Apple platforms
- 📱 **Multimodal Analysis**: Support for text, image, document, and video inputs
- 🌙 **Dark Mode**: System-following dark mode across all platforms
- 📊 **Usage Statistics**: Built-in analytics and chat history management
- 🔒 **Privacy-First**: Robust privacy protection with local data handling

## Advanced Capabilities

### Creative Image Suite
- Image generation with Chinese prompt support
- Style replication and background manipulation
- Natural language commands for Nova Canvas operations
- Background removal and replacement

### System Prompt Management
- Preset system prompts with full CRUD operations
- Custom prompt creation and organization
- Sort and manage conversation contexts

### Enhanced User Experience
- LaTeX formula rendering (inline and display modes)
- Landscape mode optimization for tables and code
- Text selection and copy functionality
- Streamlined chat history and settings

## Use Cases

**Developers**: Perfect for integrating AI capabilities into mobile applications with AWS infrastructure. The open-source codebase provides excellent learning material for React Native and AWS Bedrock integration.

**Businesses**: Ideal for organizations already using AWS services who want a customizable, privacy-focused Chat solution that can be deployed on their own infrastructure.

**Students & Researchers**: Excellent for learning about multimodal AI applications, serverless architecture, and cross-platform mobile development.

## Technical Architecture

- **Frontend**: React Native for cross-platform mobile development
- **Backend**: Python FastAPI with AWS Lambda/App Runner deployment
- **AI Models**: Amazon Bedrock (Nova, Titan) with fallback to other providers
- **Infrastructure**: CloudFormation templates for easy AWS deployment
- **Storage**: AWS Parameter Store for configuration management

## Getting Started

1. **Prerequisites**: AWS account with Bedrock model access, React Native development environment
2. **Clone Repository**: Download from GitHub and navigate to react-native folder
3. **Install Dependencies**: Run npm install and platform-specific setup (pod install for iOS)
4. **Configure AWS**: Set up Parameter Store with API keys and deploy CloudFormation stack
5. **Launch**: Execute npm start and build for your target platform

## Deployment Options

- **AWS App Runner**: Fully managed container service for production
- **AWS Lambda**: Cost-effective serverless option with Function URLs
- **Local Development**: Run backend locally for testing and development

SwiftChat represents a comprehensive solution for developers looking to build sophisticated Chat applications with enterprise-grade AWS infrastructure while maintaining the flexibility of open-source development.
