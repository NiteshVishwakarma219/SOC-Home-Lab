# 🚨 Incident Response Report – Brute Force Attack Detection

---

# 📌 Incident Summary

* **Incident Type:** Brute Force Attack
* **Severity:** Medium
* **Status:** Investigated
* **Detected By:** Splunk SIEM Alert

---

# 🧠 Description

A potential brute force attack was detected based on multiple failed login attempts observed within a short time frame. The activity indicates an attempt to gain unauthorized access to the system.

---

# ⏱️ Timeline of Events

| Time | Event                                    |
| ---- | ---------------------------------------- |
| T1   | Multiple failed login attempts initiated |
| T2   | Sysmon logs generated                    |
| T3   | Logs forwarded to Splunk                 |
| T4   | Detection query triggered                |
| T5   | Alert generated                          |

---

# 🔍 Investigation Details

## Log Source

* Windows Event Logs
* Sysmon Logs

## Detection Query Used

```id="3jz0qe"
index=wineventlog EventCode=4625
```

## Findings

* Repeated login failures detected
* Attempts originated from a single source
* High frequency of attempts indicates brute force behavior

---

# ⚠️ Indicators of Compromise (IOCs)

* Multiple failed login attempts
* Suspicious login patterns
* Repeated authentication failures

---

# 🧪 Root Cause Analysis

The attack was caused by an external entity attempting to guess user credentials using automated tools.

---

# 🛡️ Response Actions Taken

* Alert triggered in Splunk
* Logs analyzed
* Attack pattern identified

---

# ✅ Recommendations

* Implement account lockout policies
* Enable multi-factor authentication (MFA)
* Monitor login attempts continuously
* Strengthen password policies

---

# 📊 Conclusion

The SOC lab successfully detected and analyzed a brute force attack using SIEM tools. The system demonstrated effective monitoring, detection, and alerting capabilities.

---
