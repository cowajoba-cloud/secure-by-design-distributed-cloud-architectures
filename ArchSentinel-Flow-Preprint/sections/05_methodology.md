# 🧪 5. Methodology: The ArchSentinelFlow Distributed Laboratory

The research was conducted within a custom-engineered, distributed cloud-native simulation environment hosted on a dedicated **ArchSentinelFlow Research Node** (DreamQuestPro Platform). This methodology prioritizes **"Deterministic Observability"** to ensure that every adversarial action is logged, indexed, and measurable across distributed trust boundaries.

### 5.1 System Specifications & Hypervisor Tier
The laboratory utilizes a Type-2 Hypervisor (VirtualBox 7.0) to orchestrate a heterogeneous cluster of nodes, ensuring a high-fidelity representation of an enterprise-distributed cloud:

*   **Host Platform**: DreamQuestPro Mini PC (Intel 12th Gen | 16GB RAM)
*   **Sentinel Node (Ubuntu Desktop 24.04)**: Acting as the CI/CD Runner and primary ingestion target (4 vCPUs | 3.1GB RAM).
*   **Governance Node (Wazuh Manager)**: A standalone SIEM/XDR orchestrator for policy enforcement and telemetry correlation.
*   **Adversarial Node (Kali Linux 2025.4)**: Native pentesting suite for multi-vector simulations (Hydra v9.6).

### 5.2 Operational Connectivity & Agent Synchronization
To ensure a high-integrity telemetry pipeline, all distributed nodes were synchronized via the Wazuh Governance Node. This provides the real-time "Pulse" required for sub-minute detection performance and continuous architectural monitoring.

![ArchSentinelFlow Agent Synchronization](../assets/fig_arch_03_active_agents.png)
*Figure 3: Live Ingestion Status confirming active synchronization between the Sentinel Node (Ubuntu) and Adversarial Node (Kali).*


### 5.3 Deterministic Network Topology
To maintain architectural integrity and ensure non-repudiation, a strictly deterministic **Static IP Hierarchy** was implemented across the Host-Only Network (192.168.56.0/24). This removes the variable "noise" of dynamic addressing, allowing for precise latency measurement.


| Research Node | Role / Identity | Static IP |
| :--- | :--- | :--- |
| **Ubuntu Server** | CI/CD + Core Infrastructure | `192.168.56.10` |
| **Kali Linux** | Adversarial Node (Red Team) | `192.168.56.20` |
| **Ubuntu Desktop** | Sentinel Node (Runner/Target) | `192.168.56.30` |
| **Wazuh Manager** | Governance Node (SIEM/XDR) | `192.168.56.100` |

### 5.4 Experimental Design: The "Single-Strike" Validation
The core experiment involved a high-velocity adversarial ingestion attempt (SSH Brute Force) initiated by the Adversarial Node (.20) against the Sentinel Node (.30). Telemetry was captured at the kernel level by the Sentinel Agent and transmitted to the Governance Node (.100) for real-time analysis and MITRE ATT&CK mapping.

---
