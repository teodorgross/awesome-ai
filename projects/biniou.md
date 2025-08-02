---
title: "biniou"
category: "Chat"
description: "Self-hosted WebUI for 30+ generative AI models covering text, image, audio, video, and 3D generation with offline capability"
website: "https://github.com/Woolverine94/biniou"
icon: "https://avatars.githubusercontent.com/u/146110286?s=48&v=4"
tags: ["self-hosted", "multi-modal", "offline", "comprehensive", "gradio"]
pricing: "Free"
---

# biniou

A comprehensive self-hosted WebUI for 30+ generative AI models, enabling multimedia content generation across text, images, audio, video, and 3D objects. Works on computers with as little as 8GB RAM and can operate completely offline once deployed.

## Key Features

**Comprehensive AI Suite**
- 30+ generative AI models in one interface
- Text, image, audio, video, and 3D generation
- Works offline after initial setup
- No dedicated GPU required (though recommended)

**Multi-Modal Capabilities**
- Text generation with llama-cpp chatbot and Llava multimodal
- Image generation via Stable Diffusion, Kandinsky, Flux, PixArt
- Audio creation through MusicGen, AudioGen, Bark
- Video generation with ModelScope, AnimateDiff, Stable Video
- 3D object creation using Shap-E

**User-Friendly Design**
- Web-based interface with dark/light themes
- Multi-language support (English, French, Chinese)
- Zeroconf installation with one-click installers
- Cross-platform compatibility (Linux, Windows, macOS)

**Advanced Management**
- Built-in control panel for updates and configuration
- Model management through simple interface
- Communication between modules
- Settings saved as metadata in generated content

## Technical Specifications

- **Minimum RAM**: 8GB (16GB+ recommended)
- **Storage**: 20-30GB base + ~200GB for all models
- **Platform**: Cross-platform (Linux, Windows, macOS)
- **Framework**: Gradio-based WebUI
- **Backend**: HuggingFace Transformers and Diffusers
- **Acceleration**: CUDA and ROCm support available

## Text Generation Modules

**Chat & Language**
- llama-cpp based chatbot (.gguf models)
- Llava multimodal chatbot (vision + text)
- Microsoft GIT image captioning
- Whisper speech-to-text (audio transcription)
- NLLB translation (200 languages)
- Prompt generator for enhanced prompts

## Image Generation & Modification

**Generation Models**
- Stable Diffusion (SD 1.5, SD 2.1, SDXL, SD3, SD3.5)
- Kandinsky text-to-image
- Latent Consistency Models (LCM)
- Midjourney-mini style generation
- PixArt-Alpha high-quality generation
- Flux (Dev, Schnell, Lite variants)

**Modification Tools**
- Img2img transformation
- IP-Adapter style transfer
- Instruct Pix2Pix editing
- MagicMix style mixing
- Inpainting and outpainting
- ControlNet guided generation
- Photobooth face manipulation
- InsightFace faceswapping
- Real ESRGAN upscaling
- GFPGAN face restoration

## Audio Generation

**Music & Sound**
- MusicGen music generation
- MusicGen Melody with conditioning
- MusicLDM audio synthesis
- AudioGen sound effects
- Harmonai audio generation
- Bark text-to-speech synthesis

## Video Generation

**Video Creation**
- ModelScope text-to-video
- Text2Video-Zero conversion
- AnimateDiff animation
- Stable Video Diffusion
- Video Instruct-Pix2Pix editing

## 3D Generation

**3D Objects**
- Shap-E text-to-3D shape
- Shap-E image-to-3D conversion
- 3D model export capabilities

## Installation Options

**One-Click Installers**
```bash
# Linux (Debian/Ubuntu)
sh <(curl https://raw.githubusercontent.com/Woolverine94/biniou/main/oci-debian.sh)

# OpenSUSE
sh <(curl https://raw.githubusercontent.com/Woolverine94/biniou/main/oci-opensuse.sh)

# RHEL/Fedora
sh <(curl https://raw.githubusercontent.com/Woolverine94/biniou/main/oci-rhel.sh)
```

**Windows Installation**
- Download and run `biniou_netinstall.exe`
- Or download and execute `install_win.cmd`
- Automated installation with UAC prompts

**Docker Deployment**
```bash
# CPU version
docker pull ghcr.io/woolverine94/biniou:main
docker run -it --restart=always -p 7860:7860 \
  -v biniou_outputs:/home/biniou/biniou/outputs \
  -v biniou_models:/home/biniou/biniou/models \
  ghcr.io/woolverine94/biniou:main

# CUDA version
docker pull ghcr.io/woolverine94/biniou-cuda:main
docker run -it --gpus all --restart=always -p 7860:7860 \
  [volumes...] ghcr.io/woolverine94/biniou-cuda:main
```

## Hardware Acceleration

**CUDA Support**
- Nvidia GPU acceleration
- CUDA 12.1 environment required
- Significant performance improvements
- All modules except chatbot benefit from CUDA

**ROCm Support (Experimental)**
- AMD GPU acceleration on Linux
- ROCm 5.6 environment required
- Linux-only support currently

**CPU Optimization**
- Works on CPU-only systems
- llama-cpp-python optimizations
- OpenBLAS, OpenCL BLAS support
- Vulkan backend available

## Model Support

**Text Models**
- Llama/2/3, Mistral, Mixtral compatibility
- GGUF quantized models
- Built-in model list + custom models
- TheBloke GGUF integration

**Image Models**
- Stable Diffusion variants (1.5, 2.1, XL, 3.x)
- LoRA model support (SD 1.5, SDXL, SD 3.5, Flux)
- Textual inversion support
- Custom .safetensors files

**Specialized Models**
- Audio: MusicGen, AudioGen, Bark variants
- Video: ModelScope, AnimateDiff, SVD
- 3D: Shap-E text and image models

## Use Cases

**Creative Content Production**
- Multi-modal content creation
- Artistic image generation and editing
- Music and audio production
- Video content creation
- 3D asset generation

**Personal AI Studio**
- Complete offline AI capabilities
- Privacy-focused content generation
- No cloud dependencies
- Local model storage and management

**Educational & Research**
- AI model experimentation
- Multi-modal AI learning
- Comparative model analysis
- Research and development

**Professional Applications**
- Content creation workflows
- Rapid prototyping
- Design iteration
- Media production

## System Requirements

**Minimum Configuration**
- 64-bit CPU (AMD64 only)
- 8GB RAM
- 20-30GB storage (base installation)
- HDD storage acceptable

**Recommended Configuration**
- Multi-core 64-bit CPU + CUDA/ROCm GPU
- 16GB+ RAM
- 200GB+ SSD storage
- High-speed internet for initial setup

## Community & Development

**Open Source Development**
- GNU GPL3 licensed
- Active weekly updates
- Community contributions welcome
- Comprehensive documentation

**Supported Platforms**
- Linux: Debian, Ubuntu, Fedora, OpenSUSE, Arch
- Windows: 10/11 with full compatibility
- macOS: Experimental support via Homebrew
- Docker: Full containerization support

biniou represents the most comprehensive self-hosted AI generation platform available, providing professional-grade capabilities across all major AI modalities in a single, easy-to-deploy package.
