# 🏛️ 3. Literature Review & The Governance Gap

Current academic discourse in distributed cloud security is characterized by high-level theoretical modeling but suffers from an **"Empirical Blind Spot."** This review evaluates the foundational work of leading researchers in the Australian and Global cybersecurity ecosystem to identify the critical "Governance Gap" that **ArchSentinelFlow** aims to bridge.

### 3.1 Analysis of Academic Frameworks
A cross-sectional analysis of contemporary research reveals a consistent emphasis on system design over operational performance:

*   **Data Protection & Access Control**: The work of **Abuadbba (UNSW)** and **Liu (Monash)** provides robust cryptographic and threat-modeling foundations. However, there remains a significant lack of empirical validation regarding runtime detection performance within operational SIEM environments.
*   **Scalability & Design**: Research by **Tari (RMIT)** and **Foo (QUT)** highlights the necessity of scalable distributed architectures but often omits security detection benchmarking as a core performance metric.
*   **Intrusion Detection Systems (IDS)**: While **Doss (Deakin)** and **Shahrestani (Newcastle)** offer extensive IDS evaluations, these studies frequently rely on simulation-based datasets (e.g., NSL-KDD) rather than real-world, distributed laboratory validation.

### 3.2 The Identified Research Gap
The primary deficit in existing literature is the **Assumption of Effectiveness**. Most studies assume that once a security control is architected, it functions at peak efficiency. Missing from the current body of work are:
1.  **Empirical Detection Latency (MTTD) Benchmarking**.
2.  **Real-world SIEM ingestion and correlation delay analysis**.
3.  **Reproducible methodologies for measuring "Architectural Resilience."**

### 3.3 ArchSentinelFlow: A Functional Intervention
ArchSentinelFlow extends the work of the aforementioned scholars by moving from **Static Validation** to **Measurable Performance**. By introducing a high-fidelity laboratory environment and utilizing live adversarial simulations, this research provides the "Industrial Receipt" required to validate Secure-by-Design theory.

