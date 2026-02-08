# Secure-by-Design Distributed Cloud Architectures

**Lab Project:** Research-Driven Security Engineering for Cloud-Native Systems
## Author : Charles Owajoba
*Project developed as part of MSc research at Sheffield Hallam University.*

Cloud and distributed systems underpin modern digital infrastructure across government, industry, and research domains. However, security incidents in these environments frequently arise not from zero-day exploits, but from **architectural weaknesses** such as misconfigurations, over-permissive access controls, and poorly defined trust boundaries.

This lab forms the first phase of a structured research programme investigating **secure-by-design distributed cloud architectures**, focusing on how architectural decisions, identity and access management (IAM), and threat modelling can reduce attack surfaces and improve system resilience.

This work is positioned to support **PhD-level research** in distributed systems security, trustworthy systems, and secure software engineering, while remaining grounded in **practical cloud security operations**.

---

## Week 1–2: Foundations

### Day 1 – Research Framing

- **Focus:** Understanding the problem of architectural weaknesses in cloud and distributed systems.  
- **Objective:** Bridge the gap between theoretical secure systems design and practical cloud security implementation.  
- **Outcome:** Defined research hypothesis, security assumptions, and practical research mapping.  

### Day 2 – Secure Architecture Design and Trust Boundary Definition

- **Focus:** Designing a secure distributed cloud architecture that operationalises Day 1 principles.  
- **Components:** External Users, API Gateway, Web Tier, Application Tier, Data Tier, Identity & Access Management, Observability Layer.  
- **Trust Boundaries:** TB1 → TB4 with explicit identity-driven controls.  

**Figure 1: Secure Distributed Cloud Architecture with Trust Boundaries**  

![Figure 1: Secure Distributed Cloud Architecture](diagrams/week1-architecture-v1.1.png)

> This architecture provides the baseline for Week 3–4 threat modelling, attack simulation, and DevSecOps pipeline integration.

---

## Week 3–4: Threat Modelling & STRIDE Analysis

- **Focus:** Systematic threat identification and adversary modelling using STRIDE.  
- **Activities:**  
  - Defining explicit trust boundaries in a cloud-native system  
  - Mapping attack surfaces across ingress, service-to-service, and data layers  
  - Applying STRIDE threat modelling to real cloud components  
  - Aligning threats with identity-driven controls, RBAC, and zero-trust principles  
  - Structuring artefacts for reproducibility, auditability, and future experimentation  

**Figure 2: Threat Model Attack Surface – Secure Distributed Cloud System**

![Figure 2: Threat Model Attack Surface](diagrams/threat-model-attack-surface-week3.png)

> All diagrams, threat models, and documentation are version-controlled and publicly available.

---

## Research Continuity & Lab Outputs

- **Controlled misconfiguration experiments** (Week 4)  
- **Detection engineering and SIEM validation**  
- **DevSecOps pipeline integration**  
- **PhD-level reproducibility** in secure distributed systems research  

---

## GitHub Repository

Access the full research artefacts, diagrams, and threat models here:  

👉 [GitHub: Week 3–4 Threat Modelling](https://github.com/cowajoba-cloud/secure-distributed-cloud-lab/tree/main/research/week3-4-threat-modelling)

# 🛡️ Secure Distributed Cloud Lab

This repository contains all lab documentation, research notes, and supporting resources for the **Secure Distributed Cloud** project. The structure is organized by weeks to reflect the lab workflow and design progression.

---

## 📂 Docs Structure

### Week 1-2: Architecture
🏗️ docs/week1-2-architecture/
└── research/
    ├── day1-research-framing.md
    └── day2-architecture-design.md

### Week 3-4: Threat Modelling
🛡️ docs/week3-4-threat-modelling/
└── research/
    ├── day1-threat-model-overview.md
    ├── day2-adversary-model.md
    └── day3-stride-analysis.md

### Week 5-6: Control Validation
🔬 docs/week5-6-control-validation/
├── 📝 01-lab-objectives.md
├── ⚙️ 02-environment-setup.md
├── 🗺️ 03-control-mapping.md
├── 🔬 04-experiments.md
├── 📊 05-results.md
├── 💬 06-discussion.md
└── ⚖️ 07-assets/
    ├── diagrams/
    └── notes/


**Notes:**

- 📝 Markdown files follow the **logical lab workflow** (Objectives → Setup → Mapping → Experiments → Results → Discussion).  
- 📂 `07-assets` contains all supporting **diagrams and notes** for the lab.  
- This layout is **clean, easy to follow**, and ensures anyone reviewing the lab sees the workflow first, then supporting materials.

---

## ⚡ Workflow Recommendation

1. Start with **01-lab-objectives.md** to understand the lab goals.  
2. Follow the workflow sequentially through **environment setup, control mapping, experiments, and results**.  
3. Reference supporting materials in **07-assets** as needed.

---

## 🚀 Next Steps

- Complete **Week 5-6 lab work** in the markdown files.  
- Keep diagrams and notes updated in `07-assets/`.  
- Commit regularly and maintain the folder naming convention for clarity.

