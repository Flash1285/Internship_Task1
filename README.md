# Internship_Task1
Learn to discover open ports on devices in your local network to understand network exposure.

# 🌐 Network Discovery and Security Analysis Workshop

A step-by-step guide for performing a basic network scan, analyzing the results, and researching potential security vulnerabilities using **Nmap** and **Wireshark**.

---

## 🚀 Phase 1: Installation

This phase covers the required tools for network scanning and packet analysis.

### 1. Install Nmap

Nmap (Network Mapper) is essential for network discovery and security auditing.

| Operating System | Download Link | Notes |
| :--- | :--- | :--- |
| **Windows** | [nmap-7.98-setup.exe](https://nmap.org/dist/nmap-7.98-setup.exe) | Use the installer to set up Nmap and Npcap. |
| **Linux (RPM)** | [nmap-7.98-1.x86_64.rpm](https://nmap.org/dist/nmap-7.98-1.x86_64.rpm) | **Alternative:** Use your distribution's package manager (e.g., `sudo apt install nmap`). |
| **macOS** | [nmap-7.98.dmg](https://nmap.org/dist/nmap-7.98.dmg) | Mount the disk image and install the application. |

---

## 🔍 Phase 2: Network Scanning with Nmap

### 2. Find Local IP Range

Before scanning, determine your local network's IP address and range.

| Operating System | Command | Purpose |
| :--- | :--- | :--- |
| **Linux/macOS** | `ip addr show` or `ifconfig` | Shows network interface configurations and your local IP. |
| **Windows** | `ipconfig` | Shows network configuration, including the IPv4 address. |

Use your local IP (e.g., `192.168.171.128`) to determine the subnet range (e.g., `192.168.171.0/24`).

### 3. Perform TCP SYN Scan

Execute a fast, stealthy scan across your local subnet to discover active hosts and open ports.

```bash
# Replace the IP range with your actual subnet
nmap -sS 192.168.171.128/24
