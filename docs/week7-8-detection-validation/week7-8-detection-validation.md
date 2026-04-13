# Week 7–8: Detection Validation & Empirical Benchmarking  
## Focus Area: Detection Performance in Distributed Cloud Architectures

---

# 🔁 Research Continuity (Weeks 1–6 → Week 7–8)

Weeks 1–4:
- Designed secure-by-design distributed cloud architecture.
- Implemented segmentation and hardened configurations.

Weeks 5–6:
- Performed control validation.
- Simulated SSH brute-force attacks.
- Validated Wazuh alert generation.
- Confirmed log ingestion and correlation pipeline.

📌 Week 7–8 Focus:

Shift from:
> “Does detection work?”

To:
> “How well does detection perform under real conditions?”

---

# 🧪 1. Experimental Environment Validation

### Wazuh Dashboard Overview
![Figure 1 – Wazuh Dashboard Overview](../00-research-assets/screenshots/week7-8-detection-validation/figure1-wazuh-dashboard-overview.png)

### Agent Connectivity Status
![Figure 2 – Wazuh Agent Connected](../00-research-assets/screenshots/week7-8-detection-validation/figure2-wazuh-agent-connected.png)

### Baseline Security Events
![Figure 3 – Baseline Security Events](../00-research-assets/screenshots/week7-8-detection-validation/figure3-wazuh-security-events-baseline.png)

📌 Observation:
- Agent successfully connected.
- Events flowing into SIEM.
- System ready for controlled experimentation.

---

# 🧪 2. File Integrity Monitoring (FIM) Validation

### File Modification Command Execution
![Figure 4 – File Modification Command](../00-research-assets/screenshots/week7-8-detection-validation/figure4-file-modification-command.png)

### Local System Log Confirmation
![Figure 5 – Local Log File Change](../00-research-assets/screenshots/week7-8-detection-validation/figure5-local-log-file-change.png)

### Wazuh FIM Detection Alert
![Figure 6 – Wazuh FIM Detection](../00-research-assets/screenshots/week7-8-detection-validation/figure6-wazuh-fim-detection.png)

📌 Key Insight:
- File change successfully detected.
- Confirms:
  - Log collection ✅
  - FIM engine ✅
  - Alert generation ✅

---

# 🧪 3. SSH Service & Network Validation

### SSH Service Status
![Figure 7 – SSH Service Running](../00-research-assets/screenshots/week7-8-detection-validation/figure7-ssh-service-running.png)

### Network Connectivity Test
![Figure 8 – Network Connectivity](../00-research-assets/screenshots/week7-8-detection-validation/figure8-network-connectivity-test.png)

📌 Observation:
- SSH service active.
- Network communication between nodes confirmed.

---

# 🧪 4. Attack Preparation

### Password List Preparation
![Figure 9 – Password List](../00-research-assets/screenshots/week7-8-detection-validation/figure9-password-list-preparation.png)

📌 Purpose:
- Enable controlled brute-force simulation.

---

# 🧪 5. Brute Force Attack Execution

### Hydra Attack Launch
![Figure 10 – Hydra Attack Execution](../00-research-assets/screenshots/week7-8-detection-validation/figure10-hydra-attack-launch.png)

### SSH Authentication Failures (Target Logs)
![Figure 11 – SSH Authentication Failures](../00-research-assets/screenshots/week7-8-detection-validation/figure11-ssh-authentication-failures.png)

📌 Key Validation:
- Attack successfully generated.
- Failed login attempts recorded in system logs.

---

# 🧪 6. Detection & Correlation Validation

### Wazuh SSH Event Ingestion
![Figure 12 – Wazuh SSH Events](../00-research-assets/screenshots/week7-8-detection-validation/figure12-wazuh-ssh-events.png)

### Brute Force Detection Alert
![Figure 13 – Wazuh Brute Force Detection](../00-research-assets/screenshots/week7-8-detection-validation/figure13-wazuh-bruteforce-detection.png)

📌 Insight:
- Logs ingested into Wazuh.
- Detection rules triggered.
- Correlation engine functioning correctly.

---

# 🧪 7. Alert Investigation

### Alert Detail Analysis
![Figure 14 – Alert Investigation](../00-research-assets/screenshots/week7-8-detection-validation/figure14-alert-investigation-details.png)

📌 Observation:
- Alert includes:
  - Source IP
  - Attack pattern
  - Rule classification

---

# 🧪 8. End-to-End Detection Validation

### Full Detection Pipeline Confirmation
![Figure 15 – End-to-End Detection](../00-research-assets/screenshots/week7-8-detection-validation/figure15-end-to-end-detection-validation.png)

📌 Validated Pipeline:

Attack → System Logs → Wazuh Agent → SIEM → Alert

---

# 📊 9. Key Experimental Findings

- Detection pipeline successfully validated end-to-end.
- File Integrity Monitoring operates in real-time.
- SSH brute-force activity generates observable logs.
- Wazuh effectively ingests and correlates events.
- Alerts provide actionable security intelligence.

---

# ⚠️ 10. Observed Limitations

- Detection latency not yet quantitatively measured.
- No stress testing under high-volume attack conditions.
- Limited benchmarking across distributed nodes.
- No formal comparison of detection performance metrics.

---

# 🔍 11. Research Gaps Identified

- Lack of empirical detection latency benchmarking frameworks.
- Limited evaluation of SIEM performance under adversarial load.
- Absence of reproducible small-scale distributed testing models.
- Minimal real-world validation of detection pipelines.

---

# ❓ 12. Refined Research Questions

1. How does architecture segmentation affect detection latency?
2. What is the impact of log volume on detection accuracy?
3. How resilient is detection under node isolation?
4. Can detection benchmarking improve secure architecture design?

---

# 🚀 13. Next Phase (Beyond Week 8)

- Introduce detection latency measurement.
- Simulate high-volume attack scenarios.
- Perform distributed node benchmarking.
- Quantify SIEM performance metrics.

---

# 🎯 Long-Term Direction

Transition from:

> Functional validation

To:

> Measurable, reproducible detection benchmarking framework  
for distributed cloud-native architectures.