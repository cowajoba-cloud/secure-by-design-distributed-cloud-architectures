Lab 01 – Week 1, Day 1
Research Framing: Secure Distributed Cloud Architectures

Author: Charles Owajoba
Research Domains: Secure Systems, Cloud Security, Distributed Systems, DevSecOps

1. Problem Statement

Security incidents in modern cloud and distributed systems are increasingly attributed to architectural weaknesses, including misconfigurations, excessive privileges, and poorly defined trust boundaries, rather than sophisticated zero-day exploits.

As systems become more distributed, identity-driven, and service-oriented, implicit trust assumptions and inadequate segmentation significantly increase the attack surface. These weaknesses enable adversaries to exploit configuration errors and perform lateral movement across system components, often with minimal resistance.

This research investigates how secure-by-design architectural principles, when applied at the system design stage, can mitigate these systemic risks in distributed cloud environments.

2. Research Motivation

The motivation for this research is to bridge the gap between theoretical secure systems design and practical cloud security implementation.

While academic literature provides robust models for trustworthy systems, real-world cloud deployments frequently prioritise functionality and scalability over principled security design. Conversely, industry security practices often focus on reactive controls rather than architectural correctness.

This work leverages cloud platforms, identity and access management (IAM), observability systems (SIEM), and DevSecOps principles to explore how architectural decisions influence security outcomes in distributed cloud systems.

The ultimate goal is to develop architectures that are not only secure in theory but operationally enforceable, auditable, and resilient in practice.

3. Research Hypothesis

A segmented distributed cloud architecture that incorporates:

Explicit trust boundaries

Least-privilege IAM policies

Identity-centric access control

Structured threat modelling

will significantly reduce lateral movement opportunities and mitigate the security risks arising from cloud misconfigurations and over-privileged services.

4. Security Assumptions

This research is conducted under the following assumptions:

The underlying cloud provider infrastructure is trusted but not infallible

Internal services are not implicitly trusted (Zero Trust assumption)

IAM misconfiguration represents a primary attack vector

Security telemetry and logs are available, reliable, and untampered

Adversaries seek to exploit architectural weaknesses rather than novel exploits

These assumptions reflect realistic threat environments observed in both academic studies and industry incident reports.

5. Practical Research Mapping

The research concepts explored in this study are mapped to concrete, implementable security controls as shown below:

Research Concept	Practical Control Implementation
Trust Boundaries	Network segmentation, zone isolation, IAM enforcement points
Least Privilege	RBAC, scoped service identities, role separation
Identity as Perimeter	Centralised IAM, token-based authentication
Observability	Centralised logging, SIEM integration, audit trails

This mapping ensures that theoretical constructs are continuously validated through practical implementation.

6. Research Scope and Methodology

This lab-based research adopts a design science methodology, combining architectural design, controlled experimentation, and iterative refinement.

Each lab output will:

Be reproducible and version-controlled

Produce artefacts suitable for academic publication

Align with industry security standards and practices

The research progresses incrementally, with each week building upon the architectural and security foundations established in earlier stages.

7. Notes and Research Continuity

This lab notebook forms the foundation for architecture design (Week 1–2)

All artefacts will be GitHub-hosted and publicly verifiable

Subsequent weeks will focus on:

Threat modelling (STRIDE)

Attack path analysis

Secure DevSecOps pipeline integration

Publishable research outputs