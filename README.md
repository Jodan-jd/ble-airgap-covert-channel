# 📡 BLE-Based Covert Channel in Air-Gapped Systems

## 📌 Overview

This project explores a covert communication channel that exploits Bluetooth Low Energy (BLE) to exfiltrate data from air-gapped systems.

Air-gapped systems rely on physical isolation for security. However, modern devices with built-in BLE introduce potential side-channel communication paths that can bypass traditional network isolation.

---

## 🚀 Key Contributions

* 📡 Designed a **connection-based covert communication channel using BLE**
* ⚡ Achieved **15–29 KB/s data exfiltration rate**
* 🚀 Demonstrated **64–127× improvement** over advertisement-based methods
* 🔁 Enabled **bidirectional communication without pairing or user interaction**
* 🛡️ Proposed a **detection approach using BLE sniffing and behavioral analysis**

---

## 🧠 Core Concept

### 🔗 Connection-Based BLE Communication

Unlike traditional approaches using BLE advertisements, this system leverages:

* BLE **connection mode**
* Higher bandwidth data transfer
* Bidirectional communication

---

### 🔁 Covert Data Exfiltration

* Operates without user interaction
* Uses GATT-based communication
* Enables command-and-control (C2) channel
* Supports structured data transfer via fragmentation

---

### 🛡️ Detection Strategy

To counter this threat, the project proposes:

* BLE traffic monitoring using sniffing tools
* Behavioral detection based on:

  * Unusual connection patterns
  * High-volume data transfer
  * Lack of pairing/authentication

---

## 🛠️ Technologies

* Bluetooth Low Energy (BLE)
* GATT Protocol
* BLE Sniffing (nRF52840)
* macOS / BLE-enabled systems

---

## 📊 Experimental Highlights

* Data Rate: **15.2 – 29.97 KB/s**
* Communication Range: **50 – 125 feet**
* Channels Used: 37 frequency-hopping channels

---

## 📂 Project Structure

```
ble-airgap-covert-channel/
├── README.md
├── ARCHITECTURE.md
├── docs/
│   └── project-report.pdf
└── assets/
```

---

## 📄 Research Paper

👉 View Full Report:
docs/Project - report.pdf

---

## 🧩 Architecture

👉 Detailed system design and communication flow available in:
ARCHITECTURE.md

---

## 🔐 Implementation Note

The implementation code for this project is not publicly shared due to the sensitive nature of the research.

This repository focuses on:

* System design
* Research insights
* Security implications

---

## 🎯 Key Insights

* Air-gap isolation is not sufficient in modern environments
* BLE introduces covert communication risks
* Connection-based techniques significantly increase attack capability
* Detection requires behavioral and protocol-level analysis

---

## ⚠️ Ethical Consideration

This work is intended for:

* Security research
* Defensive system design
* Awareness of emerging threats

Not for malicious use.

---

## 🧠 Perspective

This project reflects my interest in:

* Advanced threat modeling
* Wireless and embedded security
* Covert communication channels
* Bridging offensive research with defensive strategies

---

## 📫 Connect

* LinkedIn: https://www.linkedin.com/in/ijohndaniel/
