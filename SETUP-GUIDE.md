# 🚀 UI-TARS Privacy Fork Setup Guide

## Quick Start: Computer Operator Setup

### Step 1: Grant System Permissions ⚠️ **REQUIRED**

1. **Open System Settings** (System Preferences on older macOS)
2. **Go to Privacy & Security**  
3. **Grant these permissions to UI-TARS:**
   - ✅ **Screen Recording** - Allows taking screenshots for AI analysis
   - ✅ **Accessibility** - Allows controlling mouse and keyboard

**Without these permissions, the computer operator cannot function.**

### Step 2: Configure AI Provider 🤖

You have several options for AI providers:

#### **Option A: OpenAI (Recommended for beginners)**
1. Get API key from https://platform.openai.com/api-keys
2. In the UI-TARS settings, configure:
   - **VLM Provider**: `OpenAI Compatible`
   - **VLM Base URL**: `https://api.openai.com/v1`
   - **VLM API KEY**: `your-openai-api-key`
   - **VLM Model**: `gpt-4-vision-preview` or `gpt-4o`

#### **Option B: Anthropic Claude**
1. Get API key from https://console.anthropic.com/
2. Configure:
   - **VLM Provider**: `OpenAI Compatible` (uses OpenAI format)
   - **VLM Base URL**: `https://api.anthropic.com/v1`
   - **VLM API KEY**: `your-anthropic-api-key`
   - **VLM Model**: `claude-3-sonnet-20240229`

#### **Option C: Local/Self-hosted Models**
1. Set up a local OpenAI-compatible API server (vLLM, Ollama, etc.)
2. Configure:
   - **VLM Base URL**: `http://localhost:8000/v1` (your local endpoint)
   - **VLM API KEY**: `your-local-key` (if required)

### Step 3: Create Environment File

Create a `.env` file in the root directory with your settings:

```bash
# Example for OpenAI
VLM_PROVIDER=openai
VLM_BASE_URL=https://api.openai.com/v1
VLM_API_KEY=sk-your-openai-key-here
VLM_MODEL_NAME=gpt-4o

# Example for Anthropic
# VLM_PROVIDER=anthropic
# VLM_BASE_URL=https://api.anthropic.com/v1
# VLM_API_KEY=sk-ant-your-key-here
# VLM_MODEL_NAME=claude-3-sonnet-20240229
```

### Step 4: Start Using Computer Operator

1. **Launch the app**: The UI-TARS window should be open
2. **Check permissions**: Green indicators should show permissions are granted
3. **Test with a simple task**: Try "Take a screenshot and describe what you see"
4. **Advanced automation**: "Open Safari and search for 'privacy-focused browsers'"

## 🔐 Privacy Features Active

✅ **No behavioral tracking** - Your usage isn't monitored
✅ **No device fingerprinting** - Random session IDs only  
✅ **No auto-updates** - Manual updates only
✅ **Local-first** - Data stays on your computer

## ⚠️ Data Sharing Notice

**The ONLY data that leaves your computer:**
- Screenshots sent to your chosen AI provider (OpenAI/Anthropic/etc.)
- Your natural language commands sent to the AI
- This happens ONLY when you run automations

**Everything else stays local!**

## Troubleshooting

### "Permissions Denied" Error
- Restart UI-TARS after granting permissions
- Check System Settings > Privacy & Security again

### "API Error" Messages  
- Verify your API key is correct
- Check your API provider has sufficient credits/quota
- Ensure the base URL is correct for your provider

### App Won't Start
- Make sure Node.js 20+ is in your PATH: `node --version`
- Try: `pnpm install` then `pnpm run dev` in `apps/ui-tars/`

## Need Help?

- Check the [main README](README.md) for basic setup
- Review [PRIVACY-CHANGES.md](PRIVACY-CHANGES.md) for what we removed
- Open an issue at: https://github.com/drhudson/UI-TARS-desktop-privacy/issues

---

**Enjoy your privacy-first GUI automation! 🎉**