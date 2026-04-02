# 🛡️ ORisk

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-OUtility%20%2F%20USB%20Security-cyan?style=flat-square"/>
  <img src="https://img.shields.io/badge/Dependencies-None%20(Standalone)-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-v2.0-cyan?style=flat-square"/>
</p>

> **ORisk** is a powerful USB Guardian tool. It scans, monitors, and analyzes connected USB devices for risk indicators including BadUSB attacks, HID emulators, spoofed VID/PID, composite devices, and blocklisted hardware.

---

## 📌 Overview

ORisk protects your system from malicious USB devices by detecting suspicious behavior such as BadUSB emulators, keyboard/mouse HID spoofing, unknown manufacturers, and dangerous device combinations. It maintains a local database of seen devices, supports a user-defined whitelist, and provides real-time monitoring with clear risk scoring.

**⚠️ Requires root privileges** on Linux for full USB detection.

---

## 🖥️ Modules

| # | Module                  | Description |
|---|-------------------------|-------------|
| **[1]** | **Scan Devices**            | Full analysis of all connected USB devices with risk scoring |
| **[2]** | **Real-Time Monitor**       | Continuous monitoring with connect/remove alerts |
| **[3]** | **Whitelist — View**        | Show all trusted (whitelisted) devices |
| **[4]** | **Whitelist — Add**         | Add a VID:PID device to the trusted list |
| **[5]** | **Whitelist — Remove**      | Remove a device from the whitelist |
| **[6]** | **History**                 | View past scans and connect/remove events |
| **[7]** | **Export Last Scan**        | Save scan results to JSON file |
| **[8]** | **Test Detection**          | Test USB detection methods (lsusb + sysfs) |

---

## 📊 Key Features

- **Risk Scoring System** (0-100) with 5 severity levels (TRUSTED → CRITICAL)
- **Built-in Blocklist** — Known BadUSB, Rubber Ducky clones, HID emulators
- **HID & Composite Detection** — Dangerous keyboard + storage combos
- **Manufacturer & Serial Analysis** — Flags generic/unknown devices
- **Whitelisting Support** — Permanently trust specific VID:PID devices
- **Real-Time Monitoring** — Instant alerts on new or suspicious devices
- **History & Database** — Tracks first-seen and last-seen timestamps
- **Export** — Full JSON reports for forensic use

---

## ⚙️ Requirements

- **Linux only** (full functionality)
- **Root privileges** (`sudo`)
- **No additional Python packages** — uses `lsusb` and `/sys/bus/usb/devices`

---

## 🚀 Usage

```bash
sudo ./ORisk

📁 Output & Storage

Configuration & Database: ~/.orisk/
database.json — all seen devices and risk history
whitelist.json — trusted VID:PID list
history.json — scan and event timeline

Export: User-specified JSON file (e.g. orisk_export.json)


📦 Part of OwlSec Toolkit
This tool is part of the OwlSec suite — a collection of 300+ security and privacy tools.
🔗 owlsec.org

©️ License
Proprietary — © Khaled S. Haddad
Tools are distributed as pre-built executables. Source code is proprietary.

AUTHORISED SECURITY AUDITING USE ONLY
