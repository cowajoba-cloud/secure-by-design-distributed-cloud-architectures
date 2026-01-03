# Lab 01 – Week 1, Day 1  
## Research Framing: Secure Distributed Cloud Systems

**Author:** Charles Owajoba  
**Focus:** Cloud Security • Secure Systems • DevSecOps  

---

## Problem Statement

Security incidents in cloud and distributed systems are commonly caused by
misconfigurations, excessive privileges, and unclear trust boundaries rather
than advanced exploits.

As systems scale and become more distributed, implicit trust assumptions and
weak identity controls significantly increase the risk of lateral movement and
privilege escalation.

---

## Research Motivation

This lab explores how secure-by-design architectural decisions can reduce
systemic security risk in distributed cloud environments.

The goal is to bridge the gap between:
- academic secure systems theory, and
- practical cloud security implementation.

The work draws on cloud IAM, zero-trust principles, and observability to design
architectures that are enforceable, auditable, and resilient.

---

## Hypothesis

A segmented cloud architecture with explicit trust boundaries and least-privilege
identity controls will significantly reduce attack surface and lateral movement
opportunities.

---

## Security Assumptions

- Cloud provider infrastructure is trusted but not infallible
- Internal services are not implicitly trusted (zero-trust assumption)
- IAM misconfiguration is a primary attack vector
- Logs and telemetry are available for analysis

---

## Practical Research Mapping

| Research Concept | Practical Implementation |
|-----------------|--------------------------|
| Trust boundaries | Network zones, IAM enforcement |
| Least privilege | RBAC, scoped service identities |
| Identity as perimeter | Centralised IAM |
| Observability | Centralised logging and SIEM |

---

## Outcome

This research framing establishes the foundation for architecture design and
threat modelling in subsequent lab stages.
