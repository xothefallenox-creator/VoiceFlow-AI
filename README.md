# VoiceFlow-AI

<div align="center">
  <h1>🎤 VoiceFlow-AI</h1>
  <p><strong>Open-source Windows desktop AI assistant with advanced voice control and automation</strong></p>
  
  [![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
  [![Windows 10/11](https://img.shields.io/badge/platform-Windows%2010%2F11-lightgrey.svg)](https://www.microsoft.com/en-us/windows)
  [![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
  [![Status: Active](https://img.shields.io/badge/status-active%20development-brightgreen.svg)](#)
</div>

---

## Overview

**VoiceFlow-AI** is a powerful, open-source Windows desktop assistant that combines cutting-edge voice recognition with AI-powered automation, intelligent task execution, and document generation—all powered by Gemini and OpenRouter APIs.

Designed for advanced users and developers, VoiceFlow-AI delivers:

✨ **Core Features**
- 🎤 Voice-first command and desktop automation
- 🤖 Gemini 2.5 Flash + OpenRouter fallback AI
- 📱 Desktop to mobile control via Brahma Connect
- 📊 Document & presentation generation
- 🔌 Plugin-ready architecture
- 🖥️ Cross-application browser automation
- 🏠 Smart home device integration
- 🎮 Steam/Epic Games management

---

## Quick Start

### Prerequisites

- **Windows 10** or **Windows 11**
- **Python 3.11+** or **Python 3.12**
- **Git** installed
- **API Keys:**
  - Gemini API key (required) — [Get here](https://ai.google.dev/)
  - OpenRouter API key (optional) — [Get here](https://openrouter.ai/)

### Installation

#### 1️⃣ Clone the Repository

```bash
git clone https://github.com/xothefallenox-creator/VoiceFlow-AI.git
cd VoiceFlow-AI
```

#### 2️⃣ Create Virtual Environment

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

#### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
playwright install
```

#### 4️⃣ Configure API Keys

Copy the template and add your credentials:

```bash
cp config/api_keys.json.template config/api_keys.json
```

Edit `config/api_keys.json`:

```json
{
  "gemini_api_key": "YOUR_GEMINI_API_KEY",
  "openrouter_api_key": "YOUR_OPENROUTER_API_KEY"
}
```

#### 5️⃣ Launch VoiceFlow-AI

```bash
python main.py
```

---

## Configuration

### Configuration Files

| File | Purpose |
|------|---------|
| `config/api_keys.json` | Gemini & OpenRouter API credentials |
| `config/app_settings.json` | Application preferences (wake word, theme, voice) |
| `config/brahma_connect.json` | Device pairing & gateway settings |
| `config/discord_bot.json` | Discord bot token & settings |

### Customize Wake Word

Edit `config/app_settings.json`:

```json
{
  "app_name": "VoiceFlow-AI",
  "wake_word": "hello voice flow",
  "theme": "dark",
  "voice_language": "en-US"
}
```

### Enable Developer Mode (Website Builder)

```json
{
  "developer_mode_enabled": true,
  "developer_mode_workspace": "C:\\path\\to\\workspace"
}
```

---

## Project Structure

```
VoiceFlow-AI/
├── main.py                      # Application entry point & AI orchestration
├── ui.py                        # PyQt6 desktop interface
├── or_client.py                 # OpenRouter AI client
├── plugin_manager.py            # Plugin system
├── requirements.txt             # Python dependencies
├── setup.py                     # Installation script
│
├── config/                      # Configuration & credentials
│   ├── api_keys.json            # API credentials
│   ├── app_settings.json        # Application settings
│   ├── brahma_connect.json      # Device pairing config
│   └── discord_bot.json         # Discord integration
│
├── actions/                     # Modular automation tools
│   ├── open_app.py             # App launcher
│   ├── browser_control.py      # Browser automation
│   ├── file_controller.py      # File/folder management
│   ├── screen_processor.py     # Screen capture & analysis
│   └── weather_report.py       # Weather fetching
│
├── plugins/                     # Custom plugin extensions
│   └── example_plugin.py        # Plugin template
│
├── memory/                      # Long-term memory storage
│   └── memory_manager.py        # Memory persistence
│
├── smart_home/                  # Smart home device control
│   ├── service.py              # Smart home service
│   └── smart_device_manager.py # Device management
│
└── tests/                       # Testing suite
```

---

## Features & Capabilities

### 🎤 Voice & Text Control
- Natural language command processing
- Wake-word detection
- Multi-language support
- Real-time transcription

### 🖥️ Desktop Automation
- Open/close applications
- Window management
- Keyboard & mouse control
- Screenshot capture & analysis

### 🌐 Browser Automation
- Navigate websites
- Click elements & fill forms
- Web search
- YouTube integration

### 📄 Document Generation
- PowerPoint presentations
- Excel spreadsheets
- Word documents
- PDF exports

### 🏠 Smart Home Integration
- TP-Link Kasa devices
- Atomberg fans
- Room-based control

### 📱 Brahma Connect
- Pair Android devices
- Remote app launching
- File transfer
- Media control

### 💬 Integrations
- Discord bot
- WhatsApp/Telegram
- Gemini API
- OpenRouter fallback

### 🔌 Plugin System

Extend VoiceFlow-AI with custom plugins in the `plugins/` directory.

---

## API Keys Setup

### Gemini API Key
1. Visit [Google AI Studio](https://ai.google.dev/)
2. Click "Get API Key"
3. Add key to `config/api_keys.json`

### OpenRouter API Key
1. Register at [OpenRouter.ai](https://openrouter.ai/)
2. Generate API key
3. Add key to `config/api_keys.json`

---

## Troubleshooting

### Port Already in Use
```powershell
netstat -ano | findstr :8000
kill PID
```

### Missing Playwright Browsers
```bash
python -m playwright install
```

### API Key Issues
- Ensure JSON is valid
- Check for extra whitespace
- Verify keys are active

---

## Best Practices

✅ Store API keys in config files only  
✅ Use virtual environment  
✅ Restart after config changes  
✅ Review plugins before loading  

❌ Never commit API keys  
❌ Don't share credentials  

---

## Community & Support

- 📧 [GitHub Issues](https://github.com/xothefallenox-creator/VoiceFlow-AI/issues)
- 💬 [GitHub Discussions](https://github.com/xothefallenox-creator/VoiceFlow-AI/discussions)
- 🤝 Contributing welcome!

---

## License

MIT License — See [LICENSE](LICENSE) for details.

---

<div align="center">
  <p><strong>🚀 Ready to automate your Windows desktop?</strong></p>
  <p><a href="#quick-start">Get Started</a> • <a href="#features--capabilities">Features</a> • <a href="#configuration">Config</a> • <a href="#community--support">Support</a></p>
</div>
