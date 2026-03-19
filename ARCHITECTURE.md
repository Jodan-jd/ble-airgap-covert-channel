# 📡 System Architecture — BLE Covert Channel in Air-Gapped Systems

## 📌 Overview

This document describes the system architecture of a covert communication channel that leverages Bluetooth Low Energy (BLE) to exfiltrate data from air-gapped environments.

The system is designed to bypass traditional network isolation by exploiting BLE connection capabilities available in modern computing devices.

---

## 🧠 Architecture Summary

The system consists of two primary components:

* **Transmitter (Air-Gapped System)**
* **Receiver (External Device / Attacker System)**

Communication is established using BLE connection mode without requiring device pairing or user interaction.

---

## 🔗 High-Level Communication Flow

```id="jhjcbi"
[Air-Gapped Device]  →  BLE Connection  →  [Receiver Device]
       (Data Source)                           (Data Sink)
```

---

## ⚙️ System Components

### 🖥️ 1. Air-Gapped Device (Transmitter)

* Contains sensitive data
* Runs covert transmission logic
* Uses BLE peripheral role
* Encodes and fragments data for transmission

#### Responsibilities:

* Establish BLE connection
* Accept commands from receiver
* Read sensitive data (files, system info)
* Transmit data in chunks

---

### 📡 2. Receiver Device (Attacker System)

* Located within BLE range
* Acts as BLE central device
* Initiates connection and controls communication

#### Responsibilities:

* Discover BLE devices
* Establish connection
* Send commands
* Receive and reconstruct data

---

## 🔁 Communication Protocol

### BLE Mode Used:

* **Connection Mode (NOT advertisement mode)**

### Key Characteristics:

* Bidirectional communication
* No pairing required
* Uses GATT services

---

### 🧩 GATT Structure

* **Service UUID** → identifies covert service
* **Command Characteristic** → Receiver → Transmitter
* **Response Characteristic** → Transmitter → Receiver

---

## 🔄 Data Flow

### Step-by-step process:

1. Receiver scans for BLE devices
2. Detects transmitter using predefined identifiers
3. Establishes BLE connection
4. Sends command (e.g., request file/data)
5. Transmitter processes command
6. Data is fragmented into chunks
7. Transmitter sends data via BLE packets
8. Receiver reconstructs original data

---

## ⚡ Performance Optimization

The system improves throughput by:

* Using **connection mode instead of advertisement mode**
* Leveraging:

  * 37 frequency-hopping data channels
  * Multiple packets per connection event
* Implementing batch transmission

---

## 📊 Performance Characteristics

* Data Rate: **15–29 KB/s**
* Range: **50–125 feet**
* Communication Type: Bidirectional
* Detection Difficulty: Moderate to High

---

## 🛡️ Detection Architecture

A defensive monitoring system can be implemented using BLE sniffing tools.

### Detection Strategy:

* Monitor BLE traffic patterns
* Identify:

  * High data throughput
  * Absence of pairing
  * Continuous connections
* Use behavioral heuristics rather than signatures

---

## ⚠️ Threat Model

### Assumptions:

* Both devices are pre-compromised
* BLE capability is enabled
* Devices are within communication range

---

### Attack Capabilities:

* Data exfiltration
* Remote command execution
* Persistent covert communication

---

## 🔐 Security Implications

* Air-gap isolation is no longer sufficient
* BLE introduces covert channels in modern systems
* Traditional network monitoring cannot detect this activity

---

## 🎯 Design Insights

* Connection-based BLE communication significantly increases attack efficiency
* Covert channels can exist without user interaction
* Detection requires protocol-level monitoring

---

## ⚠️ Ethical Note

This architecture is presented for:

* Security research
* Defensive system design
* Awareness of emerging threats

Not for malicious use.
