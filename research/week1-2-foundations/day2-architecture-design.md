# Lab 01 – Week 1, Day 2: Secure Architecture Design and Trust Boundary Definition

**Author:** Charles Owajoba  
**Research Domains:** Secure Systems, Cloud Security, Distributed Systems

---

## **Objective**

The objective of Day 2 is to design a **secure distributed cloud architecture** that operationalises the research framing established in Day 1.

This phase focuses on translating abstract security principles—such as **zero trust, least privilege, and defense in depth**—into **explicit architectural components, trust boundaries, and identity enforcement points** within a cloud-native system.

---

## **Architecture Overview**

The proposed system follows a **layered, zone-based architecture** that separates components by trust level and security responsibility. Each layer enforces security controls appropriate to its exposure and function.

The architecture is designed to:

- Minimise the attack surface  
- Prevent unauthorised lateral movement  
- Centralise identity and access enforcement  
- Support observability and auditability  

---

## **Architecture Components**

The architecture consists of the following core components:

1. **External Users**  
   Untrusted external clients that initiate requests to the system over the public internet.

2. **API Gateway (Azure API Management)**  
   Acts as the primary ingress point. Enforces authentication, request validation, and rate limiting before forwarding traffic to internal services.

3. **Web Tier (Stateless Frontend Services)**  
   Handles request routing and presentation logic. Designed to be stateless and horizontally scalable.

4. **Application Tier (Private Internal Services)**  
   Hosts core business logic and internal service communication. Access restricted to authorised upstream services.

5. **Data Tier (Private Databases and Storage)**  
   Stores persistent and sensitive data. Direct access from public or web-facing components is explicitly prohibited.

6. **Identity and Access Management (Azure AD)**  
   Central identity provider enforcing authentication, authorisation, and RBAC across all tiers.

7. **Observability Layer (Log Analytics and Microsoft Sentinel)**  
   Aggregates logs and security telemetry from all components for detection, auditing, and incident response.

---

## **Trust Boundary Definition**

Trust boundaries define points where the assumed trust level changes and **additional security controls** must be applied.

| Trust Boundary | Description | Enforced Security Controls |
|----------------|------------|----------------------------|
| TB1: Internet → API Gateway | Public ingress | Authentication, rate limiting, TLS |
| TB2: API Gateway → Web Tier | Controlled internal access | Token validation, TLS |
| TB3: Web Tier → Application Tier | Application logic boundary | Role-based access control, TLS |
| TB4: Application Tier → Data Tier | Data access boundary | RBAC, encryption at rest and in transit |

> Each trust boundary is explicitly enforced using **identity-driven controls**, not implicit network trust.

---

## **Architecture Diagram**

The secure distributed cloud architecture, including **trust boundaries** and **IAM enforcement points**, is illustrated in **Figure 1** below:

![Figure 1: Secure Distributed Cloud Architecture with Trust Boundaries](../../diagrams/week1-architecture-v1.1.png)

---

## **Identity and Access Enforcement**

- Identity is the **primary security perimeter**.  
- Azure AD issues tokens to authenticated entities.  
- Services assume **narrowly scoped identities**.  
- Role assignments are aligned with **functional responsibilities**.  
- No tier has **default access** to downstream components.  

> This approach aligns with **zero-trust models** and reduces the blast radius of compromised services.

---

## **Security Design Rationale**

The architecture enforces security through a combination of:

- Explicit trust boundary segmentation  
- Identity-based access control at each layer  
- Encryption of all inter-service communication  
- Centralised observability and audit logging  

> By combining architectural controls with IAM and monitoring, the system resists **common cloud attack patterns** such as credential abuse, lateral movement, and privilege escalation.

---

## **Alignment with Research Framing (Day 1)**

This architecture dire
