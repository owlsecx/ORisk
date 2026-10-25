# 🦉 ORisk

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **ORisk** — USB device threat analysis and forensics: BadUSB/HID detection, risk scoring, quarantine and audit

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

ORisk is a USB threat-detection and monitoring tool (USB Guardian). It scans connected USB devices for threats such as BadUSB and HID emulation, monitors for new devices in real time, and supports whitelisting, quarantine, forensic dumps and reporting. Device fingerprints and audit history are stored in a persistent database.

---

## ✨ Features

- Deep USB threat analysis (BadUSB, HID emulation, spoofed VID/PID)
- Real-time monitoring with a configurable polling interval
- Device quarantine via udev rules plus whitelist/blocklist management
- Forensic dump of device tree, interfaces and endpoints
- SQLite-backed audit log with SHA-256 device fingerprints
- HTML and JSON export, multi-profile support and an offline self-test

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ORisk --scan
./ORisk --monitor -n 10
./ORisk --export-html report.html
./ORisk --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
