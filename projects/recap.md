---
title: "Recap"
category: "Chat"
description: "Open-source, privacy-first macOS-native AI meeting summary tool with local processing and automatic audio recording"
website: "https://github.com/rawandahmad698/Recap"
icon: "https://raw.githubusercontent.com/rawandahmad698/Recap/refs/heads/main/Recap/Assets.xcassets/AppIcon.appiconset/appstore1024.png"
tags: ["meeting-summary", "privacy-first", "macos", "local-processing", "audio-transcription"]
github: "https://github.com/rawandahmad698/Recap"
pricing: "Free"
---

# Recap

Recap is an open-source, privacy-focused, macOS-native application designed to automatically summarize meetings and audio content. Built for professionals who need to stay focused on their work while capturing important meeting highlights without compromising privacy.

![Recap](https://raw.githubusercontent.com/rawandahmad698/Recap/refs/heads/main/Recap/Assets.xcassets/AppIcon.appiconset/appstore1024.png)


## Key Features

**Privacy-First Architecture**: All audio processing and transcription happens locally on your Mac using Apple's native technologies - no data leaves your device unless you explicitly choose to share it.

**Automatic Meeting Detection**: Automatically detects meetings in Microsoft Teams, Zoom, Google Meet, and other popular platforms using macOS ScreenCaptureKit (coming soon).

**Local Audio Processing**: Records system audio and optionally microphone input using native Core Audio taps and AVAudioEngine for driver-free system audio capture.

**AI-Powered Transcription**: Uses WhisperKit (MLX) for local speech-to-text transcription with high accuracy and multiple model options including Large v3 for best results.

**Intelligent Summarization**: Leverages Ollama for local LLM processing or optionally OpenRouter for cloud-based summarization when local compute is insufficient.

**Native macOS Integration**: Built with Swift + SwiftUI for optimal performance and seamless integration with macOS features and UI conventions.

## Technical Architecture

- **Audio Capture**: Core Audio taps, AVAudioEngine for system and microphone audio
- **Transcription**: WhisperKit (MLX) running locally on Apple Silicon
- **Summarization**: Ollama (local) or OpenRouter (cloud) for LLM processing
- **Framework**: Swift + SwiftUI for native macOS experience
- **Storage**: Local database with optional keychain integration for secure token storage

## System Requirements

### Ollama (Local Processing - Recommended)
- **macOS**: 15.0 or later
- **Processor**: Apple M1 minimum, M2 Pro or newer recommended
- **RAM**: 16 GB minimum, 32 GB+ recommended
- **Storage**: 10 GB free space minimum, 50 GB recommended

### OpenRouter (Cloud Processing)
- **macOS**: 15.0 or later  
- **Processor**: Apple M1 minimum, M2 or newer recommended
- **RAM**: 8 GB minimum, 16 GB recommended
- **Storage**: 2 GB free space minimum, 5 GB recommended

**Note**: Intel Macs are not officially supported - use at your own risk.

## Workflow Process

1. **App Selection**: Choose target application for audio monitoring
2. **Recording**: Capture system audio + optional microphone input
3. **Processing**: Automatic transcription using local Whisper models
4. **Summarization**: Generate meeting summaries using local or cloud LLM
5. **Storage**: Save results locally with database record management
6. **Review**: Access summaries and transcripts through native interface

## Setup Instructions

### Prerequisites
- Xcode 15.0 or later
- Hugging Face token for Whisper model downloads
- OpenRouter API key (optional, for cloud processing)
- Ollama installation (for local processing)

### Installation
```bash
git clone https://github.com/rawandahmad698/recap.git
cd recap
open Recap.xcodeproj
# Build and run in Xcode (⌘+R)
```

### Configuration
1. **Environment Variables**: Set HF_TOKEN (required) and OPENROUTER_API_KEY (optional) in Xcode Scheme Editor
2. **Ollama Setup**: Install Ollama and pull models (`ollama pull llama3`)
3. **Whisper Models**: Download Whisper model through Settings → Whisper Models
4. **LLM Provider**: Configure preferred provider in Settings → LLM Models

## Development Status

**Current State**: Proof of concept with core functionality working but incomplete features. Developer uses daily and actively developing new features.

**Planned Features**:
- Enhanced meeting detection for major platforms
- Custom prompt configuration via settings
- Background audio processing
- Automatic recording stop functionality
- Improved error handling and user experience
- 85%+ test coverage for reliability

## Use Cases

**Meeting Productivity**: Stay focused on work while automatically capturing meeting highlights and decisions without manual note-taking.

**Content Creation**: Transcribe and summarize interviews, podcasts, or any audio content for content creators and researchers.

**Business Intelligence**: Extract key insights from customer calls, team meetings, and strategic discussions while maintaining data privacy.

**Personal Productivity**: Capture ideas from voice memos, phone calls, or any audio source with automatic organization and summarization.

**Educational Applications**: Transcribe lectures, seminars, or educational content for students and educators.

## Privacy & Security

- **Local Processing**: WhisperKit transcription runs entirely on-device
- **Data Ownership**: All recordings and transcripts stored locally on user's Mac
- **Optional Cloud**: OpenRouter integration available but data leaves device only when explicitly chosen
- **Transparent Code**: Fully open-source codebase for complete transparency
- **No Tracking**: No analytics, telemetry, or data collection

## Contributing

The project actively seeks contributions from developers of all skill levels. Key areas for contribution include:

- **Core Features**: Meeting detection, background processing, UI improvements
- **Code Quality**: Testing, documentation, SwiftLint/SwiftFormat integration
- **Platform Support**: Enhanced macOS integration, accessibility features
- **Performance**: Optimization for various Mac configurations

Fork the repository, create feature branches, and submit pull requests with clear descriptions of changes.
