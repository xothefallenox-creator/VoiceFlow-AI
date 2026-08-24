# VoiceFlow-AI Installation Guide

## Prerequisites

- Windows 10 or Windows 11
- Python 3.11 or Python 3.12
- Git installed
- Gemini API key (required)
- OpenRouter API key (optional but recommended)

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/xothefallenox-creator/VoiceFlow-AI.git
cd VoiceFlow-AI
```

### 2. Create Virtual Environment

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
playwright install
```

### 4. Configure API Keys

Copy the template files and add your credentials:

```bash
cp config/api_keys.json.template config/api_keys.json
cp config/app_settings.json.template config/app_settings.json
```

Edit `config/api_keys.json`:

```json
{
  "gemini_api_key": "YOUR_GEMINI_API_KEY",
  "openrouter_api_key": "YOUR_OPENROUTER_API_KEY"
}
```

### 5. Launch VoiceFlow-AI

```bash
python main.py
```

## Configuration Files

| File | Purpose |
|------|----------|
| `config/api_keys.json` | API credentials (Gemini, OpenRouter) |
| `config/app_settings.json` | Application preferences (wake word, theme, voice) |
| `config/brahma_connect.json` | Device pairing & network settings |
| `config/discord_bot.json` | Discord integration settings |

## Advanced Configuration

### Custom Wake Word

Edit `config/app_settings.json`:

```json
{
  "wake_word": "your custom wake word"
}
```

### Developer Mode (Website Builder)

```json
{
  "developer_mode_enabled": true,
  "developer_mode_workspace": "C:\\path\\to\\workspace"
}
```

## Troubleshooting

### Port Already in Use

If port 8000 or 8765 is already in use, VoiceFlow-AI will disable those services.

### Missing Playwright Browsers

```bash
python -m playwright install
```

### API Key Issues

Ensure your API keys are correctly placed in `config/api_keys.json` with no extra whitespace.

## Support

For issues and feature requests, please open an issue on GitHub.