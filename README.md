# 🛡️ NetDeck Manager Pro Suite

> **Universal Multi-Protocol VPN Tunnel Engine (WireGuard, OpenVPN, SSH, Custom), Remote Node Engine, Server Fleet Management, SFTP File Explorer, Embedded Terminal & Automated Task Execution Workflows.**

![Release Version](https://img.shields.io/github/v/release/Dywa0204/netdeck-app?style=for-the-badge&color=blue)
![Platform Support](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-brightgreen?style=for-the-badge)

NetDeck Manager is a modern, high-performance cross-platform desktop application designed for DevOps engineers, system administrators, and developers. It serves as a unified command center to manage **Universal VPN Tunnels** (WireGuard, OpenVPN, SSH Tunneling, and Custom network interfaces), remote host nodes, SSH server infrastructure, dual-pane SFTP file transfers, web application catalogs, and automated multi-step deployment pipelines.

---

## 💾 Download & Installation Options (v1.0.6)

Direct download links for pre-built binaries (Windows & Linux Portable + Installers):

| Platform       | Download Artifact Name                    | Type / Format         | Notes                                          |
| :------------- | :---------------------------------------- | :-------------------- | :--------------------------------------------- |
| **🪟 Windows** | `netdeck-1.0.6-windows-x64-portable.exe`  | Executable Portable   | Standalone Portable (No installation required) |
| **🪟 Windows** | `netdeck-1.0.6-windows-x64-portable.zip`  | Zip Archive Portable  | Zipped Standalone Portable                     |
| **🪟 Windows** | `netdeck-1.0.6-windows-x64-setup.exe`     | Setup Installer       | Full NSIS Windows Setup Wizard                 |
| **🪟 Windows** | `netdeck-1.0.6-windows-x64-setup.zip`     | Zip Archive Installer | Zipped NSIS Windows Setup Wizard               |
| **🐧 Linux**   | `netdeck-1.0.6-linux-x64-setup.deb`       | Debian Package        | Linux `.deb` Package (Ubuntu / Debian / Mint)  |
| **🐧 Linux**   | `netdeck-1.0.6-linux-x64-setup.zip`       | Zip Package           | Zipped `.deb` Package                          |
| **🐧 Linux**   | `netdeck-1.0.6-linux-x64-portable.tar.gz` | Tarball Portable      | Tarball Portable Archive                       |
| **🐧 Linux**   | `netdeck-1.0.6-linux-x64-portable.zip`    | Zip Archive Portable  | Zipped Portable Executable                     |

🔗 [View All Release Files on GitHub Releases](https://github.com/Dywa0204/netdeck-app/releases/latest)

---

## 🚀 How to Run & Install

### 🪟 Windows

1. Download **`netdeck-1.0.6-windows-x64-setup.exe`** (or `netdeck-1.0.6-windows-x64-portable.exe` if you prefer a standalone executable).
2. Run the executable file directly or complete the Setup Wizard (supports Full, GUI-Only, or CLI-Only setup modes).
3. _Note for WireGuard Control:_ Ensure the official WireGuard for Windows client is installed if you wish to allow NetDeck Manager to control system WireGuard services.

---

### 🐧 Linux (Debian / Ubuntu / Mint / Fedora / Arch)

#### **Option 1: Install via `.deb` Package (Recommended)**

1. Download **`netdeck-1.0.6-linux-x64-setup.deb`**.
2. Install via terminal using `apt` (automatically downloads and resolves all required dependencies and desktop shortcuts):
   ```bash
   sudo apt install ./netdeck-1.0.6-linux-x64-setup.deb
   ```
   *(Or if using `dpkg`: `sudo dpkg -i netdeck-1.0.6-linux-x64-setup.deb && sudo apt-get install -f`)*

#### **Option 2: Run Standalone Portable**

Extract `netdeck-1.0.6-linux-x64-portable.zip` or `.tar.gz` and execute `./netdeck-manager`.

_Note for Linux VPN Control:_

- WireGuard: Ensure `wireguard-tools` / `wg-quick` is installed (`sudo apt install wireguard`).
- OpenVPN: Ensure `openvpn` is installed (`sudo apt install openvpn`).

---

## ✨ Key Features

### 🌐 Remote NetDeck Engine (Node Pairing)

- **Decentralized Remote Host Daemon**: Securely pair external machines, virtual instances, and headless servers with NetDeck using 6-digit pairing codes or direct IP/token bindings.
- **Cross-Node Control & Telemetry**: Monitor live CPU/RAM metrics, trigger remote deployment workflows, and sync VPN configurations across machines from a single centralized dashboard.

### 🛡️ Universal Multi-Protocol VPN Engine

- **Multi-Protocol Support**: Seamlessly manage **WireGuard**, **OpenVPN**, **SSH SOCKS5/Local Tunneling**, and **Custom VPN commands** (`nmcli`, `tailscale`, `zerotier`, etc.).
- **Automatic Configuration Sync**: Auto-detects and imports system configurations with DPAPI decryption on Windows and `/etc/wireguard` parsing on Linux.
- **System Tray Fast Switcher (`Tunnels >`)**: Instant 1-click VPN switching directly from the desktop taskbar / notification tray or top navigation bar.
- **Traffic & Bandwidth Analytics**: Real-time handshake monitoring, connected IP display, and Tx/Rx data transfer graphs.
- **App & Workflow Auto-Connect**: Automatically triggers the required VPN tunnel before launching a web application or executing remote server workflows.

### 🖥️ Server Inventory & Infrastructure Fleet

- **Multi-Endpoint Server Profiles**: Store SSH connections with support for passwords, custom SSH private keys (ED25519, RSA), and port configuration.
- **Application-Server Relational Linking**: Directly view, manage, and launch web applications associated with each host server.
- **1-Click SSH Public Key Deploy**: Automatically deploys your local `id_ed25519.pub` or custom public key to remote `~/.ssh/authorized_keys`.
- **Live System Metrics**: Real-time CPU usage, RAM utilization, Disk consumption, and OS kernel telemetry over non-intrusive SSH probes.
- **Granular JSON Export & Import**: Backup and restore server configurations with schema validation.

### 📁 Dual-Pane SFTP Remote File Manager

- **Dual-Pane Interface**: Side-by-side local workstation explorer and remote server SFTP file tree.
- **Sequential Transfer Queue & Worker**: Background upload/download queue with live transfer progress bars, cancellation controls, and speed statistics.
- **Integrated Remote Editor**: Create, view, edit, rename, and delete remote files directly with full sudo-save support.

### 💻 Embedded Multi-Tab Terminal Canvas

- **Interactive PTY Shells**: Native xterm-powered interactive SSH terminals and local PowerShell / Bash terminals with dynamic viewport geometry sync.
- **Real-Time ICMP Ping Monitor**: Embedded continuous ping graphs with latency tracking and packet loss detection.
- **Pop-Out Window Support**: Detach terminal tabs into separate independent multi-monitor desktop windows.

### 🌐 Web Applications Master Data

- **Centralized Service Catalog**: Manage development, staging, and production web application links in one place.
- **Multi-Tag & Server Filtering**: Filter applications by custom tags or host servers.
- **Source Code Path Linking**: Bind application bookmarks directly to local source code project directories.
- **Smart VPN Binding**: Automatically connects the corresponding VPN tunnel whenever you open internal services.

### ⚡ Task Executor & Multi-Step Workflows

- **Multi-Step Automation Engine**: Build sequential deployment pipelines combining SSH commands, shell scripts, local tasks, file transfers, delay intervals, and HTTP health checks.
- **Step-by-Step Audit Logs**: Full execution history modal with live streaming logs, exit codes, and duration tracking.
- **Dynamic Variable Injection**: Inject environment variables (`{{HOST}}`, `{{PORT}}`, `{{APP_ENV}}`) at runtime or via CLI flags (`-e KEY=VALUE`).

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

# Server Fleet & Applications (Index selection supported)
netdeck server list
netdeck server edit 1
netdeck app list

# Shell Auto-Completion
netdeck completion powershell
```

### 🔔 System Tray Integration & Background Daemon

- **Seamless Background Operation**: Keep VPN tunnels, SSH sessions, and background automations active without cluttering the desktop or taskbar.
- **Dynamic Visual Status**: The system tray icon automatically updates with visual badges to show active VPN connections and running background workflows.
- **Quick-Access Context Menu**: Right-click the tray icon to view active tunnel names, disconnect VPNs on the fly, restore/focus the dashboard, or quit the application.
- **Single-Click Window Toggle**: Left-click or double-click to instantly show or hide the NetDeck application window.

---

## 🔒 Security & Privacy

- All server credentials, SSH keys, passwords, and tunnel configurations are stored **locally on your machine in encrypted SQLite / JSON storage**.
- **Zero Telemetry**: No private keys, server IPs, connection logs, or analytics are ever transmitted to external cloud servers.

---

## 📜 License & Support

For issues, bug reports, or feature requests, please submit an issue on the [Public Issue Tracker](https://github.com/Dywa0204/netdeck-app/issues).
