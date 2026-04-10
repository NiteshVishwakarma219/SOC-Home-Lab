# 🚨 Brute-Force Attack Detection using Splunk (SOC Project)

## 📌 Overview
This project demonstrates how a Security Operations Center (SOC) detects and responds to brute-force attacks using Splunk SIEM.

---

## 🛠️ Tools Used
- Splunk SIEM
- Kali Linux
- Windows/Linux System
- Sysmon
- Hydra

---

## ⚙️ Architecture
Kali Linux (Attacker) → Target System → Splunk

---

## ⚔️ Attack Simulation
A brute-force attack was simulated using Hydra:


hydra -l admin -P rockyou.txt ssh://<target-ip>


---

## 🔍 Detection Query


index=wineventlog EventCode=4625
| stats count by Account_Name, Source_Network_Address
| where count > 5


---

## 🚨 Outcome
- Detected brute-force attack
- Generated alerts
- Visualized attack patterns

---

## 📸 Screenshots
(To be added)

---

## 👨‍💻 Author
Nitesh Vishwakarma
