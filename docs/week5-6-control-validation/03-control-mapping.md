
---

### **03-control-mapping.md**

```markdown
# 🗺️ Control Mapping – Week 5-6

## STRIDE Threats → Security Controls

| STRIDE Category | Threat Description           | Implemented Control          | Control Validation Method |
|----------------|------------------------------|-----------------------------|--------------------------|
| S – Spoofing   | Unauthorized login attempts  | MFA, IAM policies           | Login simulation tests   |
| T – Tampering  | File modification            | File integrity monitoring   | Modify test files        |
| R – Repudiation| Log deletion attempts        | Centralized logging         | Attempt log deletion     |
| I – Info Disclosure | Sensitive data exposure | Encryption, ACLs            | Data access simulation   |
| D – DoS       | Service disruption           | Rate limiting, firewall     | Stress test VM           |
| E – Elevation | Privilege escalation         | Role-based access controls  | sudo escalation tests    |

---

### Notes

- Expand with **observed results** in the `results.md` file.  
- Link to any diagrams or notes as needed.
