# 🛡️ Secure-by-Design Distributed Cloud Architectures

**Lab Project:** Research-Driven Security Engineering for Cloud-Native Systems  
**Author:** Charles Owajoba  
*MSc Research — Sheffield Hallam University*

---

## 📖 Overview

Modern distributed cloud systems frequently fail due to architectural weaknesses rather than zero-day exploits.

Misconfigurations.  
Over-permissive access controls.  
Poorly defined trust boundaries.

This lab investigates how **secure-by-design architectural decisions**, structured threat modelling, and empirical control validation can reduce attack surface and improve system resilience.

The project is structured as a staged research programme:

Architecture → Threat Modelling → Experimental Control Validation

This foundation supports future PhD-level research in:

- Distributed systems security  
- Trustworthy cloud architectures  
- Secure software engineering  
- Detection engineering & observability  

---

# 🏗️ Week 1–2 — Architecture Design

Focus:
- Secure distributed cloud system modelling
- Trust boundary identification
- Identity-driven segmentation
- Observability layer integration

**Architecture Diagram:**
 docs/00-research-assets/diagrams/week1-architecture-v1.1.png


This architecture forms the baseline for structured adversarial modelling.

---

# 🛡️ Week 3–4 — Threat Modelling (STRIDE)

Focus:
- Adversary modelling
- Trust boundary evaluation
- Attack surface analysis
- Risk prioritisation

Threats are systematically mapped using STRIDE and aligned with control strategy.

**Threat Model Diagram:**
docs/00-research-assets/diagrams/threat-model-attack-surface-week3.png


Outputs directly inform experimental design.

---

# 🔬 Week 5–6 — Control Validation & Experimental Security Testing

Focus:
- SSH brute force simulation
- File integrity tampering
- Privilege escalation attempts
- Denial-of-service simulation
- Detection engineering validation via Wazuh

Screenshots and artefacts stored under:
docs/00-research-assets/screenshots/


This phase transitions from theoretical modelling to empirical validation.

---

# 🎯 Research Methodology

The lab follows a layered engineering research approach:

1. Design secure architecture
2. Identify threats systematically
3. Prioritise risk
4. Validate controls experimentally
5. Evaluate detection effectiveness
6. Document limitations and future work

Each phase builds upon the previous.

Reproducibility is a core principle.

---

# 🛠 Technology Stack

- Wazuh (Intrusion Detection & Log Analysis)
- Kali Linux (Adversarial Simulation)
- Ubuntu Server (Monitored Node)
- Virtualized Lab Environment

---

# 📌 Research Positioning

This repository supports:

- MSc-level structured security research
- PhD-oriented distributed systems security exploration
- Practical cloud security engineering
- Detection engineering experimentation

It bridges theory and operational security.

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
│ │ ├── 📁 week5-control-validation
│ │ └── 📁 week6-extended-analysis
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
│ └── 📁 week5-6-control-validation
│ ├── 01-lab-objectives.md
│ ├── 02-environment-setup.md
│ ├── 03-control-mapping.md
│ ├── 04-experiments.md
│ ├── 05-results.md
│ ├── 06-discussion.md
│ └── 07-limitations-and-future-work.md


# 📄 Licence

Academic and research use.

---

# 👤 Author

Charles Owajoba  
Cyber Security & Software Engineering
