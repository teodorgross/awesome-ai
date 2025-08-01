---
title: "Chrome-GPT"
category: "Agent"
description: "AutoGPT agent controlling Chrome browser via Langchain and Selenium"
website: "https://github.com/richardyc/Chrome-GPT"
icon: ""
tags: ["chrome", "selenium", "langchain", "autogpt", "browser-control"]
pricing: "Free"
---

# Chrome-GPT

Chrome-GPT is an AutoGPT experiment that utilizes Langchain and Selenium to enable an AutoGPT agent take control of an entire Chrome session. The agent can interactively scroll, click, and input text on web pages to navigate and manipulate web content.

**Key Features:**
- **Chrome Integration**: Full Chrome browser session control
- **Web Navigation**: Scroll, click, and input text capabilities
- **Google Search**: Built-in search functionality
- **Memory Management**: Both long-term and short-term memory
- **Multiple Agent Types**: Zero-shot, BabyAGI, and Auto-GPT support
- **Tab Management**: Switch between multiple browser tabs
- **Form Interaction**: Fill out contact forms and web forms

**Use Cases:**
- Event planning and venue booking
- Form automation and data entry
- Web research and information gathering
- E-commerce automation and shopping
- Social media management
- Lead generation and contact form filling

**Technical Requirements:**
- Chrome browser
- Python >3.8
- Poetry package manager
- OpenAI API key
- Langchain and Selenium dependencies

**Installation:**
```bash
# Install Poetry and dependencies
poetry install
poetry shell
# Set environment variable
export OPENAI_API_KEY=your_key_here
# Run with GPT-4 (recommended)
python -m chromegpt -v -a auto-gpt -m gpt-4 -t "your task"
```

**Known Limitations:**
- Limited web crawling features
- Slow response time (1-10 seconds per action)
- Occasional parsing errors with GPT outputs
