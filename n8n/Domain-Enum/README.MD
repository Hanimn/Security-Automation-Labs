# n8n Security Automation Workflows

This directory contains n8n workflows for security automation, specifically focused on domain enumeration and reconnaissance tasks.

## 🎯 Overview

These workflows automate various security reconnaissance tasks including:
- Subdomain discovery using multiple sources
- Port scanning and service detection
- Technology stack identification
- Certificate transparency log analysis
- Automated reporting and alerting

## 📁 Directory Structure

```
n8n/
├── workflows/          # n8n workflow JSON files
├── docs/              # Documentation and guides
├── scripts/           # Helper scripts and utilities
├── templates/         # Templates for notifications and reports
└── examples/          # Sample outputs and test data
```

## 🚀 Quick Start

1. **Prerequisites:**
   - n8n installed and running
   - API keys for external services (SecurityTrails, Shodan, etc.)
   - Access to target domains (own domains only)

2. **Import Workflows:**
   - Copy workflow JSON files from `workflows/` directory
   - Import into your n8n instance
   - Configure credentials and API keys

3. **Run Basic Domain Enumeration:**
   - Open `domain-enumeration-basic.json` workflow
   - Enter your target domain
   - Execute workflow

## 🔐 Security & Legal Notice

⚠️ **IMPORTANT**: These tools are for authorized security testing only. Only use on domains you own or have explicit written permission to test. Unauthorized scanning may violate terms of service and local laws.

## 📚 Documentation

- [Setup Guide](docs/setup-guide.md) - Complete installation and configuration
- [API Configuration](docs/api-configuration.md) - Setting up external API integrations
- [Troubleshooting](docs/troubleshooting.md) - Common issues and solutions

## 🛠 Workflows Included

### Basic Domain Enumeration
- Certificate transparency lookup
- Basic subdomain discovery
- Live host validation
- Simple reporting

### Advanced Domain Enumeration
- Multiple subdomain discovery sources
- Port scanning integration
- Technology detection
- Comprehensive reporting
- Slack/Discord notifications

### Continuous Monitoring
- Scheduled domain monitoring
- Change detection
- Alert generation
- Historical tracking

## 🔗 External Dependencies

- [SecurityTrails API](https://securitytrails.com/corp/api)
- [Shodan API](https://developer.shodan.io/)
- [VirusTotal API](https://developers.virustotal.com/)
- [Certificate Transparency Logs](https://crt.sh/)

## 📊 Sample Output

See `examples/sample-output.json` for example enumeration results.

## 🤝 Contributing

Feel free to submit improvements, additional workflows, or bug fixes via pull requests.

## 📄 License

This project is part of the Security-Automation-Labs repository. Use responsibly and in accordance with applicable laws and regulations.