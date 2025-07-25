# Lab 5 Summary – Network Packet Analysis with Wireshark

**Course**: LIS 5775 – Cybersecurity Fundamentals  
**Student**: Jonah McKitty

---

## 🌐 Part 1: Packet Capture and Inspection

### Tool Used:
- **Wireshark**

### Key Activities:
- Captured and analyzed network traffic using Wireshark.
- Observed packet structure, including SYN, ACK, FIN, and GET flags.
- Interpreted hexadecimal packet contents and sequence numbers.
- Compared normal vs blocked ICMP traffic (e.g., ping requests).

### Key Takeaways:
- Data is broken into smaller packets for efficient transmission and error handling.
- TCP flags (SYN, ACK, FIN) are essential for connection setup and teardown.
- Sequence numbers ensure packets are reassembled correctly at the destination.
- ICMP blocking can prevent reconnaissance but may hinder diagnostics.

---

## 🔐 Part 2: Firewall Rules and Port Behavior

### Key Activities:
- Configured firewall rules to block or allow traffic on specific ports (e.g., 80 and 443).
- Observed behavior when accessing secure (HTTPS) vs unsecure (HTTP) websites.
- Disabled and re-enabled rules to test traffic filtering.

### Key Takeaways:
- Blocking Port 80 (HTTP) while allowing Port 443 (HTTPS) improves security by enforcing encrypted communication.
- Malware can disguise itself to bypass firewalls if rules are based on file names or superficial attributes.
- Packet filtering and rule ordering are critical to effective firewall configuration.

---

## 🧠 Reflection Questions

- **Why so many packets per click?**  
  A single web request can trigger dozens or hundreds of packets due to DNS, HTML, CSS, JS, and media content.

- **Can malware bypass firewalls?**  
  Yes, by mimicking trusted processes or exploiting weak rule configurations.

- **Why filter traffic in Wireshark?**  
  To isolate relevant data and simplify analysis of specific protocols or IPs.

---

## 🧾 Conclusion

This lab provided hands-on experience with packet-level network analysis and firewall behavior. It emphasized the importance of understanding traffic flow, protocol behavior, and the role of filtering in both diagnostics and defense.

