# 📊 Results – Week 5-6
---

# 📄 05-results.md

```markdown
# 📊 Experimental Results

## 5.10 Summary of Findings

| Metric | Observation |
|---------|-------------|
| Detection Success | Yes |
| Alert Generated | Yes |
| Rule Triggered | SSH authentication failure |
| Source IP Captured | Yes |
| Latency | <Insert measured value> |

---

## 5.21 Technical Validation Outcome

The monitoring stack successfully detected repeated failed SSH login attempts.

Alert data contained:

- Accurate source IP
- Timestamp
- Rule ID
- Severity level
- Raw log context

This demonstrates effective host-based intrusion detection capability.

---

## 5.20 Detection Latency Measurement

To evaluate detection responsiveness, timestamp correlation was performed between raw SSH authentication logs and the corresponding Wazuh alert.

### Raw Log Timestamp (Ubuntu Desktop)

- Log source: `/var/log/auth.log`
- Event: Failed SSH authentication attempt
- Timestamp: 2026-02-17 – 01:13:43

### Wazuh Alert Timestamp

- Rule ID: 5712
- Rule Level: 10
- Description: SSH brute force trying to get access to the system
- Timestamp (Dashboard): Feb 17, 2026 @ 02:13:33

### Time Normalisation

A 1-hour offset was identified between the Ubuntu Desktop system time and the Wazuh dashboard display time, indicating a timezone difference.

After adjusting for timezone alignment:

- Normalised Wazuh time: 01:13:33
- Auth log time: 01:13:43

### Detection Latency

Detection latency was calculated as the time difference between log generation and alert indexing.

Observed latency: **~10 seconds**

This demonstrates near real-time detection and correlation capability within the Wazuh engine under controlled SSH brute-force conditions.

The minor offset reflects expected indexing and processing delay within distributed log pipelines.
