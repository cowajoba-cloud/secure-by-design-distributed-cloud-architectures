 ⚙️ Environment Setup – Week 5–6: Control Validation

## 5.1 Experimental Context

Weeks 5–6 focus on empirical validation of implemented detection controls under controlled adversarial simulation.

This phase evaluates:

- Detection accuracy  
- Alert generation fidelity  
- Log ingestion integrity  
- Rule transparency  
- Detection latency  

The objective is to validate monitoring effectiveness using measurable, repeatable attack scenarios.

---

## 5.2 Lab Infrastructure Overview

The experimental environment consists of isolated virtual machines within a host-only network.

### Virtual Machines Deployed

| VM | Role | Function |
|-----|------|----------|
| **Ubuntu Server** | Monitoring + Target Node | Hosts Wazuh stack and monitored services |
| **Kali Linux** | Adversary Simulation Node | Executes controlled attack scenarios |
| Ubuntu Desktop | Auxiliary endpoint | Extended endpoint validation |
| Metasploit VM | Exploitation platform | Advanced adversary simulation (Week 6) |
| OWASP VM | Application testing node | Secure SDLC experimentation |

---

## 5.3 Architectural Model

Unlike distributed SIEM deployments, this lab uses a **single-node Wazuh deployment**.

The Ubuntu Server performs dual roles:

1. Hosts:
   - Wazuh Manager
   - Wazuh Indexer
   - Wazuh Dashboard

2. Acts as:
   - Monitored endpoint via local Wazuh Agent

This consolidated architecture is acceptable for controlled academic experimentation but differs from production-grade distributed monitoring designs.

---

## 5.4 Network Architecture

- **Network Type:** Isolated Host-Only Network  
- **Subnet Example:** `192.168.56.0/24`  
- **Traffic Flow:**
  - Kali Linux → Attack source
  - Ubuntu Server → Target + Monitoring node

Connectivity validation performed:

ping <target-ip>

---
## 5.5 Security Monitoring Stack Configuration

### Wazuh Single-Node Deployment Characteristics

Installed on Ubuntu Server:

- Wazuh Manager  
- Wazuh Indexer (OpenSearch backend)  
- Wazuh Dashboard  
- Wazuh Agent (local agent monitoring the same host)  

Deployment properties:

- Encrypted internal communication  
- Real-time log ingestion  
- Rule-based detection engine  
- Integrated alert indexing  

This configuration enables direct mapping between raw log events and triggered security alerts.

---

## 5.6 Monitoring Capabilities Enabled

| Capability | Status | Purpose |
|-------------|----------|----------|
| Log analysis | Enabled | Authentication and system monitoring |
| SSH authentication monitoring | Enabled | Brute force detection validation |
| File Integrity Monitoring (FIM) | Enabled | File tampering detection |
| Rootcheck | Enabled | Host compromise indicators |
| Active Response | Disabled (controlled) | Prevent automated mitigation during experiments |

Active response is intentionally disabled to allow observation of detection behaviour without automated blocking.

---

## 5.7 Baseline Validation Procedures

Prior to executing experiments, the following validations are performed.

### Validate Wazuh Core Services

sudo systemctl status wazuh-indexer
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-dashboard
Expected tate : (running)
Validate Local Agent: sudo systemctl status wazuh-agent

Dashboard verification confirms:

Agent status: Active

Recent keep-alive timestamp

Validate SSH Service Availability
sudo systemctl status ssh


Ensures SSH is operational for authentication monitoring experiments.

Validate Authentication Log Generation
sudo tail /var/log/auth.log


Confirms real-time logging prior to adversarial simulation.

---

## 5.8 Experimental Integrity Controls

To preserve reproducibility and analytical validity:

Experiments executed within isolated lab environment

No external traffic interference

Manual control of attack intensity

Time synchronization verified across VMs

Logging confirmed operational before attack execution

Automated blocking mechanisms disabled

These controls ensure that observed alerts are attributable solely to controlled experimental activity.

---

## 5.9 Architectural Constraints

The single-node deployment introduces measurable limitations:

Monitoring stack and target share system resources

Potential performance degradation under heavy load

Reduced architectural realism compared to distributed SIEM deployments

Despite these constraints, this configuration remains technically appropriate for controlled detection validation experiments.

---

## 5.10 Justification for Wazuh Selection

Wazuh was selected due to:

Transparent rule-level inspection

Direct correlation between raw logs and generated alerts

Host-based intrusion detection capabilities

Support for authentication monitoring, file integrity validation, and rootcheck

Alignment with NIST detection and monitoring control families

This enables measurable, repeatable, and academically defensible evaluation of detection controls under controlled adversarial conditions.