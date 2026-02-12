# IP-Hunter
IPHunter adalah defensive security assessment tool untuk membantu pemilik website dan developer mengidentifikasi potensi risiko keamanan dan kesalahan konfigurasi web tanpa menampilkan detail eksploitasi.
---

# IP HUNTER 
Professional IP Discovery Tool with Premium UI & Dual Language Support

![Python](https://img.shields.io/badge/Python-3.++-blue)
![License](https://img.shields.io/badge/License-MIT-lightgrey)
![Support](https://img.shields.io/badge/Support-Saweria-orange)
![Support](https://img.shields.io/badge/Support-Trakteer-red)
![Cybersecurity](https://img.shields.io/badge/Topic-Cybersecurity-blueviolet)
---

## 📋 Table of Contents
● Overview

● Features

● Installation

● Usage

● Screenshots

● How It Works

● Language Support

● Output Formats

● Cloudflare Detection

● Contributing

● License

● Contact


## 🎯 Overview
IP HUNTER is a professional-grade tool designed for discovering origin IP addresses behind domains. With its premium UI, dual language support (English & Indonesian), and intelligent analysis system, it helps security researchers and network administrators identify potential origin servers.
``⚠️ Educational Purpose Only - This tool is designed for legitimate security research and authorized testing only.
``
## ✨ Features
## 🚀 Core Capabilities

● DNS Resolution - Resolve domains to all associated IP addresses

● CDN Detection - Automatically detect Cloudflare and major cloud providers

● Origin IP Analysis - Score and rank potential origin IP candidates

● Port Scanning - Quick scan of common ports on discovered IPs

● HTTP Analysis - Extract server information and headers

# 🌐 Dual Language
```
English - Full English interface

Bahasa Indonesia - Complete Indonesian translation
```

# 📊 Export Options
```
JSON Export - Structured data format

CSV Export - Spreadsheet-compatible format

Screen Output - Real-time display
```
# 💻 Installation
Prerequisites
Python 3.++

## Quick Install
```
# Clone the repository
git clone https://github.com/ruyynn/iphunter.git

# Navigate to directory
cd iphunter

# Make executable (Linux/Mac)
chmod +x iphunterV2.py
```
# 🎮 Usage
Basic Usage
```bash
# Run the tool
python3 iphunterV2.py
```

# Menu Options
Option	English	& Bahasa Indonesia	Description

[1]	Scan Single Domain	Scan Domain Tunggal	Scan one domain

[2]	Scan Multiple Domains	Scan Banyak Domain	Bulk scan (coming soon)

[3]	View Scan History	Lihat Riwayat Scan	History viewer (coming soon)

[4]	Settings	Pengaturan	Configuration (coming soon)

[5]	Help & Tutorial	Bantuan & Tutorial	User guide

[0]	Exit	Keluar	Exit program

# 📸 Screenshots

# 🔧 How It Works
1. DNS Resolution
Performs A/AAAA record lookup

Collects all associated IP addresses

Filters unique addresses

2. Provider Detection
Checks against Cloudflare IP ranges

Identifies major cloud providers (Google, AWS, Azure)

Flags CDN-protected IPs

3. HTTP Analysis
Connects to port 80

Analyzes server headers

Detects Cloudflare-specific headers (CF-Ray, CF-Cache-Status)

4. Port Scanning
Quick scan of common ports (21,22,23,25,53,80,110,143,443,445)

Identifies open services

Non-intrusive, single packet per port

5. Origin Analysis
Scoring System:

-40 points: Major cloud provider (not origin)

+5 points per open port

+10 points for web ports (80,443)

+5 points for non-CDN reverse DNS

6. Confidence Levels
 
Score	Confidence	Color

60+	HIGH	🟢 Green

30-59	MEDIUM	🟡 Yellow

0-29	LOW	⚪ White

## 🌍 Language Support

English Interface
```text
🌐 Select Language:
  [1] English
  [2] Bahasa Indonesia
Indonesian Interface
```
```text
🌐 Pilih Bahasa:
  [1] English
  [2] Bahasa Indonesia
```
## Both languages feature complete translations of:

All menu items and options

Error messages and notifications

Help documentation

Scan results and analysis

Recommendations

## 📁 Output Formats
JSON Output
```json
{
  "domain": "example.com",
  "timestamp": "2024-01-01T12:00:00",
  "ips": ["192.168.1.1"],
  "cloudflare_detected": false,
  "big_provider_detected": false,
  "candidates": [
    {
      "ip": "192.168.1.1",
      "score": 65,
      "open_ports": [80, 443],
      "reasons": ["2 open ports", "Standard web ports"],
      "is_big_provider": false
    }
  ],
  "confidence": "HIGH"
}

```

CSV Output
```
Domain	     IP	       Score	Open Ports	Cloudflare
example.com	192.168.1.1	65	80,443	        No
🛡️ Cloudflare Detection
When Cloudflare is detected, IP HUNTER provides:

🔴 Warning Display
Clear indication of Cloudflare protection
```
List of detected Cloudflare IPs

Educational information about why origin IP cannot be directly found

📚 Alternative Methods
Historical DNS Records - Check before Cloudflare implementation

SSL Certificate Analysis - Examine Subject Alternative Names

Subdomain Enumeration - Find unprotected subdomains

MX/SPF Records - Email infrastructure may reveal origin

Cloudflare Leaks - Search for misconfigurations

⚠️ Important Note
No tool can directly find origin IP behind properly configured Cloudflare protection.
IP HUNTER provides candidates and recommendations, but manual investigation is required.

🗺️ Roadmap
✅ Version 1.1 (Current)
Dual language support (EN/ID)

Premium UI with animations

Origin IP scoring system

Basic port scanning

Cloudflare detection

JSON/CSV export

🚧 Version 1.2 (Planned)
Bulk domain scanning

Threading for faster scans

SSL certificate analysis

Reverse DNS lookup

WHOIS integration

🔮 Version 2.0 (Future)
Historical DNS records

Subdomain enumeration

Favicon hash analysis

SSL SAN extraction

Autonomous System (AS) lookup

Geographical IP mapping

🤝 Contributing
Contributions are welcome! Here's how you can help:

Fork the repository

Create a feature branch (git checkout -b feature/amazing-feature)

Commit your changes (git commit -m 'Add amazing feature')

Push to the branch (git push origin feature/amazing-feature)

Open a Pull Request

Contribution Guidelines
Maintain PEP 8 style guide

Add comments for complex logic

Update documentation

Test thoroughly

📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

text
MIT License

Copyright (c) 2024 ruyynn

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files...
📞 Contact
Developer
ruyynn / ellreynn

Instagram: @ellreynn

GitHub: @ruyynn

Support
⭐ Star this repository if you find it useful!

🐛 Report issues via GitHub Issues

💬 Contact developer for questions or collaboration

🙏 Acknowledgments
Python community for excellent documentation

Security researchers for sharing knowledge

All users who provided feedback and suggestions

⚖️ Disclaimer
This tool is for educational and authorized testing purposes only.

Only scan domains you own or have permission to test

Respect websites' terms of service and robots.txt

The developer is not responsible for misuse of this tool

Always verify findings through multiple sources

Use responsibly and ethically

<div align="center">
Made with ❤️ by ruyynn

⬆ Back to Top

</div>
