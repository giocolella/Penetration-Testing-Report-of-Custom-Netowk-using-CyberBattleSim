# 🔥 Penetration Testing Report of Custom Netowork using CyberBattleSim and comparison with other simulators and real life tools
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
6. [Setup Guide](#-setup-guide)
7. [Tools & Documentation](#-tools--documentation)

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
- 🧠 **Study Reinforcement Learning-based attackers and defenders** in different network environments.
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

#### **CybORG CAGE 4**
- Challenge that shows the features of the CybORG tool
- Simulated but also realistic network environments with API-driven agents  
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
- Host machine capable of running multiple VMs
- Minimum recommended: 16 GB RAM, multi-core CPU
### **Software**
- Python 3.x
- Virtualization software (e.g., VirtualBox, VMware)
- CyberBattleSim, CybORG, NASim packages
- Infection Monkey package

## 📦 Setup Guide

### **Setup Guide for CyberBattleSim**

To correctly run **CyberBattleSim** on a Linux machine like Kali, follow these steps:

1. **Update the system:**

   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. **Install Miniconda**, if not already installed. It is recommended to download it from the official site.

3. **Clone the official repository:**

   ```bash
   git clone https://github.com/microsoft/CyberBattleSim.git
   cd CyberBattleSim
   ```

4. **Create a new conda environment for the simulator:**

   ```bash
   conda create -n cyberasim python=3.9
   conda activate cyberbattlesim
   ```

5. **Install the dependencies:**

   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   pip install jupyter ipykernel
   pip install asciichartpy pre-commit
   pip install --upgrade pyright
   pip install torch --index-url https://download.pytorch.org/whl/cpu
   ```

6. **Run the initialization script:**

   ```bash
   bash init.sh
   ```

7. **Register the kernel for Jupyter:**

   ```bash
   python -m ipykernel install --user \
     --name cyberbattlesim --display-name "CyberBattleSim"
   ```

8. **Install the package in editable mode so its dependencies are visible to Jupyter:**

   ```bash
   pip install -e .
   ```

9. **After downloading the repository, replace the file** `learner.py` **in:**

   ```
   /CyberBattleSim/cyberbattle/agents/baseline
   ```


### **Setup Guide for CAGE 4**

To configure the environment for Challenge CAGE 4, proceed as follows:

1. **Create and activate the environment:**

   ```bash
   conda create -n cage4 python=3.10 -y
   conda activate cage4
   ```

2. **Clone the official repository:**

   ```bash
   git clone https://github.com/cage-challenge/cage-challenge-4.git
   cd cage-challenge-4
   ```

3. **Manually install PyTorch:**

   ```bash
   pip install torch==2.2.0 --index-url https://download.pytorch.org/whl/cpu
   ```

4. **Remove the line `torch==2.2.0` from `Requirements.txt`, since it was already installed separately.**

5. **Install the dependencies:**

   ```bash
   pip install -r Requirements.txt
   pip install jupyterlab ipykernel
   ```

6. **Register the Jupyter kernel:**

   ```bash
   python -m ipykernel install --user --name cage4 --display-name "Python (cage4)"
   ```

7. **Install the package in editable mode:**

   ```bash
   pip install -e .
   ```

8. **After downloading the repository, replace the file** `FiniteStateRedAgent.py` **inside:**

   ```
   /CybORG/Agents/SimpleAgents
   ```

###  **Setup Guide for NASim (Network Attack Simulator)**

To correctly run NASim, proceed as follows:

1. **Update the system:**

   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

2. **Install Miniconda**, if not already installed.

3. **Create and activate a new conda environment:**

   ```bash
   conda create -n nasim python=3.11 -y
   conda activate nasim
   ```

4. **Clone the official repository from the `master` branch:**

   ```bash
   git clone -b master https://github.com/Jjschwartz/NetworkAttackSimulator.git
   cd NetworkAttackSimulator
   ```

5. **Enter the `docs` folder and install the documentation requirements:**

   ```bash
   cd docs
   pip install -r requirements.txt
   ```

6. **Install PyTorch (CPU version):**

   ```bash
   pip install torch --index-url https://download.pytorch.org/whl/cpu
   ```

7. **Return to the root directory:**

   ```bash
   cd ..
   ```

8. **Install optional NASim extensions:**

   ```bash
   pip install nasim[dqn]
   pip install nasim[test]
   pip install nasim[docs]
   ```

9. **Install additional dependencies:**

   ```bash
   pip install jupyterlab ipykernel
   ```

10. **Register the Jupyter kernel:**

    ```bash
    python -m ipykernel install --user \
      --name nasim --display-name "NetworkAttackSimulator"
    ```

11. **Install the package locally in editable mode:**

    ```bash
    pip install -e .
    ```

12. **After downloading the repo, replace the file** `ql-replay_agent.py` **inside:**

    ```
    /nasim/agents
    ```

### **Setup Guide for Infection Monkey on Ubuntu 18.04 Desktop (Bionic Beaver)**

To correctly configure Infection Monkey on a virtual machine with **Ubuntu 18.04 Desktop (Bionic Beaver)**, follow the steps below:

1. **Download Ubuntu 18.04 Desktop Bionic Beaver.**

2. **If the terminal doesn’t start, apply the following workaround:**

   ```
   Settings → Language & Settings → Change English (United States) to English (Canada)
   ```
   Then reboot the system.

3. **Enter TTY mode using Ctrl + Alt + F3 and elevate the current user to sudoer:**

   ```bash
   sudo usermod -aG sudo ubuntu
   ```

4. **Reboot the system.**

5. **Update packages:**

   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

6. **Remove any previous MongoDB installations:**

   ```bash
   sudo systemctl stop mongod
   sudo apt purge mongodb mongodb-server mongodb-server-core mongodb-clients
   sudo rm -rf /var/lib/mongodb
   sudo rm -rf /etc/mongodb.conf
   ```

7. **Add MongoDB 4.2 repository:**

   ```bash
   wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -
   echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list
   sudo apt update
   ```

8. **Install MongoDB and required tools:**

   ```bash
   sudo apt install -y mongodb-org
   dpkg --purge mongo-tools
   sudo rm -f /usr/bin/bsodump
   sudo apt-get clean
   sudo apt-get update
   sudo apt-get install -y mongodb-org-tools mongodb-org
   sudo dpkg --configure -a
   sudo apt-get install -f
   sudo systemctl restart mongod
   ```

9. **Download the Infection Monkey AppImage:**

   ```bash
   https://github.com/guardicore/monkey/releases/tag/v2.3.0
   ```

10. **Place the `.AppImage` in your home directory and run it:**

   ```bash
   chmod +x InfectionMonkey-v2.3.0.AppImage
   ./InfectionMonkey-v2.3.0.AppImage
   ```

> **Note:** Before each run, it is recommended to restart the MongoDB service:
>
> ```bash
> sudo systemctl restart mongod
> ```

11. **Access the web interface:**

   ```
   http://localhost:5000 (use Firefox browser)
   ```

12. **In `Configurations → Network`:**

   - Enable the checkbox **Agent Scan**
   - Exclude any specific IPs you don’t want to scan

13. **In `Configurations → Plugins`:**

   - Download all plugins marked as **SAFE**

14. **Manually enter common credentials to test (examples):**

   ```
   "user,user"  "root,toor"  "SHaylett,SHaylett"
   ```

15. **Ensure all virtual machines involved are connected to the same NAT Network.**


## 📚 Tools & Documentation
[CyberBattleSim](https://github.com/microsoft/CyberBattleSim)

[CybORG Cage 4](https://github.com/cage-challenge/cage-challenge-4)

[NASim](https://github.com/Jjschwartz/NetworkAttackSimulator/tree/master)

[NASim Docs](https://networkattacksimulator.readthedocs.io/en/latest/index.html)

[Infection Monkey](https://www.akamai.com/it/infectionmonkey)

[Infection Monkey Docs](https://techdocs.akamai.com/infection-monkey/docs/welcome-infection-monkey)

