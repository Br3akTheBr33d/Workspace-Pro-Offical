# Public Repository README Refresh Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Refresh the public Workspace Pro issue-tracker README with July 2026 product information while retaining v1.0.8 as the sole live Chrome Web Store release.

**Architecture:** The existing GitHub information repository remains deliberately small. A rewritten `README.md` describes the live v1.0.8 release first, then separates a clearly unreleased v1.1.0 preview; four relative PNG assets illustrate the product without copying the marketing site or extension source.

**Tech Stack:** GitHub Markdown, PNG assets, Node.js built-in assertions, Git.

## Global Constraints

- `v1.0.8` is the current live Store release.
- `v1.1.0` must be described only as a preview/coming-soon release.
- Do not include proprietary extension code or copy the full website.
- Keep bug-report and feature-request links prominent and leave issue templates unchanged.
- README images must use relative `assets/...` paths.

---

### Task 1: Add current product screenshots

**Files:**
- Create: `assets/dashboard-overview.png`
- Create: `assets/wiki-graph.png`
- Create: `assets/popup-assistant.png`
- Create: `assets/drive-snapshots.png`

**Interfaces:**
- Consumes: four PNGs in `website-july-2026/files/`.
- Produces: paths embedded by Task 2: `assets/dashboard-overview.png`, `assets/wiki-graph.png`, `assets/popup-assistant.png`, `assets/drive-snapshots.png`.

- [ ] **Step 1: Verify the four curated source images before copying**

```bash
test -s /Users/tim/Programming/Git/Projects/Chrome-Extensions/Workspace-Pro/website-july-2026/files/overview.png
test -s /Users/tim/Programming/Git/Projects/Chrome-Extensions/Workspace-Pro/website-july-2026/files/wiki-graph.png
test -s /Users/tim/Programming/Git/Projects/Chrome-Extensions/Workspace-Pro/website-july-2026/files/popup-assistant.png
test -s /Users/tim/Programming/Git/Projects/Chrome-Extensions/Workspace-Pro/website-july-2026/files/drive-snapshots.png
```

Expected: all commands exit `0`.

- [ ] **Step 2: Copy the selected sources under the final public names**

```bash
cp /Users/tim/Programming/Git/Projects/Chrome-Extensions/Workspace-Pro/website-july-2026/files/overview.png assets/dashboard-overview.png
cp /Users/tim/Programming/Git/Projects/Chrome-Extensions/Workspace-Pro/website-july-2026/files/wiki-graph.png assets/wiki-graph.png
cp /Users/tim/Programming/Git/Projects/Chrome-Extensions/Workspace-Pro/website-july-2026/files/popup-assistant.png assets/popup-assistant.png
cp /Users/tim/Programming/Git/Projects/Chrome-Extensions/Workspace-Pro/website-july-2026/files/drive-snapshots.png assets/drive-snapshots.png
file assets/dashboard-overview.png assets/wiki-graph.png assets/popup-assistant.png assets/drive-snapshots.png
```

Expected: each destination reports `PNG image data`.

- [ ] **Step 3: Commit the independently reviewable asset addition**

```bash
git add assets/dashboard-overview.png assets/wiki-graph.png assets/popup-assistant.png assets/drive-snapshots.png
git commit -m "docs: add current product screenshots"
```

### Task 2: Replace the stale README with the public product overview

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: exact asset names created by Task 1.
- Produces: a README with the headings `Workspace Pro v1.0.8 — Live on the Chrome Web Store`, `Features in v1.0.8`, `Dashboard widgets`, `Keyboard shortcuts`, `Privacy and backup`, `Coming in v1.1.0`, `Pricing`, and `Bug reports and feature requests`.

- [ ] **Step 1: Run the failing public-release regression checks**

```bash
node --input-type=module -e "import fs from 'node:fs'; import assert from 'node:assert/strict'; const s=fs.readFileSync('README.md','utf8'); assert.match(s,/version-1\\.0\\.8/); assert.match(s,/Chrome%20Web%20Store-Live/); assert.match(s,/Ctrl \\+ Shift \\+ 9/); assert.match(s,/## Coming in v1\\.1\\.0/); assert.match(s,/not part of the published v1\\.0\\.8 Chrome Web Store release/);"
```

Expected: FAIL because the existing README contains `version-1.0.0`, a Coming Soon Store badge, no Assistant shortcut, and no release-boundary warning.

- [ ] **Step 2: Write the live v1.0.8 header and navigation block**

Replace the current top block with this exact Markdown:

```markdown
<div align="center">

<img src="assets/workspace-pro-with-text.png" alt="Workspace Pro" width="560" />

[![Version](https://img.shields.io/badge/version-1.0.8-crimson?style=flat-square)](https://workspace-pro.app)
[![Chrome Web Store](https://img.shields.io/badge/Chrome%20Web%20Store-Live-1a73e8?style=flat-square&logo=google-chrome&logoColor=white)](https://chrome.google.com/webstore/detail/jplhkjcdmpchejmdjjdckpbhdognoknm)
[![Works on](https://img.shields.io/badge/Works%20on-Chrome%20%7C%20Brave%20%7C%20Edge-555?style=flat-square)](https://workspace-pro.app)
[![License](https://img.shields.io/badge/license-Proprietary-555?style=flat-square)](https://workspace-pro.app/terms)

**Your Browser. Your Rules.**

Tab & session management for power users — built for developers, homelab enthusiasts, and IT professionals.

[Website](https://workspace-pro.app) · [Documentation](https://workspace-pro.app/docs) · [Chrome Web Store](https://chrome.google.com/webstore/detail/jplhkjcdmpchejmdjjdckpbhdognoknm) · [Report a Bug](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=bug_report.yml) · [Request a Feature](https://github.com/Br3akTheBr33d/Workspace-Pro-Offical/issues/new?template=feature_request.yml)

</div>
```

- [ ] **Step 3: Write the product, feature, widget, shortcut, privacy, preview, pricing, and support sections**

Use these exact content requirements in `README.md`:

```markdown
## Workspace Pro v1.0.8 — Live on the Chrome Web Store

Workspace Pro turns every new tab into a local-first command center for your browser. Organize tabs into workspaces and collections, restore saved sessions, and use an optional Pro dashboard for AI tools, widgets, and private Google Drive backup.

<img src="assets/dashboard-overview.png" alt="Workspace Pro v1.0.8 dashboard with productivity widgets" width="100%" />

## Features in v1.0.8

Use Free and Pro tables covering: Workspaces & Collections; Session History; Current Session; Personalization; Local-first data; unlimited organization; AI tab grouping and summaries; the Assistant with user-provided provider key; widgets; resource monitoring; and private Drive AppData backup with restore points.

## Dashboard widgets

List Clock & Timer, Weather, News, Notepad, Workspace Pro Assistant, Countdown, and Quick Links in a two-column table.

<p align="center"><img src="assets/popup-assistant.png" alt="Workspace Pro Assistant in the browser popup" width="380" /></p>

## Keyboard shortcuts

| Action | Windows / Linux | Mac |
|---|---|---|
| Open Popup | `Ctrl + Shift + 1` | `⌘ + Shift + 1` |
| Open Dashboard | `Ctrl + Shift + 2` | `⌘ + Shift + 2` |
| Open Workspace Pro Assistant | `Ctrl + Shift + 9` | `⌘ + Shift + 9` |
| Close any modal | `Esc` | `Esc` |
| Save a form | `Enter` | `Enter` |
| Save a note | `Ctrl + Enter` | `⌘ + Enter` |

## Privacy and backup

State that there is no analytics, tracking, or advertising; AI requests are opt-in and use only action-selected content; Drive uses private AppData; and licence validation does not use workspace data.

<img src="assets/drive-snapshots.png" alt="Workspace Pro Google Drive versioned restore points" width="100%" />

## Coming in v1.1.0

> **Preview only:** v1.1.0 is in development and is **not part of the published v1.0.8 Chrome Web Store release**. Screens and wording may change before release.

Describe the upcoming Pro Wiki as a local searchable knowledge base with clipping, full-text search, tags, wikilinks, backlinks, graph, Markdown export, and optional provider-key AI Compile, Lint, and Ask Wiki. Mention Assistant coverage, popup improvements, and richer Drive restore controls.

<img src="assets/wiki-graph.png" alt="Preview of the Workspace Pro Wiki knowledge graph" width="100%" />

## Pricing

Keep the existing Free versus one-time Pro model; include 1 versus unlimited workspaces, 1-per-workspace versus unlimited collections, 50 saved sessions, all themes/languages, and Pro-only widgets/AI/Drive.

## Bug reports and feature requests

Keep the existing Bug Report, Feature Request, contact, and support-email destinations.
```

- [ ] **Step 4: Re-run the structural checks and inspect version boundaries**

```bash
node --input-type=module -e "import fs from 'node:fs'; import assert from 'node:assert/strict'; const s=fs.readFileSync('README.md','utf8'); assert.match(s,/version-1\\.0\\.8/); assert.match(s,/Chrome%20Web%20Store-Live/); assert.match(s,/Ctrl \\+ Shift \\+ 9/); assert.match(s,/## Coming in v1\\.1\\.0/); assert.match(s,/not part of the published v1\\.0\\.8 Chrome Web Store release/); for (const p of ['assets/dashboard-overview.png','assets/wiki-graph.png','assets/popup-assistant.png','assets/drive-snapshots.png']) assert.match(s,new RegExp(p.replace('.', '\\\\.')));"
rg -n "v1\.0\.8|v1\.1\.0|Coming soon|Chrome Web Store" README.md
```

Expected: all assertions pass; v1.0.8 is live and v1.1.0 occurs only in the preview section and its warning.

- [ ] **Step 5: Commit the independently reviewable README update**

```bash
git add README.md
git commit -m "docs: refresh public product overview for v1.0.8"
```

### Task 3: Verify and publish the public-repository update

**Files:**
- Verify: `README.md`
- Verify: `assets/dashboard-overview.png`
- Verify: `assets/wiki-graph.png`
- Verify: `assets/popup-assistant.png`
- Verify: `assets/drive-snapshots.png`
- Verify: `.github/ISSUE_TEMPLATE/bug_report.yml`
- Verify: `.github/ISSUE_TEMPLATE/feature_request.yml`

**Interfaces:**
- Consumes: committed tasks 1 and 2.
- Produces: a clean main branch ready for GitHub.

- [ ] **Step 1: Validate images, links, issue templates, and whitespace**

```bash
node --input-type=module -e "import fs from 'node:fs'; import assert from 'node:assert/strict'; const s=fs.readFileSync('README.md','utf8'); for (const p of ['assets/dashboard-overview.png','assets/wiki-graph.png','assets/popup-assistant.png','assets/drive-snapshots.png']) assert.ok(fs.existsSync(p), 'missing '+p); assert.match(s,/https:\/\/chrome\.google\.com\/webstore\/detail\/jplhkjcdmpchejmdjjdckpbhdognoknm/); assert.ok(fs.existsSync('.github/ISSUE_TEMPLATE/bug_report.yml')); assert.ok(fs.existsSync('.github/ISSUE_TEMPLATE/feature_request.yml'));"
git diff HEAD~2..HEAD --check
git status --short
```

Expected: all assertions pass, `git diff --check` has no output, and `git status --short` has no output.

- [ ] **Step 2: Push the two content commits to the public repository**

```bash
git push origin main
```

Expected: Git reports both commits pushed to `https://github.com/Br3akTheBr33d/Workspace-Pro-Offical.git`.
