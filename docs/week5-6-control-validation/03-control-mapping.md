# 🛡️ Control Mapping

## 5.11 Control Under Validation

The primary control validated in Week 5 is:

**SSH Authentication Monitoring**

Mapped to:

- NIST SI-4 (System Monitoring)
- NIST AU-6 (Audit Review, Analysis, and Reporting)

---

## 5.12 Technical Control Components

| Component | Function |
|------------|------------|
| SSH daemon | Generates authentication logs |
| /var/log/auth.log | Log source |
| Wazuh Agent | Log collection |
| Wazuh Manager | Rule evaluation |
| Wazuh Indexer | Alert storage |
| Wazuh Dashboard | Alert visualisation |

---

## 5.13 Detection Logic

Repeated failed login attempts generate log entries within:
- /var/log/auth.log

# Wazuh decoders parse SSH events.

# Detection rules trigger based on:

- Failed authentication attempts
- Frequency threshold
- Source IP correlation
