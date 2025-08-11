# 🔥 Penetration Testing Report of Custom Netowork using CyberBattleSim
**From Simulation to Real-World Penetration Testing & Ethical Hacking**

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![CyberSecurity](https://img.shields.io/badge/Security-PenTest-red.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()
[![License](https://img.shields.io/badge/License-TBD-lightgrey.svg)]()

---

## 📑 Table of Contents
1. [Overview](#-overview)
2. [Motivation](#-motivation--why-this-project)
3. [Components & Capabilities](#-components--capabilities)
4. [Integration / Architecture](#-integration--architecture)
5. [Requirements](#-requirements)
6. [Setup Guide](#-setup-guide-to-be-completed)
7. [Tools & Documentation](#-tools--documentation)
8. [Demo / Usage](#-demo--usage)
9. [Contributing / License](#-contributing--resources--license)

---

## 📌 Overview
This project explores **Cyber Battle** and **Network Attack Simulation** platforms, moving from purely simulated environments to controlled real-world penetration testing.  

We model and test different attack/defense scenarios using:
- Simulation frameworks: **CyberBattleSim**, **CybORG**, **NASim**
- Real-world tool: **Infection Monkey**

The goals are:
- Study attacker and defender behavior
- Compare simulation realism and usability
- Produce a structured **Penetration Testing Report** with results and tool comparisons

---

## 🎯 Motivation / Why This Project?
- 🧠 **Study Reinforcement Learning-based attackers** in different network environments.
- 🛡 **Evaluate security countermeasures** without risking production systems.
- ⚖ **Compare multiple platforms** for cyber range simulation in terms of realism, usability, and capabilities.
- 🌐 **Bridge simulation and real-world testing** to validate results.

---

## ⚙ Components & Capabilities

### 🖥 Simulators Analyzed
#### **CyberBattleSim**
- Python-based corporate network model  
- RL attacker/defender agents  
- Customizable topologies & vulnerability modeling  
- Supports scanning, exploitation, privilege escalation, lateral movement

#### **CybORG**
- Realistic network environments with API-driven agents  
- Zone-based segmentation  
- Variety of OS/services & vulnerabilities  
- Supports attacker/defender interaction with formal action definitions

#### **NASim**
- YAML-defined scenarios  
- Fully customizable topology  
- Multiple ML attacker agents available  
- No defender implementation

#### **Infection Monkey**
- Real-world penetration testing tool  
- Scanning & exploitation plugins  
- Works on Windows/Linux  
- Exploits: SMBExec, WMIExec, Log4Shell, MSSQL, RDP, Zerologon, etc.

---

### 🤖 Attacker Agents Implemented
- **Deep Q-Network (DQN Agent)**
- **Q-Learning with Replay Memory (QL Agent)**
- **Random Agent**

---

### 🛡 Defender Capabilities
- Scan & restore compromised nodes  
- Deploy decoys  
- Block/allow network traffic  
- Detect deception and degrade malicious services  

---

## 🏗 Integration / Architecture

### **Simulation Flow**
- Define network model — Nodes, services, vulnerabilities, credentials, firewall rules.
- Select attacker/defender agents — RL models or scripted behaviors.
- Run simulation — Probe, exploit, privilege escalation, lateral movement.
- Collect metrics — Steps to success, total cost, compromised hosts, defender actions.
- Analyze & compare — Performance of agents and tools.

### **Real-World Test Flow (Infection Monkey)**
- Setup NAT Network with intentionally vulnerable VMs (like Stapler1 and Metasploitable2).
- Deploy Infection Monkey agent.
- Monitor and log scanning/exploitation attempts.
- Compare effectiveness against simulated environments.

## 💻 Requirements
### **Hardware**
Host machine capable of running multiple VMs
Minimum recommended: 16 GB RAM, multi-core CPU
### **Software**
Python 3.x
Virtualization software (e.g., VirtualBox, VMware)
CyberBattleSim, CybORG, NASim packages
Infection Monkey package


