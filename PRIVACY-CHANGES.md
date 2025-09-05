# Privacy-First UI-TARS Fork

This fork of UI-TARS-desktop has been modified to remove all surveillance and tracking components for GLB/WISP compliance.

## Changes Made

### 🚨 **Removed Analytics & Tracking**
- ✅ Removed **PostHog analytics** from example applications
- ✅ Removed **Vercel Analytics** tracking 
- ✅ Replaced **machine ID generation** with session-based random IDs
- ✅ Removed all user behavior tracking calls

### ⚡ **Disabled Auto-Updates**  
- ✅ Disabled automatic update checking that sent system info to GitHub
- ✅ Users can still manually check for updates if desired
- ✅ No automatic network calls for version checking

### 🔐 **Privacy-Friendly Authentication**
- ✅ Replaced hardware fingerprinting with random session IDs
- ✅ Device registration system disabled (proxy host is empty)
- ✅ No persistent device identification

### 📊 **No Telemetry**
- ✅ Confirmed no active telemetry collection in codebase
- ✅ Documentation mentions for telemetry updated
- ✅ No usage analytics transmitted

## What Still Works

✅ **All core GUI automation functionality**
- Screen capture and control
- AI-powered automation via OpenAI/Claude APIs
- Browser automation  
- System permission management

✅ **Local-first operation**
- All data processing happens on your machine
- AI API calls only when you explicitly run automations
- No background data collection

## What Was Removed

❌ User behavior tracking
❌ Device fingerprinting  
❌ Automatic update surveillance
❌ Usage analytics transmission
❌ Session recordings
❌ Performance metrics collection

## AI API Usage

**Note**: The tool still sends screenshots and user instructions to AI providers (OpenAI/Anthropic) when you run automations. This is necessary for the core functionality. 

**To minimize data exposure:**
- Use local AI models when possible
- Review screenshots before sending
- Be aware that your automation tasks are sent to third-party AI services

## Installation

1. Clone this privacy-focused fork
2. Follow normal installation procedures  
3. Set your AI provider API keys
4. Enjoy surveillance-free GUI automation!

## Compliance Status

✅ **GLB/WISP Compliant** - No unauthorized data collection
✅ **Privacy-first** - Minimal external data transmission
✅ **Transparent** - Clear documentation of any third-party communication

---

*This fork prioritizes user privacy while maintaining full automation capabilities.*