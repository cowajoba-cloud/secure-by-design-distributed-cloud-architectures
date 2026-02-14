# 🔬 Experiments – Week 5-6

# 🧪 Experiment 1 — SSH Brute Force Detection Validation

---

## 5.14 Baseline System State

- Prior to experimentation, the Wazuh dashboard was accessed to confirm operational readiness.

![Dashboard Baseline](../00-research-assets/screenshots/week5-control-validation/01_dashboard_baseline.png)

All services confirmed active.

---

## 5.15 Target Service Validation

SSH service confirmed active on Ubuntu Server.
- sudo systemctl status ssh

---

## 5.16 Attack Execution

- Controlled brute force simulation executed from Kali Linux:

# ✅ Recommended Method: sshpass Automated Simulation

- for i in {1..8}; do sshpass -p wrongpassword ssh -o StrictHostKeyChecking=no invaliduser@<UBUNTU-IP>; done

# Install first if needed:

- sudo apt install sshpass

## 🎯 Why This Method Is Recommended

- It Produces Clean, Controlled Telemetry
- Each attempt is independent.
- No interactive delay.
- No human typing variance.
- Consistent failure pattern.
- Same password each time.
- Same timing window.

That makes:

- Detection more predictable
- Logs easier to analyze
- Correlation clearer in Wazuh
- This is ideal for lab environments.

## 🔐 Why We Disabled Key Authentication

We used:

- -o PreferredAuthentications=password
- -o PubkeyAuthentication=no

or

- sshpass -p wrongpassword


Because:

- Modern SSH tries public key authentication first.

If you don’t disable it:

- The server logs extra authentication attempts.
- Detection noise increases.
- You don’t get pure password failure logs.

---

## 5.17 Detection Observation

- Security events observed in Wazuh Dashboard under the Ubuntu Server agent.

---

## 5.18 Rule-Level Analysis

- Expanded alert JSON reviewed to analyse rule ID, severity level, and source IP.

--- 

## 5.19 Control Effectiveness Assessment

- Observations:

- Alert triggered successfully

- Detection latency: <Insert measured seconds>

- Rule severity: <Insert level>

- Source IP correctly identified

- Log source integrity maintained

- The experiment confirms successful detection of authentication abuse attempts.