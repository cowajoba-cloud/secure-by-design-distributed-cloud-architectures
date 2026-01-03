# Lab 01 – Week 1, Day 2  
## Secure Cloud Architecture and Trust Boundaries

**Author:** Charles Owajoba  
**Focus:** Cloud Security • Secure Systems  

---

## Objective

The objective of Day 2 is to translate the research framing from Day 1 into a
practical, secure cloud architecture with explicit trust boundaries and identity
enforcement points.

---

## Architecture Overview

The system is designed using a layered architecture that separates components
by trust level and security responsibility.

The architecture aims to:
- minimise attack surface,
- prevent lateral movement,
- enforce identity-based access control.

---

## Architecture Components

- **External Users** – Untrusted internet clients
- **API Gateway (Azure API Management)** – Secure ingress and request control
- **Web Tier** – Stateless frontend services
- **Application Tier** – Internal business logic services
- **Data Tier** – Private databases and storage
- **Azure AD** – Identity and access management
- **Log Analytics & Sentinel** – Centralised security monitoring

---

## Trust Boundaries

| Boundary | Description | Controls |
|--------|------------|----------|
| TB1 | Internet → API Gateway | Authentication, rate limiting |
| TB2 | API Gateway → Web Tier | Token validation, TLS |
| TB3 | Web Tier → App Tier | Role-based access, TLS |
| TB4 | App Tier → Data Tier | RBAC, encryption |

---

## Architecture Diagram

The architecture and trust boundaries are illustrated below.

![Secure Distributed Cloud Architecture](../../diagrams/secure-cloud-architecture-day2.png)

## Security Rationale 

Security is enforced through: 
- Explicit trust boundaries 
- Identity driven access control
- Encrypted service-to-service communication
- Centralized logging and monitoring. 

This approach alligns with zero-trust and secure-by-design principles. 

## Outcome

This architecture provides a concrete foundation for structured threat modeling and DevSecOps security integration in future labs. 