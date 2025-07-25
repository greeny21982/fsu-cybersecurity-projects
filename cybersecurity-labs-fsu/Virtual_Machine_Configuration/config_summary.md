# Virtual Machine Configuration Summary

**Course**: LIS 5775 – Cybersecurity Fundamentals  
**Student**: Jonah McKitty

---

## 🖥️ Overview

This document explores the evolution, configuration, and security of virtual machines (VMs), with a focus on best practices and guidance from the National Institute of Standards and Technology (NIST).

---

## 🧱 Part 1: Virtualization Background

### Key Concepts:
- Virtualization emerged in the 1990s with tools like VMware, enabling multiple operating systems to run on a single physical server.
- VMs optimize resource utilization and streamline IT infrastructure.
- Each VM operates independently with its own OS, applications, and configurations.

---

## 🔐 Part 2: Security Configuration & NIST Guidance

### Key Topics:
- **NIST 2016 Bulletin**: Emphasizes securing VMs at both host and network levels.
- **Critical Configurations**:
  - Network segmentation
  - Redundant network paths
  - Firewall enforcement
  - Traffic monitoring

### Key Takeaway:
- VMs supporting business-critical processes must be secured to the same standard as physical machines.

---

## 🔑 Part 3: Access Control

### Concepts Covered:
- Evolution from basic role-based access to modern frameworks.
- Principle of **least privilege**: Users should only have access necessary for their role.
- **Zero Trust Model**: No user or device is trusted by default; every access request is verified.

### NIST Recommendation (HY-SR-13):
- Access control should be granular, allowing permissions at both the VM and group level.
- Deny rules should override group-level permissions for sensitive workloads.

---

## 🔐 Part 4: Password Management & Authentication

### Best Practices:
- Enforce complex, frequently changed passwords.
- Use stronger authentication methods (e.g., PIV cards, MFA, Kerberos).
- Integrate user accounts with enterprise directory services for centralized control.

### NIST Recommendation (HY-SR-15):
- All user accounts on hypervisors should be tied to the organization’s directory infrastructure to enforce policies and streamline account management.

---

## 🧾 Conclusion

This configuration guide highlights the importance of securing virtualized environments through layered access control, strong authentication, and adherence to NIST standards. As virtualization continues to dominate enterprise infrastructure, these practices are essential for maintaining confidentiality, integrity, and availability.

