# Analysis_of_Algorithms
Semester Project!
# 🔐 SOC Project: Brute Force Detection using Wazuh SIEM & Bash

## 📌 Overview
This project simulates a real-world Security Operations Center (SOC) environment to detect and analyze SSH brute force attacks using Wazuh SIEM and a custom Bash log analysis script.

---

## 🛠️ Tools & Technologies
- Wazuh (SIEM & HIDS)
- Kali Linux (Attacker Machine)
- Hydra (Brute Force Tool)
- Ubuntu (Target System)
- Bash Scripting

---

## 🏗️ Architecture
Attacker (Kali Linux)  
↓  
Target System (Ubuntu - SSH Server)  
↓  
Wazuh Agent  
↓  
Wazuh Manager  
↓  
Elasticsearch + Kibana  
↓  
Detection & Alerts  

---

## ⚙️ Features
- Real-time brute force detection using Wazuh  
- SSH log monitoring (`/var/log/auth.log`)  
- Custom Bash script for log analysis  
- Detection of attacker IPs  
- IOC (Indicators of Compromise) extraction  
- Table-based output for readability  

---

## 🚨 Attack Simulation
Brute force attack performed using Hydra:

```bash
hydra -l root -P passwords.txt ssh://<target-ip>
