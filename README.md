<div align="center">

<img src="https://raw.githubusercontent.com/Br3akTheBr33d/Workspace-Pro-Offical/main/assets/logo.png" alt="Workspace Pro" width="560" />

[![Version](https://img.shields.io/badge/version-1.0.0-crimson?style=flat-square)](https://workspace-pro.app)
[![Chrome Web Store](https://img.shields.io/badge/Chrome%20Web%20Store-Coming%20Soon-555?style=flat-square&logo=google-chrome&logoColor=white)](https://workspace-pro.app)
[![Works on](https://img.shields.io/badge/Works%20on-Chrome%20%7C%20Brave%20%7C%20Edge-555?style=flat-square)](https://workspace-pro.app)
[![License](https://img.shields.io/badge/license-Proprietary-555?style=flat-square)](https://workspace-pro.app/terms)

**Your Browser. Your Rules.**

Tab & session management for power users — built for developers, homelab enthusiasts, and IT professionals.

[Website](https://workspace-pro.app) · [Documentation](https://workspace-pro.app/docs) · [Report a Bug](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=bug_report.yml) · [Request a Feature](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=feature_request.yml)

</div>

---

## What is Workspace Pro?

Workspace Pro is a Chrome extension that turns every new tab into a full **command center for your browser**. It brings context-aware tab organization, AI-powered grouping, session history, and a live productivity dashboard — all local-first, with optional cloud backup.

> Built for power users who live in the browser. Works on Chrome, Brave, Edge, and all Chromium-based browsers.

<div align="center">
<img src="https://raw.githubusercontent.com/Br3akTheBr33d/Workspace-Pro-Offical/main/assets/dashboard.png" alt="Workspace Pro Dashboard" width="100%" />
</div>

---

## Features

### Core Features (Free)

| Feature | Description |
|---|---|
| **Workspaces** | Create isolated environments for every project, client, or context |
| **Collections** | Group related tabs with rich notes and sticky notes |
| **Session History** | Auto-saves up to 50 browser sessions — restore any of them with one click |
| **Current Session View** | Live overview of all open tabs with search and management |
| **8 Themes** | Crimson, Matrix, Blood Moon, Void Red, Inferno, Ocean, Forest, Aurora — all dark-first |
| **Custom Colors** | Set your own background and accent color for a fully personalized look |
| **Multi-Language UI** | Full interface in English, German, and Spanish |

### Pro Features

| Feature | Description |
|---|---|
| **Unlimited Workspaces & Collections** | No limits on how you organize |
| **AI Tab Grouping** | Claude intelligently groups your open tabs by topic |
| **AI Tab Summarize** | Summarize all open tabs with a single click |
| **Workspace Pro Assistant** | Built-in AI assistant using Haiku or Sonnet — your own API key |
| **File Attachments in Chat** | Attach images, PDFs, and text files directly to your AI conversations |
| **RAM-based Tab Sorting** | Sort open tabs by memory usage to find and close heavy tabs fast |
| **Dashboard Widgets** | Clock & Timer, Weather, News Feed, Notepad, Assistant, Countdown, Quick Links |
| **Google Drive Backup** | Auto-sync to a private AppData folder — invisible in "My Drive" |
| **License Key Activation** | Ed25519-based offline validation with periodic revocation checks |

---

## Dashboard Widgets

The Pro dashboard comes with 7 fully customizable widgets you can add, remove, and rearrange freely:

- **Clock & Timer** — World clocks, multi-timezone, analog display, alarms and countdown timer
- **Weather** — 5-day forecast via Open-Meteo. No API key needed
- **News** — AI/Tech RSS from 15+ sources with topic search
- **Notepad** — Multi-page rich text with bold, lists, and headings
- **Workspace Pro Assistant** — AI chat with Haiku or Sonnet, your own key, file attachments
- **Countdown** — Visual countdown timer with notifications
- **Quick Links** — Pinned links and shortcuts for instant access

---

## How it Works

1. **Install** the extension from the Chrome Web Store (coming soon)
2. **Open the popup** via the toolbar icon or `Ctrl+Shift+1` (`⌘+Shift+1` on Mac)
3. **Open the dashboard** via `Ctrl+Shift+2` (`⌘+Shift+2` on Mac)
4. **Create Workspaces** to organize your tabs by project or context
5. **Save Sessions** to never lose your browser state again
6. **Upgrade to Pro** for AI features, unlimited workspaces, and cloud backup

---

## Keyboard Shortcuts

| Action | Windows / Linux | Mac |
|---|---|---|
| Open Popup | `Ctrl + Shift + 1` | `⌘ + Shift + 1` |
| Open Dashboard | `Ctrl + Shift + 2` | `⌘ + Shift + 2` |
| Close any modal | `Esc` | `Esc` |
| Save form | `Enter` | `Enter` |
| Save note (textarea) | `Ctrl + Enter` | `⌘ + Enter` |
| Tab context menu | `Right-click` | `Right-click` |

---

## Pricing

**Start free. Upgrade when you need more.**

| | Free | Pro |
|---|---|---|
| **Price** | $0 forever | One-time license key |
| **Workspaces** | 1 | Unlimited |
| **Collections** | 1 per Workspace | Unlimited |
| **Session History** | Up to 50 saves | Up to 50 saves |
| **Themes** | All 8 + Custom Colors | All 8 + Custom Colors |
| **Language** | EN / DE / ES | EN / DE / ES |
| **Dashboard Widgets** | — | All 7 |
| **AI Tab Grouping** | — | ✓ |
| **AI Tab Summarize** | — | ✓ |
| **Workspace Pro Assistant** | — | ✓ |
| **File Attachments in Chat** | — | ✓ |
| **RAM-based Tab Sorting** | — | ✓ |
| **Google Drive Backup** | — | ✓ |

> **Pro licenses are validated locally** using Ed25519 cryptography. A periodic revocation check runs every 4 hours against `license.workspace-pro.app` — transmitting only a device token, no personal data or browsing history. License activation data (device ID, email) is stored on the license server for the duration of your license and deleted upon request.

[Get Pro License →](https://workspace-pro.app/#pricing)

---

## Privacy

Workspace Pro is **local-first**. All your workspaces, tabs, and sessions are stored in your browser's local storage.

- No account required
- No data sent to external servers (except optional Google Drive sync and AI features you enable yourself)
- AI features (tab grouping, Workspace Pro Assistant) use your own Anthropic API key
- Not affiliated with Google, Brave Software, or Microsoft

[Privacy Policy](https://workspace-pro.app/privacy-policy) · [Terms of Service](https://workspace-pro.app/terms)

---

## Compatibility

Works on any Chromium-based browser with Manifest V3 support:

- Google Chrome
- Brave
- Microsoft Edge

---

## Bug Reports & Feature Requests

This repository is the public issue tracker for Workspace Pro.

- **Found a bug?** → [Open a Bug Report](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=bug_report.yml)
- **Have an idea?** → [Request a Feature](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=feature_request.yml)
- **Question or support?** → [Contact us](https://workspace-pro.app/contact) or email [support@workspace-pro.app](mailto:support@workspace-pro.app)

---

<div align="center">

© 2026 Workspace Pro · [workspace-pro.app](https://workspace-pro.app)

*Not affiliated with Google, Brave Software, or Microsoft.*

</div>
