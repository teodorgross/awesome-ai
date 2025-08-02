---
title: "FreedomGPT"
category: "Chat"
description: "React and Electron-based desktop app for running LLM models locally with offline privacy and chat interface"
website: "https://github.com/ohmplatform/FreedomGPT"
icon: ""
tags: ["electron", "desktop", "offline", "privacy", "local-llm"]
pricing: "Free"
---

# FreedomGPT

A React and Electron-based desktop application that executes Large Language Models locally, providing offline and private AI conversations on Mac and Windows through an intuitive chat-based interface.

## Key Features

**Desktop Application**
- Native Electron app for Mac and Windows
- React-based modern user interface
- Offline operation with complete privacy
- Local model execution without internet dependency

**Privacy-Focused Design**
- All processing happens locally on your machine
- No data transmission to external servers
- Complete conversation privacy
- Air-gapped AI capability

**Local Model Support**
- Liberty Edge models integration
- Manual model download and configuration
- Support for GGML format models
- Customizable model paths and settings

**Advanced Features**
- Chat-based conversational interface
- Model switching and management
- Mining earnings capability (XMRig integration)
- Configurable ports and settings

## Technical Specifications

- **Framework**: Electron + React desktop application
- **Backend**: llama.cpp for model inference
- **Platform**: macOS and Windows support
- **Models**: GGML format, Liberty Edge models
- **Privacy**: Complete offline operation
- **Architecture**: Native desktop with C++ inference engine

## Installation & Setup

**Prerequisites**
- Node.js and Yarn package manager
- CMake (Windows) or Make (Linux/Mac)
- C++ compiler (g++ on Linux, MSVC on Windows)
- Git for repository cloning

**Building from Source**
```bash
# Clone repository with submodules
git clone --recursive https://github.com/ohmplatform/FreedomGPT.git freedom-gpt
cd freedom-gpt

# Install dependencies
npx yarn install

# Build llama.cpp backend
cd llama.cpp
make  # Linux/Mac
# OR for Windows:
cmake .
cmake --build . --config Release

# Return to root and start application
cd ..
npx yarn start
```

**Linux-Specific Setup**
```bash
# Install required packages
sudo apt install nodejs yarn git make g++ npm

# Build and run
cd freedom-gpt/llama.cpp
make
cd ..
npm install
npm run
npm start
```

## Model Configuration

**Liberty Edge Models**
- Download models manually from supported sources
- Configure model paths through AI Models screen
- Support for various model sizes and quantizations
- Local model storage and management

**Model Management**
- UI-based model selection
- Custom model path configuration
- Multiple model support
- Easy model switching

## Mining Integration

**XMRig Mining Support**
- Optional cryptocurrency mining functionality
- CPU-only mining capability
- Linux static binary integration
- Mining earnings to support development

**Setup Mining**
```bash
# Download XMRig CPU-only version
wget https://xmrig.com/download/xmrig-linux-static.tar.gz
tar -xzf xmrig-linux-static.tar.gz

# Copy to FreedomGPT directory
cp xmrig freedom-gpt/miner/mac/fgptminer
```

## Use Cases

**Privacy-Conscious Users**
- Sensitive conversation handling
- Complete data control and privacy
- No internet dependency for AI interactions
- Secure offline AI assistance

**Professional Applications**
- Corporate environments with privacy requirements
- Legal and medical consultation privacy
- Confidential document analysis
- Air-gapped system AI capability

**Personal AI Assistant**
- Private personal AI conversations
- Offline writing and coding assistance
- Learning and education without data sharing
- Creative writing and brainstorming

**Development & Research**
- Local AI model testing
- Privacy research applications
- Offline AI development environments
- Custom model integration testing

## Key Advantages

**Complete Privacy**
- Zero data transmission to external servers
- All conversations remain on local machine
- No tracking or analytics
- Full user control over data

**Offline Capability**
- No internet connection required for operation
- Air-gapped environment compatibility
- Reliable operation in any network condition
- Complete independence from cloud services

**Desktop Integration**
- Native desktop application experience
- System integration capabilities
- Local file system access
- Desktop notification support

## Configuration Options

**Port Configuration**
- Customizable ports in `src/ports.ts`
- Network settings adjustment
- Local server configuration
- Multi-instance support

**Model Settings**
- Custom model path configuration
- Performance optimization settings
- Memory usage controls
- Generation parameter tuning

## Community & Development

**Open Source Community**
- Active Discord server for support
- Community-driven development
- Regular updates and improvements
- User feedback integration

**Contributing**
- Open source development model
- Community contributions welcome
- GitHub-based development workflow
- Collaborative improvement process

## Acknowledgments

- **llama.cpp**: Core C++ inference library
- **Meta LLAMA**: Foundation model architecture  
- **Chatbot UI**: User interface inspiration
- **Electron & React**: Application framework
- **Open source community**: Various supporting libraries

## System Requirements

**Minimum Requirements**
- Modern CPU with sufficient performance
- 8GB+ RAM (depends on model size)
- Storage space for models (GBs)
- Windows 10+ or macOS 10.14+

**Recommended Specifications**
- Multi-core CPU with high single-thread performance
- 16GB+ RAM for larger models
- SSD storage for faster model loading
- Dedicated graphics (future GPU support)

## Target Users

- Privacy-focused individuals and organizations
- Developers needing offline AI capabilities
- Professionals in sensitive industries
- Researchers requiring data control
- Users in restricted network environments
- Anyone seeking truly private AI interactions

FreedomGPT represents a significant step toward democratizing private AI access, ensuring users maintain complete control over their data while benefiting from advanced language model capabilities.
