---
title: "TorchChat"
category: "Code"
description: "PyTorch-native CLI for running LLMs locally on servers, desktop and mobile with multiple execution modes"
website: "https://github.com/pytorch/torchchat"
icon: "https://avatars.githubusercontent.com/u/21003710?s=48&v=4"
tags: ["pytorch", "mobile", "desktop", "cli", "cross-platform"]
pricing: "Free"
---

# TorchChat

PyTorch-native CLI tool for running large language models seamlessly across servers, desktop, and mobile devices. TorchChat showcases the ability to run LLMs using Python, within C/C++ applications, and on iOS and Android platforms with multiple execution modes and optimization techniques.

## ⚠️ Important Notice

TorchChat is no longer under active development. The project remains available for learning and experimentation but is not receiving updates or new features.

## Key Features

- **Cross-Platform Support**: Python, C/C++, iOS, and Android execution
- **Multiple Execution Modes**: Eager, Compile, AOT Inductor, ExecuTorch
- **Mobile-Friendly**: Optimized for iOS 17+ and Android devices
- **PyTorch Native**: Built entirely on PyTorch ecosystem
- **Multiple Quantization**: Various quantization schemes for efficiency
- **Hardware Flexibility**: Linux x86, macOS M1/M2/M3, mobile devices

## Supported Models

### Popular LLM Support
- **Llama Family**: 3.2 (1B-11B), 3.1 (8B), 3.0 (8B), 2.0 (7B-70B)
- **Code Models**: CodeLlama 7B/34B Python variants
- **Mistral**: 7B base and instruct models
- **Stories Models**: TinyLlama 15M/42M/110M for testing
- **Granite**: IBM's 2B-8B code and instruct models
- **DeepSeek**: R1 Distill 8B reasoning model
- **Open Source**: Open Llama, Llama Guard models

### Multimodal Capabilities
- **Llama 3.2 11B Vision**: Text and image understanding
- **Vision-Language**: Integrated multimodal processing
- **Mobile Vision**: Optimized vision models for mobile devices

## Platform Support

### Desktop/Server
- **Linux x86**: Full feature support with CUDA acceleration
- **macOS**: M1/M2/M3 optimized with Metal acceleration
- **Windows**: Basic support through cross-platform tooling

### Mobile Devices
- **iOS**: iPhone 15 Pro+, iPad with Apple Silicon, 8GB+ RAM
- **Android**: XNNPACK-compatible devices, 12GB+ RAM recommended
- **Optimization**: Specialized mobile quantization and acceleration

## Execution Modes

### Python Environment
- **Eager Execution**: Direct PyTorch inference (default)
- **Torch Compile**: JIT compilation for performance
- **Interactive Chat**: CLI-based conversation interface
- **Server Mode**: REST API with OpenAI-compatible endpoints

### Native Execution
- **AOT Inductor (AOTI)**: Ahead-of-time compilation for C++
- **ExecuTorch**: Mobile-optimized inference engine
- **Shared Libraries**: .so files for native integration
- **Standalone Executables**: Self-contained inference binaries

## Advanced Features

### Quantization Support
- **Multiple Precision**: float32, float16, bfloat16
- **Mobile Quantization**: Specialized config for mobile devices
- **CUDA Optimization**: GPU-specific quantization schemes
- **Performance Tuning**: Hardware-specific optimization

### Model Management
- **Hugging Face Integration**: Direct model downloads
- **Alias System**: Friendly names for popular models
- **Inventory Management**: Download, list, remove commands
- **Authentication**: Hugging Face token integration

### Development Tools
- **Model Export**: Generate deployment artifacts
- **Evaluation**: lm-eval integration for model testing
- **Customization**: Flexible model configuration options
- **REST API**: OpenAI-compatible server interface

## Installation & Setup

### Prerequisites
- **Python**: 3.10 or higher
- **PyTorch**: Latest version via requirements
- **Platform Tools**: Platform-specific SDKs for mobile development

### Quick Start
```bash
git clone https://github.com/pytorch/torchchat.git
cd torchchat
python3 -m venv .venv
source .venv/bin/activate
./install/install_requirements.sh
mkdir exportedModels
```

### Model Download
```bash
# Login to Hugging Face
huggingface-cli login

# List available models
python3 torchchat.py list

# Download a model
python3 torchchat.py download llama3.1
```

## Usage Examples

### Interactive Chat
```bash
python3 torchchat.py chat llama3.1
```

### Text Generation
```bash
python3 torchchat.py generate llama3.1 --prompt "write me a story about a boy and his bear"
```

### REST Server
```bash
# Start server
python3 torchchat.py server llama3.1

# Query with curl
curl http://127.0.0.1:5000/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{"model": "llama3.1", "messages": [{"role": "user", "content": "Hello!"}]}'
```

## Mobile Deployment

### iOS Setup
1. **Requirements**: Xcode 15.0+, CMake 3.19+, development provisioning
2. **Export Model**: `python3 torchchat.py export llama3.1 --quantize torchchat/quant_config/mobile.json --output-pte-path llama3.1.pte`
3. **Xcode Project**: Open provided iOS project and deploy
4. **File Transfer**: Copy .pte and tokenizer files to device

### Android Setup
1. **Requirements**: Android Studio, Java 17, Android SDK 34
2. **Download AAR**: ExecuTorch Android library
3. **Push Files**: Use adb to transfer model and tokenizer
4. **Build & Run**: Use Android Studio or automated script

## Performance Optimization

### AOT Inductor
```bash
# Export optimized model
python3 torchchat.py export llama3.1 --output-aoti-package-path exportedModels/llama3_1_artifacts.pt2 --quantize torchchat/quant_config/cuda.json

# Run with C++ binary
cmake-out/aoti_run exportedModels/llama3_1_artifacts.pt2 -z $(python3 torchchat.py where llama3.1)/tokenizer.model -i "Once upon a time"
```

### ExecuTorch Mobile
```bash
# Setup ExecuTorch
export TORCHCHAT_ROOT=${PWD}
./torchchat/utils/scripts/install_et.sh

# Export for mobile
python3 torchchat.py export llama3.1 --quantize torchchat/quant_config/mobile.json --output-pte-path llama3.1.pte
```

## Technical Architecture

### Core Design Principles
- **PyTorch Native**: Pure PyTorch implementation
- **Composition Over Inheritance**: Modular, readable code structure
- **No Training Frameworks**: Explicit logic for extensibility
- **Usability First**: User experience over complexity

### Component Structure
- **Model Loading**: Hugging Face integration with local caching
- **Inference Engine**: Multiple execution backends
- **Mobile Runtime**: ExecuTorch optimization for mobile devices
- **API Layer**: OpenAI-compatible REST interface

## Use Cases

### Development & Research
- **Model Prototyping**: Quick testing of different LLMs
- **Mobile AI**: Deploy LLMs on mobile applications
- **Edge Computing**: Run inference on resource-constrained devices
- **Research Platform**: Experiment with PyTorch optimizations

### Production Applications
- **Embedded Systems**: C++ integration for embedded devices
- **Mobile Apps**: Native iOS and Android LLM integration
- **Server Deployment**: High-performance server inference
- **API Services**: OpenAI-compatible LLM services

### Educational Use
- **Learning PyTorch**: Understand PyTorch optimization techniques
- **Mobile Development**: Learn mobile AI deployment
- **Model Optimization**: Explore quantization and compilation
- **Cross-Platform Development**: Multi-platform AI applications

## Community & Support

### Development Status
- **No Active Development**: Project is in maintenance mode
- **Community Driven**: User contributions and community support
- **Discord Community**: #torchchat-general and #torchchat-contributors
- **GitHub Issues**: Bug reports and feature discussions

### Related Projects
- **Acknowledgments**: Built on GGML, llama2.c, nanoGPT, GPT-Fast
- **PyTorch Ecosystem**: Integrates with broader PyTorch tools
- **ExecuTorch**: Mobile inference optimization
- **Hugging Face**: Model distribution and authentication

## Troubleshooting

### Common Issues
- **Access Restrictions**: Some models require additional authorization
- **Build Failures**: Dependency conflicts with other PyTorch installations
- **Certificate Errors**: SSL certificate verification issues
- **Memory Requirements**: Ensure sufficient RAM for model size

### System Information
```bash
# Generate system info for bug reports
(echo "Operating System Information"; uname -a; echo ""; cat /etc/os-release; echo ""; echo "Python Version"; python --version || python3 --version; echo ""; echo "PIP Version"; pip --version || pip3 --version; echo ""; echo "Installed Packages"; pip freeze || pip3 freeze; echo ""; echo "PyTorch Version"; python -c "import torch; print(torch.__version__)" || python3 -c "import torch; print(torch.__version__)"; echo ""; echo "Collection Complete") > system_info.txt
```
