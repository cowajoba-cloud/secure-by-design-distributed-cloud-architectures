# 04 — Architecture Evaluation

## 1. Evaluation Objective

To assess whether the proposed architecture satisfies:

- Security observability requirements
- Threat modelling needs
- Control validation capability

---

## 2. Strengths

### 2.1 High Observability
Wazuh provides detailed logs across authentication, file changes, and system events.

### 2.2 Modular Design
Components can be independently modified or replaced.

### 2.3 Controlled Attack Simulation
The Kali node enables safe adversarial testing.

---

## 3. Limitations

- Single monitoring point (Wazuh Manager)
- No load balancer or redundancy
- No container orchestration layer
- Limited scalability testing

---

## 4. Risk Considerations

- Misconfiguration risk
- Log overload without tuning
- False positives during experiments

---

## 5. Evaluation Summary

The architecture is suitable for:

- Academic security validation
- Threat modelling exercises
- Experimental intrusion detection testing

It is not production-grade but research-grade.

This distinction is intentional.
