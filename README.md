# WSL Xray Client

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/fixplizz/wsl-xray-client?style=flat-square)](https://github.com/fixplizz/wsl-xray-client)
[![Status](https://img.shields.io/badge/Status-Active%20Development-green.svg)](https://github.com/fixplizz/wsl-xray-client)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04%20%7C%2024.04-orange.svg)](https://www.ubuntu.com/)
[![WSL2](https://img.shields.io/badge/WSL-v2-blue.svg)](https://docs.microsoft.com/en-us/windows/wsl/)

> **Flexible VPN Client Manager for WSL** — Deploy Xray VPN client with VLESS, VMESS, Trojan protocol support inside Windows Subsystem for Linux

---

## 🎯 Overview

**WSL Xray Client** is a professional-grade installation and configuration framework for deploying Xray VPN client inside Windows 11 WSL2 (Ubuntu 22.04/24.04). The project provides:

- ✅ **Multi-Protocol Support**: VLESS, VMESS, Trojan protocols with flexible configuration
- ✅ **Environment-Based Configuration**: All sensitive data externalized to `.env` files
- ✅ **Systemd Integration**: Automatic service management and auto-startup
- ✅ **3X-UI Panel Compatible**: Direct integration with 3X-UI management panel
- ✅ **Flexible Proxy Options**: SOCKS5, HTTP, and Freedom outbound protocols
- ✅ **Production-Ready**: Comprehensive logging, error handling, and documentation

## 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/fixplizz/wsl-xray-client.git
cd wsl-xray-client

# Configure
cp .env.example .env
nano .env  # Edit with your 3X-UI credentials

# Install
sudo chmod +x install.sh
sudo ./install.sh

# Start
sudo systemctl start xray
sudo systemctl enable xray
```

## 📋 Configuration

All configuration is managed through `.env` file:

```env
XRAY_PROTOCOL=vless
XRAY_SERVER_ADDRESS=vpn.example.com
XRAY_SERVER_PORT=443
XRAY_SERVER_UUID=a1b2c3d4-e5f6-7890-abcd-ef1234567890
XRAY_SECURITY=tls
XRAY_OUTBOUND_PROTOCOL=socks5
XRAY_OUTBOUND_PORT=1080
```

## 🔌 Supported Protocols

- **VLESS** ⭐ (Recommended) - Modern, lightweight, XTLS support
- **VMESS** - Feature-rich, stable, asymmetric encryption
- **Trojan** - Secure, SSL/TLS based, hard to detect

## 📚 Documentation

- [Installation Guide](docs/INSTALLATION.md) - Detailed setup instructions
- [Configuration Reference](docs/CONFIGURATION.md) - All configuration options
- [Protocol Details](docs/PROTOCOLS.md) - In-depth protocol information
- [Troubleshooting](docs/TROUBLESHOOTING.md) - Common issues and solutions
- [Contributing Guide](CONTRIBUTING.md) - How to contribute

## 📊 System Requirements

| Requirement | Minimum | Recommended |
|-------------|---------|-------------|
| OS | Windows 11 | Windows 11 Pro/Enterprise |
| WSL | WSL2 | WSL2 (latest) |
| Ubuntu | 22.04 LTS | 24.04 LTS |
| RAM | 2GB | 4GB+ |
| Disk | 500MB | 1GB+ |

## 🔐 Security

- ✅ Never commit `.env` file
- ✅ Use strong UUIDs from 3X-UI panel
- ✅ Keep Xray updated
- ✅ Enable TLS/XTLS security
- ✅ Use local proxy (127.0.0.1)

## 🛠️ Commands Reference

```bash
# Status
sudo systemctl status xray

# Logs (real-time)
sudo journalctl -u xray -f

# Restart
sudo systemctl restart xray

# Stop
sudo systemctl stop xray

# Test proxy
curl -x socks5://127.0.0.1:1080 https://ifconfig.me
```

## 📝 License

MIT License - see [LICENSE](LICENSE) file

## 🤝 Contributing

Contributions welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📞 Support

- [GitHub Issues](https://github.com/fixplizz/wsl-xray-client/issues)
- [GitHub Discussions](https://github.com/fixplizz/wsl-xray-client/discussions)
- [Documentation](docs/)

---

**Made with ❤️ for DevOps & Open Source Community**

[![GitHub followers](https://img.shields.io/github/followers/fixplizz?label=Follow&style=social)](https://github.com/fixplizz)