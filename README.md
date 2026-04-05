# 📡 OFlow

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux%20%2F%20Windows-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-ORec%20%2F%20Network%20Recon-cyan?style=flat-square"/>
  <img src="https://img.shields.io/badge/Dependencies-scapy%20(optional)-yellow?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-v2.0-cyan?style=flat-square"/>
</p>

> **OFlow** is a powerful network traffic analyzer that performs live packet capture, displays top talkers, protocol breakdown, active connections, and generates detailed TXT reports.

**Real-time curses dashboard + quick stats mode. Requires root for packet capture.**

---

## 📌 Overview

OFlow captures and analyzes live network traffic on a selected interface. It provides a beautiful full-screen live dashboard showing top talkers, protocol statistics, and connection flows, plus the ability to run quick captures and export reports.

Ideal for network reconnaissance, traffic monitoring, and understanding communication patterns.

---

## 🖥️ Modules

| # | Module                  | Description |
|---|-------------------------|-------------|
| **[1]** | **Live Monitor**        | Real-time curses dashboard with live stats |
| **[2]** | **Interface Info**      | List all network interfaces with IP/MAC |
| **[3]** | **Quick Stats**         | Capture for N seconds then show summary report |
| **[4]** | **Export Last Session** | Save last capture to detailed TXT report |

---

## 📊 Key Features

- **Live Curses Dashboard** — Real-time top talkers, protocol breakdown, and top connections
- **Top Talkers** — Ranked by bytes transferred (TX/RX)
- **Protocol Breakdown** — Visual percentage bars for HTTP, HTTPS, SSH, DNS, etc.
- **Connection Tracking** — Active links with byte and packet counts
- **BPF Filter Support** — Filter traffic (e.g. `tcp port 80`, `host 192.168.1.1`)
- **Quick Stats Mode** — Short capture then instant report
- **Detailed TXT Export** — Full summary with top talkers, protocols, and connections
- **Scapy Integration** — Optional advanced packet parsing

---

## ⚙️ Requirements

- **Root / sudo** — Required for raw packet capture
- **scapy** (optional but recommended)
  ```bash
  pip install scapy
  chmod +x OFlow
  sudo ./OFlow

  📁 Output

Live Dashboard — Full-screen view with top talkers, protocol bars, and top connections
Summary Report — Packets, bytes, pkt/s, unique IPs, active links
TXT Report (in current directory):
oflow_<iface>_<timestamp>.txt — Complete analysis including top talkers, protocol breakdown, and connections



📦 Part of OwlSec Toolkit
This tool is part of the OwlSec suite — a collection of 300+ security and privacy tools.
🔗 owlsec.org

©️ License
Proprietary — © Khaled S. Haddad
Tools are distributed as pre-built executables. Source code is proprietary.
AUTHORISED SECURITY TESTING USE ONLY
