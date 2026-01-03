Lab 01 – Week 1, Day 2
Secure Architecture Design and Trust Boundary Definition

Author: Charles Owajoba
Research Domains: Secure Systems, Cloud Security, Distributed Systems

1. Objective

The objective of Day 2 is to design a secure distributed cloud architecture that operationalises the research framing established in Day 1.

This phase focuses on translating abstract security principles—such as zero trust, least privilege, and defence in depth—into explicit architectural components, trust boundaries, and identity enforcement points within a cloud-native system.

2. Architecture Overview

The proposed system follows a layered, zone-based architecture that separates components by trust level and security responsibility. Each layer enforces security controls appropriate to its exposure and function.

The architecture is designed to:

Minimise the attack surface

Prevent unauthorised lateral movement

Centralise identity and access enforcement

Support observability and auditability

3. Architecture Components

The architecture consists of the following core components:

3.1 External Users

Untrusted external clients that initiate requests to the system over the public internet.

3.2 API Gateway (Azure API Management)

Acts as the primary ingress point to the system. It enforces authentication, request validation, and rate limiting before forwarding traffic to internal services.

3.3 Web Tier (Stateless Frontend Services)

Handles request routing and presentation logic. This tier is designed to be stateless and horizontally scalable.

3.4 Application Tier (Private Internal Services)

Hosts core business logic and internal service communication. Access to this tier is restricted to authorised upstream services.

3.5 Data Tier (Private Databases and Storage)

Stores persistent and sensitive data. Direct access from public or web-facing components is explicitly prohibited.

3.6 Identity and Access Management (Azure AD)

Serves as the central identity provider, enforcing authentication, authorisation, and role-based access control (RBAC) across all tiers.

3.7 Observability Layer (Log Analytics and Microsoft Sentinel)

Aggregates logs and security telemetry from all components to support detection, auditing, and incident response.

4. Trust Boundary Definition

Trust boundaries define points where the assumed trust level changes and additional security controls must be applied.

Trust Boundary	Description	Enforced Security Controls
TB1: Internet → API Gateway	Public ingress	Authentication, rate limiting, TLS
TB2: API Gateway → Web Tier	Controlled internal access	Token validation, TLS
TB3: Web Tier → Application Tier	Application logic boundary	Role-based access control, TLS
TB4: Application Tier → Data Tier	Data access boundary	RBAC, encryption at rest and in transit

Each trust boundary is explicitly enforced using identity-driven controls rather than implicit network trust.

5. Architecture Diagram

The secure distributed cloud architecture, including trust boundaries and IAM enforcement points, is illustrated in Figure 1 bellow. 
![Figure 1: Secure Distributed Cloud Architecture with Trust Boundaries](../diagrams/secure-cloud-architecture-day2.png)

6. Identity and Access Enforcement

Identity is treated as the primary security perimeter in this architecture.

Azure AD issues tokens to authenticated entities

Services assume narrowly scoped identities

Role assignments are aligned with functional responsibilities

No tier has default access to downstream components

This approach aligns with zero-trust architecture models and reduces the blast radius of compromised services.

7. Security Design Rationale

The architecture enforces security through a combination of:

Explicit trust boundary segmentation

Identity-based access control at each layer

Encryption of all inter-service communication

Centralised observability and audit logging

By combining architectural controls with IAM and monitoring, the system resists common cloud attack patterns such as credential abuse, lateral movement, and privilege escalation.

8. Alignment with Research Framing (Day 1)

This architecture directly operationalises the Day 1 research hypotheses by:

Translating trust boundaries into enforceable controls

Demonstrating least-privilege principles in practice

Providing a platform for structured threat modelling

Enabling reproducible security experiments

9. Notes and Continuity

This architecture serves as the baseline for:

Threat modelling (Week 3)

Attack simulation

DevSecOps pipeline integration

All artefacts are version-controlled and reproducible

The design is intentionally cloud-agnostic at the conceptual level, despite using Azure services