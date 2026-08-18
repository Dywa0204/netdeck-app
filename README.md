# 🛡️ NetDeck Manager Pro Suite

> **Desktop Application for Global Network Tunnels (WireGuard, OpenVPN, SSH), Server Fleet Management, & Automated Task Execution Workflows.**

![Release Version](https://img.shields.io/github/v/release/Dywa0204/wifew-app?style=for-the-badge&color=blue)
![Platform Support](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-brightgreen?style=for-the-badge)
[![Snap Store](https://snapcraft.io/netdeck-manager/badge.svg)](https://snapcraft.io/netdeck-manager)

NetDeck Manager is a cross-platform desktop management application designed for DevOps, system administrators, and developers to seamlessly handle WireGuard, OpenVPN & SSH VPN connections, SSH server infrastructure, SFTP file transfers, web application shortcuts, and automated multi-step deployment workflows.

---

## 💾 Download & Installation Options

Direct download links for pre-built binaries (Windows & Linux Portable + Installers):

| Platform | Download Artifact Name | Type / Format | Notes |
| :--- | :--- | :--- | :--- |
| **🪟 Windows** | `netdeck-1.0.1-windows-x64-portable.exe` | Executable Portable | Standalone Portable (No installation required) |
| **🪟 Windows** | `netdeck-1.0.1-windows-x64-portable.zip` | Zip Archive Portable | Zipped Standalone Portable |
| **🪟 Windows** | `netdeck-1.0.1-windows-x64-setup.exe` | Setup Installer | Full NSIS Windows Setup Wizard |
| **🪟 Windows** | `netdeck-1.0.1-windows-x64-setup.zip` | Zip Archive Installer | Zipped NSIS Windows Setup Wizard |
| **🐧 Linux** | `netdeck-manager` (Snap Store) | Snap Package | Official Snap Store Release |
| **🐧 Linux** | `netdeck-1.0.1-linux-x64-setup.deb` | Debian Package | Linux `.deb` Package (Ubuntu / Debian / Mint) |
| **🐧 Linux** | `netdeck-1.0.1-linux-x64-setup.zip` | Zip Package | Zipped `.deb` Package |
| **🐧 Linux** | `netdeck-1.0.1-linux-x64-portable.tar.gz` | Tarball Portable | Tarball Portable Archive |
| **🐧 Linux** | `netdeck-1.0.1-linux-x64-portable.zip` | Zip Archive Portable | Zipped Portable Executable |

🔗 [View All Release Files on GitHub Releases](https://github.com/Dywa0204/wifew-app/releases/latest)

---

## 🚀 How to Run & Install

### 🪟 Windows

1. Download **`netdeck-1.0.1-windows-x64-portable.exe`** (or `netdeck-1.0.1-windows-x64-setup.exe`).
2. Run the executable file directly or complete the Setup Wizard.
3. _Note for WireGuard Control:_ Ensure the official WireGuard for Windows client is installed if you wish to allow NetDeck Manager to control system WireGuard services.

---

### 🐧 Linux (Snap Store / Debian / Ubuntu / Mint)

#### **Option 1: Install via Snap Store (Recommended)**
Install directly from the official Snapcraft Store via terminal:
```bash
sudo snap install netdeck-manager
```
Or search for **NetDeck Manager** (`netdeck-manager`) in Ubuntu Software Center / Snap Store GUI.

*Grant Network & VPN Permissions (run once after installation):*
```bash
sudo snap connect netdeck-manager:network-control
sudo snap connect netdeck-manager:network-observe
sudo snap connect netdeck-manager:system-observe
```

#### **Option 2: Install via `.deb` Package**
1. Download **`netdeck-1.0.1-linux-x64-setup.deb`**.
2. Install via terminal:
   ```bash
   sudo dpkg -i netdeck-1.0.1-linux-x64-setup.deb
   sudo apt-get install -f # Fix dependencies if needed
   ```

#### **Option 3: Run Standalone Portable**
Extract `netdeck-1.0.1-linux-x64-portable.zip` or `.tar.gz` and execute `./netdeck-manager`.

_Note for WireGuard Control:_ Ensure `wg-quick` or `wg` CLI is installed (`sudo apt install wireguard`).

---

## ✨ Key Features

- **🛡️ WireGuard Tunnels Manager**: Automatic sync with system WireGuard configs, handshake & bandwidth Rx/Tx monitoring, 1-click connection toggles.
- **🖥️ Server Inventory & Fleet**: Multi-endpoint server profiles, SSH public key auto-deploy, live server CPU/RAM/Disk metrics.
- **📁 SFTP Remote File Transfer**: Full dual-pane file explorer, directory upload/download with live progress bars.
- **🌐 Web Applications Master Data**: Manage internal & external web app URLs with automated WireGuard VPN activation upon launch.
- **⚡ Task Executor & Workflows**: Build multi-step deployment & server task execution pipelines with live log streaming.

---

## 🔒 Security & Privacy

- All server keys, passwords, and tunnel configurations are stored **locally on your machine in encrypted SQLite database storage**.
- No private telemetry, analytics, or remote data is ever transmitted to external servers.

---

## 📜 License & Support

For issues, bug reports, or feature requests, please submit an issue on the [Public Issue Tracker](https://github.com/Dywa0204/wifew-app/issues).

