# Final Project Summary – System Misconfiguration Analysis & Mitigation

**Course**: LIS 5775 – Cybersecurity Fundamentals  
**Team Members**: Andrea Colon-De Feria, Michael Dunne, Jonah McKitty, James Flannery, R.J. Johns, Frank Quintana  
**Florida State University**

---

## 🎯 Project Overview

**Objective:** Demonstrate how organizations can effectively identify system misconfigurations and vulnerabilities in virtualized cloud environments and proactively address them before exploitation.

**Research Question:** How can organizations implement a repeatable and manageable framework for proactive threat management to drastically reduce the likelihood of cyber-attacks?

**Environment:** Flat network cloud environment consisting of pfsense firewall/router, Hyper-V, Linux, Windows, and Palo Alto virtual machines/appliances.

---

## 🔍 Key Vulnerabilities Identified

### Access Control Weaknesses
- **Shared credentials** across all team virtual machines
- **Default passwords** on administrative interfaces (pfsense firewall)
- **Weak password policies**: Zero minimum length, no complexity requirements
- **No account lockout** policies configured
- **Excessive privileges** with same credentials used across different system types

### Network Misconfigurations
- **Flat network topology** enabling easy lateral movement
- **No network segmentation** or VLANs implemented
- **Administrative interfaces** accessible from any network location
- **Unrestricted RDP and SSH** access from any location
- **No firewall rules** preventing inter-machine communication

### Insecure Communications
- **Clear-text protocols** in use (HTTP, Telnet, FTP, SNMP v2)
- **Unencrypted VOIP traffic** (SIP) revealing call contents
- **SMTP traffic** transmitting email data in clear text
- **Personal/financial information** transmitted over HTTP

### Patch Management Issues
- **End-of-life operating systems**: Windows Server 2012/R2 (EOL 2023), FreeBSD 11.2 (EOL 2019)
- **Outdated firewall firmware**: Palo Alto PAN-OS 9.1.9 (EOL March 2024) with 33 published vulnerabilities
- **Missing security updates** due to unsupported software versions

### Logging & Monitoring Gaps
- **No audit logging** enabled on Windows machines
- **Local-only logging** on Linux and Palo Alto systems
- **No centralized log aggregation** or monitoring
- **Limited intrusion detection** capabilities

---

## 🛠️ Tools & Methodologies Used

### Open-Source Security Tools
- **Zenmap (Nmap)** - Network reconnaissance and port scanning
- **Wireshark** - Packet capture and traffic analysis
- **Metasploit** - Vulnerability identification and exploitation testing
- **John the Ripper** - Password strength assessment and cracking
- **Kali Linux Social Engineering Toolkit** - Email spoofing demonstrations
- **Security Onion** - Network-based intrusion detection (OSSEC, Suricata)

### Analysis Techniques
- **Network topology mapping** and vulnerability assessment
- **Protocol analysis** of insecure communications (HTTP, Telnet, FTP, SNMP, SIP, SMTP)
- **Credential extraction** from network traffic
- **Social engineering attack simulation**
- **Intrusion detection log analysis**

---

## 📊 Critical Findings

### Exploitable Vulnerabilities Demonstrated
1. **Default Credentials**: Gained unauthorized firewall access using factory defaults
2. **Clear-text Authentication**: Captured usernames/passwords via Wireshark packet analysis
3. **Weak Passwords**: Cracked MD5 hashes in under 60 seconds using John the Ripper
4. **Data Exposure**: Intercepted personal information, billing details, and VOIP call contents
5. **Lateral Movement**: Used compromised telnet credentials to access Windows systems
6. **Email Intelligence**: Extracted sender/recipient information for social engineering attacks

### Network Security Impact
- **100% visibility** into network topology from single scan
- **Multiple attack vectors** available due to flat network design
- **Cross-platform credential reuse** enabling privilege escalation
- **Sensitive data leakage** through unencrypted protocols
- **Zero logging** on critical Windows infrastructure

---

## 🛡️ Recommended Mitigations

### Network Segmentation
- Implement **VLANs** with proper Access Control Lists (ACLs)
- Deploy **zero-trust network model** with default-deny policies
- Restrict **administrative interface access** to trusted network ranges
- Enable **network-based firewalls** on all virtual machines

### Access Control Hardening
- Enforce **strong password policies** (minimum length, complexity, expiration)
- Implement **unique credentials** per system and administrator
- Enable **account lockout** mechanisms after failed attempts
- Deploy **multi-factor authentication** for privileged accounts
- Apply **principle of least privilege** across all systems

### Secure Communications
- Replace **insecure protocols** (HTTP→HTTPS, Telnet→SSH, FTP→SFTP/FTPS)
- Implement **SNMP v3** with encryption and authentication
- Enable **TLS encryption** for VOIP (SIP over TLS)
- Configure **encrypted email** transmission (SMTPS/STARTTLS)

### System Lifecycle Management
- Develop **patch management** procedures with regular update cycles
- Plan **operating system upgrades** before end-of-support dates
- Implement **vulnerability scanning** with automated remediation workflows
- Establish **configuration baselines** using industry standards (NIST, CIS)

### Monitoring & Detection
- Deploy **centralized logging** with SIEM capabilities
- Enable **audit logging** on all Windows systems
- Implement **network-based intrusion detection** systems
- Configure **real-time alerting** for suspicious activities

---

## 🎓 Learning Outcomes

### Technical Skills Demonstrated
- **Vulnerability assessment** using industry-standard tools
- **Network traffic analysis** and packet inspection techniques
- **Penetration testing** methodologies and attack simulation
- **Social engineering** awareness and prevention strategies
- **Security tool integration** in enterprise environments

### Cybersecurity Frameworks Applied
- **NIST Risk Management Framework** for vulnerability prioritization
- **Defense-in-depth strategy** implementation
- **Zero-trust security model** principles
- **Industry security benchmarks** and hardening guidelines

---

## 💡 Key Insights

**Human Factor**: 77% of misconfigurations are due to lack of knowledge and experience, emphasizing the need for training and automation.

**Cost-Effective Security**: Open-source tools can provide equivalent functionality to expensive commercial solutions for small-to-medium enterprises.

**Proactive vs. Reactive**: Organizations that implement proactive vulnerability management significantly reduce cyber-attack likelihood and impact.

**Layered Security**: No single security control is sufficient; multiple overlapping defenses are essential for comprehensive protection.

**Continuous Monitoring**: Security is not a one-time implementation but requires ongoing assessment, monitoring, and improvement.

---

## 🏁 Conclusion

This comprehensive analysis demonstrated that system misconfigurations pose significant risks to organizational security, but these vulnerabilities can be effectively identified and mitigated using readily available tools and established frameworks. The project highlighted the critical importance of proactive security measures, proper configuration management, and continuous monitoring in protecting against increasingly sophisticated cyber threats.

**Impact**: By implementing the recommended security controls and leveraging both commercial and open-source tools, organizations can dramatically reduce their attack surface and improve their overall security posture in today's complex threat landscape.

---

**Research Environment**: SECNET Cloud Infrastructure (Flat network with pfsense firewall/router, Hyper-V, Linux, Windows, and Palo Alto VMs)  
**Project Duration**: Academic Semester Spring 2024  
**Methodology**: Vulnerability assessment and security analysis using open-source tools in authorized academic lab environment
