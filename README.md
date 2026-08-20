# 🛡️ NetDeck Manager Pro Suite

> **Universal Multi-Protocol VPN Tunnel Engine (WireGuard, OpenVPN, SSH, Custom), Server Fleet Management, SFTP File Explorer, Embedded Terminal & Automated Task Execution Workflows.**

![Release Version](https://img.shields.io/github/v/release/Dywa0204/wifew-app?style=for-the-badge&color=blue)
![Platform Support](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-brightgreen?style=for-the-badge)
[![Snap Store](https://snapcraft.io/netdeck/badge.svg)](https://snapcraft.io/netdeck)

NetDeck Manager is a modern, high-performance cross-platform desktop application designed for DevOps engineers, system administrators, and developers. It serves as a unified command center to manage **Universal VPN Tunnels** (WireGuard, OpenVPN, SSH Tunneling, and Custom network interfaces), SSH server infrastructure, dual-pane SFTP file transfers, web application catalogs, and automated multi-step deployment pipelines.

---

## 💾 Download & Installation Options (v1.0.4)

Direct download links for pre-built binaries (Windows & Linux Portable + Installers):

| Platform | Download Artifact Name | Type / Format | Notes |
| :--- | :--- | :--- | :--- |
| **🪟 Windows** | `netdeck-1.0.4-windows-x64-portable.exe` | Executable Portable | Standalone Portable (No installation required) |
| **🪟 Windows** | `netdeck-1.0.4-windows-x64-portable.zip` | Zip Archive Portable | Zipped Standalone Portable |
| **🪟 Windows** | `netdeck-1.0.4-windows-x64-setup.exe` | Setup Installer | Full NSIS Windows Setup Wizard |
| **🪟 Windows** | `netdeck-1.0.4-windows-x64-setup.zip` | Zip Archive Installer | Zipped NSIS Windows Setup Wizard |
| **🐧 Linux** | `netdeck-1.0.4-linux-x64-setup.deb` | Debian Package | Linux `.deb` Package (Ubuntu / Debian / Mint) |
| **🐧 Linux** | `netdeck-1.0.4-linux-x64-setup.zip` | Zip Package | Zipped `.deb` Package |
| **🐧 Linux** | `netdeck-1.0.4-linux-x64-portable.tar.gz` | Tarball Portable | Tarball Portable Archive |
| **🐧 Linux** | `netdeck-1.0.4-linux-x64-portable.zip` | Zip Archive Portable | Zipped Portable Executable |

🔗 [View All Release Files on GitHub Releases](https://github.com/Dywa0204/wifew-app/releases/latest)

---

## 🚀 How to Run & Install

### 🪟 Windows

1. Download **`netdeck-1.0.4-windows-x64-setup.exe`** (or `netdeck-1.0.4-windows-x64-portable.exe` if not prefer for installing app).
2. Run the executable file directly or complete the Setup Wizard.
3. *Note for WireGuard Control:* Ensure the official WireGuard for Windows client is installed if you wish to allow NetDeck Manager to control system WireGuard services.

---

### 🐧 Linux (Snap Store / Debian / Ubuntu / Mint / Fedora / Arch)

#### **Option 1: Install via `.deb` Package**
1. Download **`netdeck-1.0.4-linux-x64-setup.deb`**.
2. Install via terminal:
   ```bash
   sudo dpkg -i netdeck-1.0.4-linux-x64-setup.deb
   ```
   ```bash
   sudo apt-get install -f # Fix dependencies if needed
   ```

#### **Option 2: Run Standalone Portable**
Extract `netdeck-1.0.4-linux-x64-portable.zip` or `.tar.gz` and execute `./netdeck-manager`.

*Note for Linux VPN Control:*
- WireGuard: Ensure `wireguard-tools` / `wg-quick` is installed (`sudo apt install wireguard`).
- OpenVPN: Ensure `openvpn` is installed (`sudo apt install openvpn`).

---

## ✨ Key Features

### 🛡️ Universal Multi-Protocol VPN Engine
- **Multi-Protocol Support**: Seamlessly manage **WireGuard**, **OpenVPN**, **SSH SOCKS5/Local Tunneling**, and **Custom VPN commands** (`nmcli`, `tailscale`, `zerotier`, etc.).
- **Automatic Configuration Sync**: Auto-detects and imports system configurations with DPAPI decryption on Windows and `/etc/wireguard` parsing on Linux.
- **System Tray Fast Switcher (`Tunnels >`)**: Instant 1-click VPN switching directly from the desktop taskbar / notification tray.
- **Traffic & Bandwidth Analytics**: Real-time handshake monitoring, connected IP display, and Tx/Rx data transfer graphs.
- **App & Workflow Auto-Connect**: Automatically triggers the required VPN tunnel before launching a web application or executing remote server workflows.

### 🖥️ Server Inventory & Infrastructure Fleet
- **Multi-Endpoint Server Profiles**: Store SSH connections with support for passwords, custom SSH private keys (ED25519, RSA), and port configuration.
- **1-Click SSH Public Key Deploy**: Automatically deploys your local `id_ed25519.pub` or custom public key to remote `~/.ssh/authorized_keys`.
- **Live System Metrics**: Real-time CPU usage, RAM utilization, Disk consumption, and OS kernel telemetry over non-intrusive SSH probes.

### 📁 Dual-Pane SFTP Remote File Manager
- **Dual-Pane Interface**: Side-by-side local workstation explorer and remote server SFTP file tree.
- **Drag-and-Drop File Transfers**: Multi-file and directory upload/download with live progress bars, pause/cancel, and speed statistics.
- **Integrated Remote Editor**: Create, view, edit, rename, and delete remote files directly without leaving the application.

### 💻 Embedded Multi-Tab Terminal Canvas
- **Interactive PTY Shells**: Native xterm-powered interactive SSH terminals and local PowerShell / Bash terminals.
- **Real-Time ICMP Ping Monitor**: Embedded continuous ping graphs with latency tracking and packet loss detection.
- **Pop-Out Window Support**: Detach terminal tabs into separate independent multi-monitor desktop windows.

### 🌐 Web Applications Master Data
- **Centralized Service Catalog**: Manage development, staging, and production web application links in one place.
- **Source Code Path Linking**: Bind application bookmarks directly to local source code project directories.
- **Smart VPN Binding**: Automatically connects the corresponding VPN tunnel whenever you open internal services.

### ⚡ Task Executor & Multi-Step Workflows
- **Multi-Step Automation Engine**: Build sequential deployment pipelines combining SSH commands, shell scripts, local tasks, file transfers, delay intervals, and HTTP health checks.
- **Dynamic Variable Injection**: Inject environment variables (`{{HOST}}`, `{{PORT}}`, `{{APP_ENV}}`) at runtime or via CLI flags (`-e KEY=VALUE`).
- **Live Execution Streaming**: Real-time ANSI colored terminal output logs with step-by-step progress tracking.

### 📦 Comprehensive JSON Backup & Restore
- **1-Click Export & Import**: Export all servers, tunnels, applications, workflows, snippets, and application settings into a standard `.json` backup file.
- **Machine Migration**: Instantly restore your entire workspace setup across different Windows and Linux computers.

### 🚀 Powerful Headless CLI (`netdeck`)
Run and manage NetDeck completely from your terminal or CI/CD scripts:
```bash
# Manage VPN Tunnels
netdeck vpn list
netdeck vpn up <tunnel-name>
netdeck vpn down <tunnel-name>

# Execute Automation Workflows
netdeck workflow list
netdeck run <workflow-name> -e ENV=production

# Server Fleet & Applications
netdeck server list
netdeck app list
```

---

## 🔒 Security & Privacy

- All server credentials, SSH keys, passwords, and tunnel configurations are stored **locally on your machine in encrypted SQLite / JSON storage**.
- **Zero Telemetry**: No private keys, server IPs, connection logs, or analytics are ever transmitted to external cloud servers.

---

## 📜 License & Support

For issues, bug reports, or feature requests, please submit an issue on the [Public Issue Tracker](https://github.com/Dywa0204/wifew-app/issues).
