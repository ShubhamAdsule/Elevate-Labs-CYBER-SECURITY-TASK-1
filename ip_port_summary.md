 IP and Port Summary

 🔍 Subnet Scanned:
`192.168.214.0/24`

---

** 📡 Active Hosts and Open Ports:
**
| IP Address         | Open Ports | Services Detected | MAC Address            | Notes                              |
|--------------------|------------|--------------------|------------------------|-------------------------------------|
| 192.168.214.2      | 53         | DNS (domain)       | 00:50:56:F4:27:77      | Likely a DNS resolver (VMware VM)   |
| 192.168.214.140    | None       | N/A                | 00:0c:29:75:df:32 (you)| Host is up, but no open ports       |
| 192.168.214.254    | None       | N/A                | 00:50:56:ED:A2:81      | Host responded, but all ports filtered|

---

 🔐 Observations & Risks:

- **Port 53 (DNS)** is open on `192.168.214.2`. This suggests it's likely a DNS server or service running on a virtual machine. If improperly secured, DNS can be vulnerable to spoofing or amplification attacks.
- `192.168.214.140` (your system): All ports closed — this is good from a defense standpoint.
- `192.168.214.254`: All ports filtered (no response) — could be a router, firewall, or hardened system blocking scans.

---

 💡 Conclusion:

The scan helped identify active systems on the network and showed that only one host had an open port (DNS). Minimal exposure is a good sign, but further analysis would be needed if these were production systems. This task improved my understanding of how attackers and defenders use port scanning techniques to assess network security posture.
