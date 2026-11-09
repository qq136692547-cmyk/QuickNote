<p align="center">
  <img src="https://quicknote-official.pages.dev/assets/app-logo.png?v=2" alt="QuickNote Logo" width="108" height="108" style="border-radius: 24px; box-shadow: 0 8px 32px rgba(56, 189, 248, 0.25);" />
</p>

<h1 align="center">QuickNote (随身记)</h1>

<p align="center">
  <b>The Blazing-Fast, 100% Offline-First AI Scratchpad for Developers.</b><br>
  <i>Summon your external brain in <b>0.1s</b> anywhere in Windows with <code>Ctrl+Shift+Q</code>. Zero telemetry. Zero SaaS lock-in.</i>
</p>

<p align="center">
  <a href="https://github.com/qq136692547-cmyk/QuickNote/releases"><img src="https://img.shields.io/badge/Release-v0.1.0-sky.svg?style=flat-square&logo=windows" alt="Release v0.1.0" /></a>
  <a href="https://github.com/qq136692547-cmyk/QuickNote/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-Freemium%20%2F%20Commercial-blue.svg?style=flat-square" alt="License" /></a>
  <img src="https://img.shields.io/badge/Built%20with-Rust%20%2B%20Tauri-orange.svg?style=flat-square&logo=rust" alt="Rust" />
  <img src="https://img.shields.io/badge/Storage-100%25%20Offline%20SQLite-003B57.svg?style=flat-square&logo=sqlite" alt="SQLite" />
  <img src="https://img.shields.io/badge/AI%20Engine-DeepSeek--V4.1%20Flash-indigo.svg?style=flat-square" alt="DeepSeek" />
  <a href="https://quicknote-official.pages.dev"><img src="https://img.shields.io/badge/Website-Live%20Demo-emerald.svg?style=flat-square&logo=cloudflare" alt="Website" /></a>
  <a href="https://dengli.gumroad.com/l/quicknote-pro"><img src="https://img.shields.io/badge/Gumroad-Pro%20Lifetime%20%2429-FF90E8.svg?style=flat-square&logo=gumroad" alt="Gumroad" /></a>
</p>

<p align="center">
  <a href="#-quickstart--installation">⚡ Quickstart</a> •
  <a href="#-killer-features">✨ Key Features</a> •
  <a href="#-why-quicknote-vs-others">⚔️ Comparison</a> •
  <a href="#-dual-track-ai-architecture">🤖 AI Architecture</a> •
  <a href="#-offline-first-privacy-manifesto">🛡️ Privacy</a> •
  <a href="https://quicknote-official.pages.dev">🌐 Official Website</a>
</p>

---

## ⚡ Why QuickNote?

How many times a day do you break your coding flow state?
- You need to temporarily stash an API secret, a regex snippet, or a curl command;
- You need to draft a prompt for an LLM and find yourself opening a browser tab, fighting with a 500MB Electron app, or searching for Notepad;
- You're worried about cloud-based note apps scanning your uncommitted credentials or internal database schemas.

**QuickNote was engineered from scratch in Rust to eliminate this friction entirely.**  
Hit `Ctrl+Shift+Q`. A sleek, dark-mode acrylic scratchpad appears over your active IDE in **< 100ms**. Take notes, optimize your prompt with one click, pin it as a floating cheat sheet, or press `Esc` to disappear. Your notes stay encrypted on your SSD in a local SQLite vault.

---

## ✨ Killer Features

### ⚡ 0.1s Global Summoning (`Ctrl+Shift+Q`)
Slides out immediately from the edge of your screen over full-screen IDEs, debuggers, games, or terminals. Dismisses back to tray without stealing window focus.

### 🔒 100% Offline-First SQLite Local Vault
Zero accounts required. Zero telemetry pings. All notes, tags, and timestamps are persisted in a clean, local SQLite database with `WAL` journaling and `FTS5` full-text search (< 2ms query time across 50,000 notes).

### 📌 Always-on-Top Floating Pin Card
Pin critical API endpoints, SQL query templates, or meeting action items directly over your workspace with customizable acrylic opacity.

### 🤖 Dual-Track AI Engine (No SaaS Hostage)
Never worry about losing your AI tools if a subscription expires:
- **Official Cloud Channel**: Included with Pro — 100 high-speed daily requests via official DeepSeek-V4.1 Flash.
- **BYOK (Bring Your Own Key) Freedom**: Enter your own DeepSeek, OpenAI, or local Ollama endpoint (`http://localhost:11434/v1`) for **unlimited, uncapped lifetime usage**.

### ✨ 1-Click System Prompt Polish
Paste raw, sloppy thoughts and let QuickNote automatically restructure them into battle-tested System Prompts with **Role**, **Task Context**, **Strict Constraints**, and **Standardized Output Formats**.

### 🖼️ Multimodal Vision OCR Code Extractor
Drag & drop screenshots of code, JSON payloads, or tabular data directly into QuickNote for instant Markdown extraction.

### 🛡️ Mathematically Secure Ed25519 Licensing
Pro editions use asymmetric Ed25519 cryptographic signatures. Activates completely offline on up to 3 personal machines with **zero central verification server**.

---

## ⚔️ Why QuickNote vs. Others?

| Feature | QuickNote (随身记) | Notion / Obsidian | Windows Sticky Notes | Typical Electron Apps |
| :--- | :---: | :---: | :---: | :---: |
| **Launch Speed** | **< 100ms (Rust Native)** | 2.5s – 6s | ~800ms | 3s – 8s |
| **RAM Usage** | **~25 MB** | 350 MB – 1.2 GB | ~90 MB | 450 MB – 1.5 GB |
| **Global Summon Hotkey** | **Yes (`Ctrl+Shift+Q`)** | No (3rd-party plugin) | No | Rarely |
| **100% Offline Privacy** | **Yes (Local SQLite)** | Depends on cloud sync | Cloud synced | Depends |
| **Native DeepSeek AI** | **Yes (Dual-track + BYOK)** | Extra monthly fee | None | Add-on plugins |
| **Prompt Refiner & OCR** | **Built-in** | Manual copy-paste | None | None |
| **Pricing Model** | **Free Forever / $29 Lifetime** | $10–$20/mo subscription | Free (Barebones) | Heavy subscriptions |

---

## ⚡ Quickstart & Installation

### Option 1: Direct Download (Recommended)
Download the latest pre-compiled binaries from our official mirror or GitHub Releases:

- **[Download Portable Green Edition (.zip)](https://quicknote-official.pages.dev/downloads/QuickNote_v0.1.0_x64_Portable.zip)** — Extract and run anywhere (ideal for USB sticks, zero registry changes).
- **[Download Windows Installer (.exe)](https://quicknote-official.pages.dev/downloads/QuickNote_v0.1.0_x64_Installer.exe)** — Complete setup wizard with desktop shortcuts.

### Option 2: Windows Package Manager (Winget)
*(Manifest submission in progress)*
```powershell
winget install quicknote
```

### Option 3: Scoop Package Manager
```powershell
scoop bucket add extras
scoop install quicknote
```

---

## 🛡️ Offline-First Privacy Manifesto

1. **No Analytics**: QuickNote contains zero telemetry trackers, Google Analytics, or third-party tracking pixels.
2. **Local Credentials**: When using BYOK mode, your API keys are masked and stored solely in your local SQLite file.
3. **Transparent Network Traffic**: When running in offline mode, QuickNote makes 0 outbound network requests. You can verify this using Wireshark, Windows Resource Monitor, or Fiddler.

---

## 💎 Pricing & Pro Tier

QuickNote is built under an **Open-Core & Commercial Lifetime** philosophy:
- **Free Edition ($0 forever)**: Unlimited offline notes, full SQLite vault, tags, FTS5 instant search, global hotkey, pin cards.
- **Lifetime Pro ($29 one-time purchase)**: Unlocks the full AI suite (Prompt Refiner, Vision OCR, Web Summarizer), 1 full year of 100 requests/day official DeepSeek AI cloud channel, and lifetime uncapped BYOK mode.

👉 **[Get Pro Lifetime License ($29) on Gumroad](https://dengli.gumroad.com/l/quicknote-pro)**  
*(Instant delivery with strictly signed Ed25519 license key. 7-day 100% money-back guarantee).*

---

## 🗺️ Roadmap & Community

- [x] v0.1.0: Rust + Tauri native architecture, SQLite FTS5 search, 0.1s global hotkey.
- [x] v0.1.0: Cloudflare Worker serverless AI gateway & Ed25519 cryptographic licensing.
- [ ] v0.2.0: Clipboard history snippet manager with regex auto-detection.
- [ ] v0.2.0: Local Ollama / vLLM model auto-discovery on `localhost`.
- [ ] v0.3.0: Community-driven Prompt Template marketplace.

Give us a **⭐️ Star** if QuickNote saves you even 5 minutes a day!

---

## 💬 Support & Contact

- **Official Website**: [https://quicknote-official.pages.dev](https://quicknote-official.pages.dev)
- **Email Support**: [support@quicknote.dev](mailto:support@quicknote.dev)
- **Issue Tracker**: [GitHub Issues](https://github.com/qq136692547-cmyk/QuickNote/issues)

<p align="center">
  <sub>Crafted with passion for developers who value speed, privacy, and flow state. &copy; 2026 QuickNote.</sub>
</p>
