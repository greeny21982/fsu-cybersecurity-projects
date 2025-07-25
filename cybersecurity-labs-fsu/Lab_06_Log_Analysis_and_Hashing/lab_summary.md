# Lab 6 Summary – Log Analysis and Hashing

**Course**: LIS 5775 – Cybersecurity Fundamentals  
**Student**: Jonah McKitty

---

## 🖥️ Part 1: macOS Log Analysis

### Tools Used:
- **macOS Terminal**
- **Console.app**

### Key Activities:
- Used Terminal to interact with `.dmg` files and system logs.
- Explored Console.app to search and filter system logs.
- Identified errors, faults, and system events related to application usage.

### Key Takeaways:
- macOS logs provide detailed insight into system and application behavior.
- Logs can track failed login attempts, application usage, and system events.
- Tools like Console.app allow filtering and exporting logs for analysis.

---

## 🔐 Part 2: NIST 800-171 & Security Baselines

### Reference:
- [NIST SP 800-171 Rev. 2](https://csrc.nist.gov/publications/detail/spurity controls for protecting Controlled Unclassified Information (CUI).
- Emphasizes access control, audit logging, incident response, and system integrity.
- macOS security baselines can be aligned with NIST standards using tools like GitHub’s `macos_security` repo.

---

## 🔢 Part 3: File Hashing & Integrity

### Key Activities:
- Discussed how to calculate hashes (e.g., MD5, SHA-256) for files.
- Explored how hashes can verify file integrity and detect tampering.

### Key Takeaways:
- Hashes are unique digital fingerprints for files.
- Comparing hashes before and after transfer ensures data integrity.
- Longer hashes (e.g., SHA-256) offer stronger protection against collisions.

---

## 🧠 Reflection Questions

- **Can logs track remote login attempts?**  
  Yes, logs can capture both local and remote login events.

- **Why track Microsoft Office usage?**  
  For auditing, productivity monitoring, or license compliance.

- **Can a hacker hide file changes?**  
  Yes, by modifying logs or using fileless malware techniques.

---

## 🧾 Conclusion

This lab emphasized the importance of system logging, secure configuration baselines, and file integrity verification. It highlighted how logs and hashes are essential tools for monitoring, auditing, and defending modern systems.

