# ⚙️ Environment Setup – Week 5-6: Control Validation

## Lab Environment

- **VMs:** Kali, Ubuntu Desktop, Ubuntu Server, Metasploit, OWASP VM  
- **Network:** Isolated lab network with defined subnets (e.g., 192.168.56.0/24)  
- **Tools Installed:**
  - Nessus / Qualys (vulnerability scanning)
  - Azure Sentinel / Splunk (log collection)
  - Wireshark / tcpdump (network analysis)
  - Python scripts for control validation automation
  - Secure SDLC testing tools (OWASP ZAP, Burp Suite basic scans)

---

## Steps to Set Up

1. Spin up all VMs.  
2. Configure static IPs and check network connectivity:
   ```bash
   # Example
   ping 192.168.56.30
