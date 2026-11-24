# 🦉 OFlow

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OFlow** — Network Flow / Connection Session Analyzer

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OFlow — Network Flow / Connection Session Analyzer. It provides ingest from /proc/net/{tcp,tcp6,udp,udp6,raw}, `ss -antup`, `netstat -antup` or a saved text dump (format auto-detected: ss / netstat / proc table). Operators can export results (including machine-readable formats) and gate CI with severity thresholds where supported.

---

## ✨ Features

- Ingest from /proc/net/{tcp,tcp6,udp,udp6,raw}, `ss -antup`, `netstat -antup` or a saved text dump (format auto-detected: ss / netstat / proc table)
- Unified flow records — proto, local/remote address, ports, state, inode, uid, pid, process, cmdline
- Flow table — sort / filter by state, port, process, remote IP, listening vs established views
- Offline Geo/ASN stub — private / public / loopback / link-local / CGNAT / multicast / bogon classes, well-known service map, optional local JSON enrichment file (CIDR → label / ASN / country)
- Anomaly heuristics — fan-in / fan-out to one remote, rare high-port listeners, wildcard listeners, long- lived odd sessions, reverse-shell heuristics, spike-vs-baseline, half-open SYN floods
- Baseline snapshots + diff (new listeners, new remotes, new processes, vanished services)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OFlow                                     # interactive menu
./OFlow --file sample.txt
./OFlow --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OFlow --help   # watch every network call
firejail --net=none ./OFlow --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
