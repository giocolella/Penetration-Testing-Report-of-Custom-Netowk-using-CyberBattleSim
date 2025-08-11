# 🔥 Penetration Testing Report of Custom Netowork using CyberBattleSim
**From Simulation to Real-World Penetration Testing & Ethical Hacking**

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![CyberSecurity](https://img.shields.io/badge/Security-PenTest-red.svg)]()
[![License](https://img.shields.io/badge/License-TBD-lightgrey.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

---

## 📑 Table of Contents
1. [Overview](#-overview)
2. [Motivation](#-motivation--why-this-project)
3. [Components & Capabilities](#-components--capabilities)
4. [Architecture](#-integration--architecture)
5. [Requirements](#-requirements)
6. [Setup Guide](#-setup-guide-to-be-completed)
7. [Tools & Documentation](#-tools--documentation)
8. [Demo / Usage](#-demo--usage)
9. [Contributing / License](#-contributing--resources--license)

---

## 📌 Overview
This project explores **Cyber Battle** and **Network Attack Simulation** platforms, moving from purely simulated environments to controlled real-world penetration testing.  

We model and test different attack/defense scenarios using multiple simulation frameworks and real-world tools, focusing on:
- Studying attacker and defender behavior
- Comparing simulation realism and usability
- Producing a structured **Penetration Testing Report** with results and tool comparisons

---

## 🎯 Motivation / Why This Project?
- 🧠 Study **Reinforcement Learning-based** attackers in different network environments.
- 🛡 Evaluate **security countermeasures** without risking production systems.
- ⚖ Compare multiple platforms for cyber range simulation in terms of realism, usability, and capabilities.
- 🌐 Bridge **simulation and real-world testing**.

---

## ⚙ Components & Capabilities

### 🖥 Simulators Analyzed
- **CyberBattleSim** — Python-based, abstract corporate network model, RL attacker/defender agents, customizable topologies.
- **CybORG** — Realistic network simulations with API-driven agents, zone-based segmentation, OS/services diversity.
- **NASim** — YAML-defined scenarios, customizable topology, multiple ML attacker agents, no defender.
- **Infection Monkey** — Real-world attack simulation tool with scanning and exploitation plugins.

### 🤖 Attacker Agents Implemented
- Deep Q-Network (**DQN Agent**)
- Q-Learning with Replay Memory (**QL Agent**)
- **Random Agent**

### 🛡 Defender Capabilities
- Scanning & node restoration
- Deploying decoys
- Network traffic control

---

## 🏗 Integration / Architecture

### **Simulation Flow**
```text
[Define Network Model] → [Select Agents] → [Run Simulation] → [Collect Metrics] → [Analyze & Compare]
