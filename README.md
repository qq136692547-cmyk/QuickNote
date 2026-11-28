<p align="center">
  <img src="https://anan.lat/assets/app-logo.png?v=2" alt="QuickNote Logo" width="108" height="108" style="border-radius: 24px; box-shadow: 0 8px 32px rgba(56, 189, 248, 0.25);" />
</p>

<h1 align="center">QuickNote</h1>

<p align="center">
  <b>The Blazing-Fast, 100% Offline-First AI Scratchpad &amp; Encrypted Credential Vault for Developers.</b><br>
  <i>Summon your external brain in <b>&lt;50ms</b> anywhere on Windows with <code>Ctrl+Shift+Q</code>. Zero telemetry. Zero SaaS lock-in.</i>
</p>

<p align="center">
  <a href="https://github.com/qq136692547-cmyk/QuickNote/releases"><img src="https://img.shields.io/badge/Release-v0.2.0-sky.svg?style=flat-square&logo=windows" alt="Release v0.2.0" /></a>
  <a href="https://anan.lat/#terms"><img src="https://img.shields.io/badge/License-Freemium%20%2F%20Commercial-blue.svg?style=flat-square" alt="License" /></a>
  <img src="https://img.shields.io/badge/Built%20with-Rust%20%2B%20Tauri%202.0-orange.svg?style=flat-square&logo=rust" alt="Rust + Tauri 2.0" />
  <img src="https://img.shields.io/badge/Vault-AES--256--GCM%20%2B%20Argon2id-003B57.svg?style=flat-square&logo=sqlite" alt="Encrypted SQLite" />
  <img src="https://img.shields.io/badge/AI%20Gateway-SenseNova%206.8%20%2B%20BYOK-indigo.svg?style=flat-square" alt="SenseNova 6.8 + BYOK" />
  <a href="https://anan.lat"><img src="https://img.shields.io/badge/Website-anan.lat-emerald.svg?style=flat-square&logo=cloudflare" alt="Website" /></a>
  <a href="https://www.producthunt.com/products/quicknote-5"><img src="https://img.shields.io/badge/Product%20Hunt-QuickNote-DA552F.svg?style=flat-square&logo=producthunt" alt="Product Hunt" /></a>
  <a href="https://dengli.gumroad.com/l/quicknote-pro"><img src="https://img.shields.io/badge/Gumroad-Lifetime%20Pro%20%2429-FF90E8.svg?style=flat-square&logo=gumroad" alt="Gumroad" /></a>
</p>

<p align="center">
  <a href="#-quickstart--installation">⚡ Quickstart</a> •
  <a href="#-killer-features">✨ Key Features</a> •
  <a href="#-why-quicknote-vs-others">⚔️ Comparison</a> •
  <a href="#-engineering-blog--deep-dives">📚 Engineering Blog</a> •
  <a href="#-offline-first-privacy-manifesto">🛡️ Privacy</a> •
  <a href="https://anan.lat">🌐 Official Website</a>
</p>

> **Note on Repository Scope**: This public repository hosts QuickNote's official Windows binary releases, SHA256 integrity manifests, security documentation, roadmap, and issue tracker. Core application source code remains proprietary and commercial.

---

## ⚡ Why QuickNote?

How many times a day do you break your coding flow state?
- You need to temporarily stash an API secret, a regex snippet, or a `curl` command;
- You need to draft a prompt for an LLM and find yourself opening a browser tab, fighting with a 500MB Electron app, or searching for Notepad;
- You're worried about cloud-based note apps scanning your uncommitted credentials or internal database schemas.

**QuickNote was engineered from scratch in Rust &amp; Tauri 2.0 to eliminate this friction entirely.**  
Hit `Ctrl+Shift+Q`. A sleek, dark-mode scratchpad appears over your active IDE in **&lt;50ms typical** (~15–25MB RAM, &lt;12MB binary). Take notes, refine your prompt with one click, pin it as a floating cheat sheet, or press `Esc` to disappear. Your notes and credentials stay encrypted on your SSD in a local SQLite vault.

---

## ✨ Killer Features

### ⚡ Sub-50ms Global Summoning (`Ctrl+Shift+Q`)
Slides out immediately over full-screen IDEs (VS Code, Cursor), debuggers, or terminals, and dismisses back to tray without stealing window focus.

### 🔒 100% Offline-First Encrypted SQLite Vault
Zero accounts required. Zero telemetry pings. Sensitive vaults (`card`, `account`, `api`) are encrypted locally with **AES-256-GCM + Argon2id**, memory-scrubbed with Rust `zeroize`, and strictly isolated from the plaintext **FTS5** full-text search index (**1.8ms** median search across 10,000 notes in WAL mode).

### 📌 Always-on-Top Floating Pin Card
Pin critical API endpoints, SQL query templates, or meeting action items directly over your workspace while coding.

### 🤖 Dual-Track AI Engine (No SaaS Hostage)
Never worry about losing your AI workflow if a cloud service hiccups:
- **Official Cloud Gateway**: Built-in **SenseNova 6.8 Flash** with 5-account round-robin load balancing and automatic 429 failover retry via Cloudflare Workers.
- **BYOK (Bring Your Own Key) Freedom**: Enter your own **SenseNova, DeepSeek, OpenAI**, or local **Ollama** endpoint (`http://localhost:11434/v1`) for **unlimited, uncapped lifetime usage**.

### ✨ 1-Click System Prompt Refiner &amp; Vision OCR
Turn raw thoughts into structured System Prompts (**Role**, **Task**, **Constraints**), or drop screenshots of code and tables for clean Markdown/SQL extraction.

### 🛡️ Offline Ed25519 Cryptographic Licensing
Pro editions verify compact `QN-PRO-...` keys locally in **&lt;0.2ms** using `ed25519-dalek` asymmetric signatures. Activates completely offline on up to **3 personal Windows devices** with **zero call-home DRM**.

---

## ⚔️ Why QuickNote vs. Others?

| Feature | QuickNote | Notion / Obsidian | Windows Sticky Notes | Typical Electron Apps |
| :--- | :---: | :---: | :---: | :---: |
| **Hotkey Summon** | **&lt;50ms (`Ctrl+Shift+Q`)** | 2.5s – 6s (3rd-party plugin) | ~800ms (No global hotkey) | 3s – 8s |
| **Memory Footprint** | **~15–25 MB RAM** | 350 MB – 1.2 GB | ~90 MB | 450 MB – 1.5 GB |
| **Local Encryption** | **AES-256-GCM + Argon2id** | Cloud-dependent / plugins | Cloud synced | Varies |
| **Local FTS5 Search** | **1.8ms (10k notes, WAL)** | Varies | Basic | Heavy |
| **AI Engine** | **SenseNova 5-Key + BYOK** | Paid add-on | None | Paid add-on |
| **License Verification** | **Offline Ed25519 (&lt;0.2ms)** | Online SaaS | Account-tied | Online DRM |
| **Pricing Model** | **Free (50 notes) / $29 Lifetime** | $10–$20/mo subscription | Free (Barebones) | Recurring SaaS |

---

## 📚 Engineering Blog &amp; Deep Dives

Read our systems architecture papers on [anan.lat/blog](https://anan.lat/blog/):

1. **[Offline Ed25519 Software Licensing in Rust: Perpetual Ownership Without Call-Home DRM](https://anan.lat/blog/offline-ed25519-cryptographic-licensing-without-drm)** — Sub-0.2ms `ed25519-dalek` verification, canonical payloads, and honest threat modeling.
2. **[Sub-2ms Local Search Across 10,000 Notes: SQLite FTS5, WAL Mode, and Encrypted Vault Isolation](https://anan.lat/blog/sqlite-fts5-sub-2ms-full-text-search-rust-tauri)** — Tuning `unicode61`, `prefix='2 3'`, BM25 ranking, and keeping AES-256-GCM secrets out of inverted indices.
3. **[Why Rust + Tauri Beats Electron for Developer Scratchpads](https://anan.lat/blog/why-rust-tauri-beats-electron-for-scratchpads)** — Memory footprint (15MB vs 500MB RAM) and sub-50ms summon benchmarks on Windows 11.
4. **[Building an Offline-First SQLite Vault with AES-256-GCM and Argon2id](https://anan.lat/blog/building-offline-first-sqlite-vault-aes-256-gcm)** — Authenticated encryption with AAD binding and `zeroize` memory scrubbing.
5. **[Dual-Track AI Architecture: SenseNova 5-Key Gateway Load Balancing vs. Local BYOK](https://anan.lat/blog/dual-track-ai-sensenova-load-balancing-vs-byok)** — Resilient multi-key failover alongside zero-telemetry local Ollama/BYOK routing.

---

## ⚡ Quickstart &amp; Installation (Windows 10 / 11 x64)

Download pre-compiled Windows binaries from [GitHub Releases](https://github.com/qq136692547-cmyk/QuickNote/releases) or our Cloudflare Pages CDN mirror:

- **[Download Portable Edition (.zip)](https://github.com/qq136692547-cmyk/QuickNote/releases/download/v0.2.0/QuickNote_v0.2.0_x64_Portable.zip)** ([CDN Mirror](https://anan.lat/downloads/QuickNote_v0.2.0_x64_Portable.zip)) — Extract and run immediately, zero registry writes.
- **[Download Windows Installer (.exe)](https://github.com/qq136692547-cmyk/QuickNote/releases/download/v0.2.0/QuickNote_v0.2.0_x64_Installer.exe)** ([CDN Mirror](https://anan.lat/downloads/QuickNote_v0.2.0_x64_Installer.exe)) — Standard Windows setup wizard.
- **[SHA256SUMS.txt](https://anan.lat/downloads/SHA256SUMS.txt)** — Verify binary integrity before execution.

---

## 🛡️ Offline-First Privacy Manifesto

1. **Zero Telemetry**: QuickNote contains zero analytics SDKs, crash-upload beacons, or background tracking pings.
2. **Local-Only Encrypted Storage**: Sensitive credentials and BYOK API keys stay encrypted in your local SQLite vault (`quicknote.db`).
3. **Auditable Network Silence**: In offline mode, QuickNote opens zero outbound sockets—independently verifiable via Wireshark or Windows Resource Monitor.

---

## 💎 Pricing &amp; Lifetime Pro

- **Free Edition ($0)**: Up to 50 local notes, FTS5 instant search, `Ctrl+Shift+Q` global hotkey, floating pin window.
- **Lifetime Pro ($29 one-time)**: Unlimited notes &amp; encrypted vaults, SenseNova 6.8 Flash 5-Key gateway, unlimited BYOK (SenseNova / DeepSeek / OpenAI / Ollama), Prompt Refiner &amp; Vision OCR, and offline Ed25519 activation on up to **3 personal devices**.

👉 **[Get Lifetime Pro ($29) on Gumroad](https://dengli.gumroad.com/l/quicknote-pro)** — Use promo code **`PHHUNTER`** for **50% OFF** *(valid through Nov 30, 2026; 7-day 100% money-back guarantee)*.

---

## 💬 Links &amp; Support

- **Official Website**: [https://anan.lat](https://anan.lat)
- **Engineering Blog**: [https://anan.lat/blog/](https://anan.lat/blog/)
- **Product Hunt**: [https://www.producthunt.com/products/quicknote-5](https://www.producthunt.com/products/quicknote-5)
- **Maker Open-Source Hub**: [https://qq136692547-cmyk.github.io/](https://qq136692547-cmyk.github.io/)
- **Support Email**: [support@anan.lat](mailto:support@anan.lat)
- **Issue Tracker**: [GitHub Issues](https://github.com/qq136692547-cmyk/QuickNote/issues)

<p align="center">
  <sub>Crafted with Rust &amp; Tauri for developers who value speed, privacy, and flow state. &copy; 2026 QuickNote Studio.</sub>
</p>
