# 🔐 Secure-by-Design Distributed Cloud Architectures

A structured research project focused on designing, validating, and benchmarking detection capabilities in distributed cloud-native environments.

---

# 📌 Research Overview

This project explores:

- Secure architecture design  
- Threat modeling and attack surface analysis  
- Control validation using real-world attack simulation  
- Detection engineering and SIEM validation  
- Empirical benchmarking of detection performance  

---

# 🧠 Research Progression

## 🏗️ Weeks 1–2: Architecture Design
- Designed distributed cloud architecture  
- Defined trust boundaries and system components  

---

## ⚠️ Weeks 3–4: Threat Modeling
- STRIDE analysis  
- Attack surface identification  
- Adversary modeling  

---

## 🛡️ Weeks 5–6: Control Validation
- Deployed Wazuh SIEM  
- Simulated SSH brute-force attacks  
- Validated detection rules  
- Confirmed log ingestion pipeline  

📸 Evidence includes:
- Attack execution logs  
- Wazuh alert correlation  
- MITRE ATT&CK mapping  

---

## 🧪 Weeks 7–8: Detection Validation & Benchmarking

Focus:
> Moving from functional validation → performance validation

### Key Activities:
- File Integrity Monitoring (FIM) validation  
- SSH brute-force detection  
- End-to-end detection pipeline verification  
- Alert investigation and correlation analysis  

### Key Outcomes:
- Verified full detection pipeline:
  - Attack → Logs → Wazuh Agent → SIEM → Alert  
- Confirmed real-time detection capability  
- Identified limitations in detection benchmarking  

---

# 📊 Research Direction

This project is evolving toward:

> A reproducible detection benchmarking framework  
for distributed cloud-native architectures

---

# 🔍 Identified Research Gaps

- Lack of detection latency benchmarking  
- Limited SIEM stress testing  
- No standardized validation frameworks  
- Minimal real-world distributed experimentation  

---

# 🚀 Next Phase

- Detection latency measurement  
- High-volume attack simulation  
- Distributed node benchmarking  
- Empirical performance evaluation  

---

# 🎯 Long-Term Goal

To develop:

> A structured, measurable, and reproducible framework  
for validating detection performance in distributed systems

---

# 🛠️ Technologies Used

- Wazuh (SIEM & XDR)  
- Kali Linux (Attack Simulation)  
- Ubuntu Desktop (Target System)  
- Hydra (Brute-force testing)  
- VirtualBox (Lab environment)  

---

# 📁 Repository Structure


---

# 📂 Repository Structure

```text
📁 Lab01-SecureDistributedCloud
│
├── 📄 README.md
│
├── 📁 docs
│ │
│ ├── 📁 00-research-assets
│ │ ├── 📁 diagrams
│ │ │ ├── secure-cloud-architecture.drawio
│ │ │ ├── week1-architecture-v1.1.png
│ │ │ └── threat-model-attack-surface-week3.png
│ │ │
│ │ └── 📁 screenshots
│ │     ├── 📁 week5-control-validation
│ │     ├── 📁 week6-extended-analysis
│ │     └── 📁 week7-8-detection-validation   ✅ (ADD THIS)
│ │
│ ├── 📁 week1-2-architecture
│ │ ├── 01-research-framing.md
│ │ ├── 02-system-architecture-design.md
│ │ ├── 03-design-rationale.md
│ │ └── 04-architecture-evaluation.md
│ │
│ ├── 📁 week3-4-threat-modelling
│ │ ├── 01-threat-model-overview.md
│ │ ├── 02-adversary-model.md
│ │ ├── 03-stride-analysis.md
│ │ ├── 04-attack-surface-analysis.md
│ │ └── 05-threat-prioritisation.md
│ │
│ ├── 📁 week5-6-control-validation
│ │ ├── 01-lab-objectives.md
│ │ ├── 02-environment-setup.md
│ │ ├── 03-control-mapping.md
│ │ ├── 04-experiments.md
│ │ ├── 05-results.md
│ │ ├── 06-discussion.md
│ │ └── 07-limitations-and-future-work.md
│ │
│ └── 📁 week7-8-literature-review   ✅ (ADD THIS)
│     └── week7-8-literature-review.md


# 📄 Licence

Academic and research use.

---

# 👤  Author

Charles Owajoba  
Cybersecurity | Cloud Security | Detection Engineering  

---

# 🌍 Vision

Bridging the gap between:

> Secure system design  
and  
> measurable detection effectiveness