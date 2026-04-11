# ⚙️ SOC Home Lab – Detailed Setup Guide

---

# 🧰 Overview

This guide explains how to build a SOC Home Lab with detailed steps and reasoning behind each configuration.

---

# 🖥️ Step 1: Create Virtual Environment

## What to Do

* Install VirtualBox or VMware
* Create:

  * Windows VM (Target)
  * Kali Linux VM (Attacker)

## Why This Step

A SOC analyst must monitor real systems under attack.
This setup simulates:

* Real attacker behavior
* Real system monitoring

---

# 💻 Step 2: Install Splunk Enterprise

## What to Do

* Download and install Splunk
* Access via browser

## Why This Step

Splunk acts as a **central SIEM platform** where:

* Logs are collected
* Data is analyzed
* Threats are detected

Without SIEM, SOC operations are not possible.

---

# ⚙️ Step 3: Install Sysmon

## What to Do

Run:
sysmon64.exe -i sysmonconfig.xml

## Why This Step

Default Windows logs are limited.
Sysmon provides:

* Process tracking
* Network activity
* File changes

This improves detection capability significantly.

---

# 🔗 Step 4: Configure Log Forwarding

## What to Do

* Install Splunk Universal Forwarder
* Forward Sysmon logs

## Why This Step

In real organizations:

* Logs are centralized
* Analysts don’t check each machine

This step simulates enterprise SOC architecture.

---

# 🔥 Step 5: Simulate Attacks

## What to Do

* Use Kali Linux to perform:

  * Brute force attack
  * Command execution

## Why This Step

Detection requires real data.
Simulating attacks:

* Generates logs
* Tests detection rules

---

# 🔍 Step 6: Perform Detection

## What to Do

Use Splunk queries:

* Failed login detection
* Process monitoring

## Why This Step

Detection is the core job of a SOC analyst.
This step shows:

* Analytical thinking
* Log investigation skills

---

# 🚨 Step 7: Create Alerts

## What to Do

* Configure alerts in Splunk

## Why This Step

SOC analysts rely on automation.
Alerts help:

* Detect threats faster
* Reduce manual monitoring

---

# 📊 Step 8: Build Dashboard

## What to Do

* Create visualization dashboards

## Why This Step

Dashboards provide:

* Real-time monitoring
* Quick insights
* Better decision-making

---

# ✅ Final Outcome

After completing this lab, you will:

* Understand SOC workflow
* Detect real-world attacks
* Gain hands-on SIEM experience

---
