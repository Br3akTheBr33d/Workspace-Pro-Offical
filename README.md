<div align="center">

<img src="assets/workspace-pro-with-text.png" alt="Workspace Pro" width="560" />

[![Version](https://img.shields.io/badge/version-1.2.0-crimson?style=flat-square)](https://workspace-pro.app)
[![Chrome Web Store](https://img.shields.io/badge/Chrome%20Web%20Store-Live-1a73e8?style=flat-square&logo=google-chrome&logoColor=white)](https://chrome.google.com/webstore/detail/jplhkjcdmpchejmdjjdckpbhdognoknm)
[![Works on](https://img.shields.io/badge/Works%20on-Chrome%20%7C%20Brave%20%7C%20Edge-555?style=flat-square)](https://workspace-pro.app)
[![License](https://img.shields.io/badge/license-Proprietary-555?style=flat-square)](https://workspace-pro.app/terms)

**Your Browser. Your Rules.**

Tab & session management for power users — built for developers, homelab enthusiasts, and IT professionals.

[Website](https://workspace-pro.app) · [Documentation](https://workspace-pro.app/docs) · [Chrome Web Store](https://chrome.google.com/webstore/detail/jplhkjcdmpchejmdjjdckpbhdognoknm) · [Report a Bug](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=bug_report.yml) · [Request a Feature](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=feature_request.yml)

</div>

---

## Workspace Pro v1.2.0 — Live on the Chrome Web Store

Workspace Pro turns every new tab into a local-first command center for your browser. Organize tabs into workspaces and collections, restore saved sessions, keep a personal searchable Wiki of clipped pages, and use an optional Pro dashboard for multi-provider AI tools, widgets, and private Google Drive sync.

**v1.2.0** extends that workspace to your phone and your AI tools: Mobile Companion on phone and tablet, Agent Connect for MCP clients, and encrypted two-way Google Drive sync with recovery and rotation.

> Built for power users who live in the browser. Works on Chrome, Brave, Edge, and other Chromium-based browsers.

<img src="assets/dashboard.png" alt="Workspace Pro v1.2.0 dashboard with productivity widgets" width="100%" />

---

## Features in v1.2.0

### Free

| Feature | What it does |
|---|---|
| **Workspaces & Collections** | Organize projects, clients, and contexts; save tabs with notes and sticky notes. |
| **Session History** | Keep up to 50 saved browser sessions and restore them when needed. |
| **Current Session** | Search and manage your currently open tabs. |
| **Personalization** | Eight dark-first themes, custom colors, readability controls, and English, German, or Spanish UI. |
| **Local-first data** | Workspace data remains on your device by default. |

### Pro

| Feature | What it does |
|---|---|
| **Unlimited organization** | Remove free-tier workspace and collection limits. |
| **Personal Wiki** | Clip pages into a local, full-text-searchable knowledge base with tags, `[[wikilinks]]`, backlinks, and a visual graph. |
| **AI tab tools** | Group tabs by category, domain, or your AI provider and summarize open tabs. |
| **Workspace Pro Assistant** | Chat with your own Claude, OpenAI, or OpenRouter key, browse live model lists, attach files, and act on contextual browser and Wiki tools. |
| **Dashboard widgets** | Add, resize, and arrange Clock & Timer, Weather, News, Notepad, Assistant, Countdown, and Quick Links widgets. |
| **Tab Resource Monitor** | Find memory-heavy tabs quickly; Sessions view unifies tabs, windows, groups, and memory. |
| **Mobile Companion** | Workspaces, Collections, Wiki, and Widgets on phone and tablet with encrypted two-way sync over private Google Drive AppData — the unlock key stays on your devices. |
| **Agent Connect** | MCP server for AI clients (Hermes, OpenClaw, Claude Desktop/Code, Cursor, Codex, and any MCP client). With browser (live tabs via Cloudflare Rendezvous) or Without computer / Drive MCP (Wiki, Workspaces, Collections, bookmarks, notes). Pair under Settings → Agent Bridge. |
| **Encrypted Google Drive sync** | Drive Envelope v2, Recovery Key / Recovery Hub, key rotation, sync-merge, and versioned restore points in a private Drive AppData folder. |

<p align="center"><img src="assets/popup-assistant.png" alt="Workspace Pro Assistant in the browser popup" width="380" /></p>

---

## Mobile Companion

Your workspaces now fit in your pocket. The [Mobile Companion](https://app.workspace-pro.app) is a progressive web app for phones and tablets — Workspaces, Collections, Wiki, and Widgets, installed from the browser with no app-store account.

Data syncs through your own encrypted Google Drive AppData file. The unlock key travels in the pairing URL fragment (QR) and never reaches a Workspace Pro server — it lives on your devices.

<p align="center">
  <img src="assets/companion-home.png" alt="Workspace Pro Mobile Companion home screen" width="280" />
  &nbsp;&nbsp;
  <img src="assets/companion-workspaces.png" alt="Workspace Pro Mobile Companion workspaces" width="280" />
</p>

[Open the Companion →](https://app.workspace-pro.app) · [News & overview →](https://workspace-pro.app/news.html)

---

## Agent Connect

Workspace Pro is an MCP server your AI can use. Agent Connect works with Hermes, OpenClaw, Claude Desktop, Claude Code, Cursor, Codex, and any MCP-compatible client.

| Mode | What you get |
|---|---|
| **With browser** | Live tabs and browser context via Cloudflare Rendezvous while Chrome is on. |
| **Without computer / Drive MCP** | Wiki, Workspaces, Collections, bookmarks, and notes against your encrypted Google Drive — no live tabs. |

Pairing is one paste from **Settings → Agent Bridge**. The pairing code is chat-safe and expires in about ten minutes.

[Agent Connect docs →](https://workspace-pro.app/docs#doc-agent-connect) · [Agent Connect page →](https://workspace-pro.app/agent-connect.html)

---

## Personal Wiki

Clip any page from the dashboard or popup and it becomes a local Wiki page — Markdown content, editable metadata, tags, and notes, all stored on your device. Full-text search supports operators like `tag:`, `title:`, and `-exclude`, pages link to each other with `[[wikilinks]]`, and a visual graph shows how everything connects.

<img src="assets/wiki-list.png" alt="Workspace Pro Wiki list grouped by workspace and collection" width="100%" />

<img src="assets/wiki-graph.png" alt="Workspace Pro Wiki knowledge graph" width="100%" />

Bring in existing notes with **bulk import** (Markdown, text, Word, Excel, and images) in one batch, or export any page — or the whole Wiki — as Obsidian-compatible Markdown.

<img src="assets/wiki-import.png" alt="Workspace Pro Wiki bulk import" width="100%" />

Everything above is local and works without AI. If you add your own provider key, optional **Compile**, **Lint**, and **Ask Wiki** workflows can synthesize new pages, flag orphaned or broken links, and answer questions grounded only in your own Wiki content — every AI call is opt-in, requires explicit consent, and is logged in an activity log you can review.

<img src="assets/wiki-ai-tools.png" alt="Workspace Pro Wiki optional AI compile workflow" width="100%" />

[Read the full Wiki guide in the documentation →](https://workspace-pro.app/docs#doc-wiki)

---

## Dashboard widgets

| Widget | Highlights |
|---|---|
| **Clock & Timer** | World clocks, stopwatch, timer, and alarms. |
| **Weather** | Five-day forecast from Open-Meteo; no API key required. |
| **News** | RSS-based tech and AI news with topic filters. |
| **Notepad** | Multi-page rich text notes with headings and lists. |
| **Workspace Pro Assistant** | Persistent AI chat using your Claude, OpenAI, or OpenRouter key. |
| **Countdown** | Recurring deadlines with Chrome notifications. |
| **Quick Links** | Pinned shortcuts with favicons and emoji. |

---

## Keyboard shortcuts

| Action | Windows / Linux | Mac |
|---|---|---|
| Open Popup | `Ctrl + Shift + 1` | `⌘ + Shift + 1` |
| Open Dashboard | `Ctrl + Shift + 2` | `⌘ + Shift + 2` |
| Open Workspace Pro Assistant | `Ctrl + Shift + 9` | `⌘ + Shift + 9` |
| Close any modal | `Esc` | `Esc` |
| Save a form | `Enter` | `Enter` |
| Save a note | `Ctrl + Enter` | `⌘ + Enter` |

Default shortcuts can be changed in `chrome://extensions/shortcuts`.

---

## Privacy, sync, and backup

Workspace Pro has no analytics, tracking, or advertising. The Wiki is stored locally like the rest of your workspace data. Optional AI actions (tab tools, Assistant, or Wiki Compile/Lint/Ask) send only the content needed for the action you explicitly start, to the provider you configured.

Optional **encrypted two-way Google Drive sync** writes ciphertext to the private AppData folder (not visible in "My Drive"), uses authenticated Drive Envelope v2, supports Recovery Key / Recovery Hub and transactional key rotation, keeps versioned restore points, and merges edits from desktop and Mobile Companion instead of overwriting. License validation uses a pseudonymous device token rather than workspace data.

<img src="assets/drive-snapshots.png" alt="Workspace Pro Google Drive versioned restore points" width="100%" />

[Drive encryption docs →](https://workspace-pro.app/docs#doc-drive-encryption) · [Encryption overview →](https://workspace-pro.app/encryption.html) · [Privacy Policy](https://workspace-pro.app/privacy-policy) · [Terms of Service](https://workspace-pro.app/terms)

---

## Pricing

**Start free. Upgrade when you need more.**

| | Free | Pro |
|---|---|---|
| **Price** | €0 | One-time license key |
| **Workspaces** | 1 | Unlimited |
| **Collections** | 1 per workspace | Unlimited |
| **Session History** | Up to 50 saves | Up to 50 saves |
| **Themes & languages** | All themes; EN / DE / ES | All themes; EN / DE / ES |
| **Wiki, widgets, AI & Drive sync** | — | Included |
| **Mobile Companion** | — | Included |
| **Agent Connect** | — | Included |

[Get Pro License →](https://workspace-pro.app/#pricing)

---

## Bug reports and feature requests

This repository is the public issue tracker for Workspace Pro.

- **Found a bug?** → [Open a Bug Report](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=bug_report.yml)
- **Have an idea?** → [Request a Feature](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=feature_request.yml)
- **Need help?** → [Contact support](https://workspace-pro.app/contact) or email [support@workspace-pro.app](mailto:support@workspace-pro.app)

---

<div align="center">

© 2026 Workspace Pro · [workspace-pro.app](https://workspace-pro.app)

*Not affiliated with Google, Brave Software, or Microsoft.*

</div>
