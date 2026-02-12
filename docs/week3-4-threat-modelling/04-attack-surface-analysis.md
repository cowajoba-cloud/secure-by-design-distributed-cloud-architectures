# 04 — Attack Surface Analysis

## 1. Objective

To identify exposed interfaces and potential entry points within the system.

---

## 2. External Attack Surface

- SSH (Port 22)
- Network connectivity between nodes
- Log ingestion endpoints

---

## 3. Internal Attack Surface

- Privilege escalation vectors
- File system modification
- Misconfigured services

---

## 4. Monitoring Surface

- Authentication logs
- File integrity alerts
- System performance metrics

---

## 5. Observations

The primary attack vector is remote authentication.

Secondary risks include:
- Unauthorized file manipulation
- Resource exhaustion attacks

---

## 6. Implication for Control Validation

Attack surface findings directly inform the Week 5–6 experiment design.
