# Security & Privacy Policy

QuickNote was architected from day one under a strict **Zero-Telemetry, Offline-First** security philosophy. We believe developer tools should respect your local machine and your source code.

---

## 🔒 Security Commitments

1. **Zero Phone-Home Analytics**  
   QuickNote does not bundle telemetry SDKs, crash uploaders, or tracking pixels. When offline, outbound network sockets remain completely uninitialized.

2. **Local Cryptographic Vault**  
   All notes, tags, and scratchpad data are stored exclusively in your local SQLite database on your SSD. We have zero access to your uncommitted API tokens, database connection strings, or proprietary source code.

3. **API Key Security (BYOK Mode)**  
   When you connect your personal DeepSeek or OpenAI API keys, they are stored locally with memory-safe masking. Outbound calls only connect directly to your specified endpoint.

4. **Official AI Gateway Isolation**  
   If you use our official DeepSeek channel, all requests pass through an enterprise-grade Cloudflare Worker proxy. Your requests are stateless, never written to disk, and protected by Cloudflare's global DDoS mitigation.

---

## 🛡️ Supported Versions

| Version | Supported | Security Updates |
| :--- | :---: | :---: |
| `v0.1.x` | ✅ | Active |
| `< v0.1.0` | ❌ | End of Life |

---

## 🚨 Reporting a Vulnerability

If you discover a security vulnerability within QuickNote:

- **Please do NOT open a public GitHub issue.**
- Send an encrypted or direct email to: **[security@quicknote.dev](mailto:security@quicknote.dev)** (or `support@quicknote.dev`).
- Include detailed steps to reproduce the issue and affected platform specifications.
- We pledge to acknowledge your submission within **24 hours** and provide a patch within **72 hours** for any critical vulnerability.

Thank you for helping keep the developer ecosystem safe!
