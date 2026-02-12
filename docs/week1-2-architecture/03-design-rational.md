# 03 — Design Rationale

## 1. Introduction

This document explains the reasoning behind the architectural decisions made for the Secure Distributed Cloud Lab.

The goal was to design a secure, observable, and testable distributed cloud environment suitable for threat modelling and control validation.

---

## 2. Architectural Philosophy

The design follows three core principles:

- Segmentation by role
- Observability by default
- Principle of least privilege

The system is intentionally simple but security-focused.

---

## 3. Component Justification

### 3.1 Wazuh Manager

Selected for:
- Centralised log collection
- File Integrity Monitoring (FIM)
- Intrusion detection
- Security event correlation

This enables measurable control validation in Week 5–6.

---

### 3.2 Wazuh Agent (Victim Node)

Acts as:
- Target system
- Monitored asset
- Attack surface representation

Provides:
- Authentication logs
- File integrity events
- System telemetry

---

### 3.3 Kali Linux (Attacker)

Chosen to simulate:
- SSH brute force
- Privilege escalation attempts
- Denial of Service simulation
- Information disclosure attempts

This creates controlled adversarial conditions.

---

## 4. Network Segmentation

The architecture enforces logical isolation between:

- Monitoring infrastructure
- Production simulation
- Adversary node

This prevents uncontrolled lateral movement.

---

## 5. Security Controls Embedded

Controls embedded include:

- Authentication monitoring
- File integrity validation
- Privilege monitoring
- System performance anomaly detection

---

## 6. Conclusion

The architecture was intentionally designed to enable measurable security validation rather than theoretical modelling.

It supports reproducibility, observability, and controlled experimentation.
