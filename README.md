# 🦉 OFlow

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OFlow** — Network Flow / Connection Session Analyzer

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Network flow & connection session analyzer — ss/netstat/proc, anomalies, baseline diff

---

## ✨ Features

- Ingest from /proc/net/{tcp,tcp6,udp,udp6,raw}, `ss -antup`, `netstat -antup` or a saved text dump (format auto-detected: ss / netstat / proc table)
- Unified flow records — proto, local/remote address, ports, state, inode, uid, pid, process, cmdline
- Flow table — sort / filter by state, port, process, remote IP, listening vs established views
- Offline Geo/ASN stub — private / public / loopback / link-local / CGNAT / multicast / bogon classes, well-known service map, optional local JSON enrichment file (CIDR → label / ASN / country)
- Anomaly heuristics — fan-in / fan-out to one remote, rare high-port listeners, wildcard listeners, long- lived odd sessions, reverse-shell heuristics, spike-vs-baseline, half-open SYN floods
- Baseline snapshots + diff (new listeners, new remotes, new processes, vanished services)
- PCAP-lite — summarise `tcpdump -nn` text or run `tcpdump -nn -r file.pcap` (graceful if missing)
- Process ↔ socket map via /proc/<pid>/fd inodes
- Export TXT / CSV / JSON with location chooser, clipboard copy, live watch mode
- Full CLI (--ss, --file, --watch, --json, --baseline, --diff, --pcap, --anomalies, --version ...)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OFlow
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
