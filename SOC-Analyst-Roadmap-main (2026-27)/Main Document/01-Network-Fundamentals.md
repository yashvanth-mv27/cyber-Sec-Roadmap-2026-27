# <span style="color:#00C2FF">01. Network Fundamentals</span>

> Enterprise networking foundation for SOC analysts, security engineers, and blue team professionals.

## <span style="color:#32D74B">Overview</span>

Networking is the backbone of enterprise security. Every alert, packet capture, log source, and access flow ultimately depends on network fundamentals. Security teams need to understand traffic flow, segmentation, identity boundaries, and protocol behavior to detect and respond to incidents accurately.

## <span style="color:#FFB000">1. Introduction to Networking</span>

### Definition
A network is a collection of connected devices that exchange information using standardized communication protocols.

### Architecture
- Endpoints: computers, servers, mobile devices
- Access layer: switches, wireless access points
- Distribution/core: routers and high-speed aggregation
- Security layer: firewalls, proxies, IDS/IPS, WAF

### How it works
Devices use IP addresses, MAC addresses, ports, and protocols to transmit data across LANs and WANs.

### Use cases
- Internal office connectivity
- Remote access
- Cloud communication
- Data center segmentation

### Real examples
- Corporate LAN with VLAN segmentation
- VPN access for remote users
- Web traffic to SaaS over HTTPS

### Troubleshooting
- Check physical link status
- Validate IP configuration
- Review ARP tables
- Confirm firewall rules
- Trace route and packet capture

### Interview questions
- What is the difference between TCP and UDP?
- How does a router decide where to forward traffic?
- Why is segmentation important in SOC design?

### SOC relevance
Network visibility is required for log correlation, lateral movement detection, traffic anomalies, and incident response.

---

## <span style="color:#FF5F57">2. How Networks Work</span>

### Key concepts
- IP addressing
- MAC addressing
- Ports and services
- Segmentation and routing
- Protocol negotiation

### Security relevance
Attackers abuse protocol trust and default routing assumptions. SOC teams must understand normal behavior to spot unusual connection patterns.

---

## <span style="color:#7C3AED">3. OSI Model</span>

| Layer | Name | Example |
|---|---|---|
| 7 | Application | HTTP, DNS, SMTP |
| 6 | Presentation | Encoding, TLS |
| 5 | Session | Session control |
| 4 | Transport | TCP, UDP |
| 3 | Network | IP, routing |
| 2 | Data Link | Ethernet, ARP |
| 1 | Physical | Cables, fiber, Wi-Fi |

### SOC use
Understanding layer behavior helps in packet analysis, incident correlation, malware traffic detection, and protocol abuse investigation.

---

## <span style="color:#00D4AA">4. TCP/IP Model</span>

- Application layer
- Transport layer
- Internet layer
- Link layer

### Core protocols
- TCP: reliable, connection-oriented
- UDP: low latency, connectionless
- IP: addressing and routing
- ICMP: diagnostics and echo

---

## <span style="color:#FFB000">5. Encapsulation</span>

At each networking layer, headers are added to payload data. This allows computers to communicate across multiple network technologies.

### Example
- Application data
- TCP header
- IP header
- Ethernet frame

### Security impact
Attackers use fragmentation, tunneling, and protocol abuse to evade detections. SOC teams investigate packet anomalies, malformed headers, and uncommon ports.

---

## <span style="color:#32D74B">6. Routing and Switching</span>

### Routing
Routers determine the best path for packets based on routing tables and control protocols.

### Switching
Switches forward traffic within a LAN using MAC address tables.

### Threat examples
- Blackhole routing
- ARP poisoning
- VLAN hopping
- BGP hijacking

---

## <span style="color:#FF5F57">7. ARP, DNS, DHCP, NAT, PAT</span>

### ARP
Maps IP address to MAC address.

### DNS
Resolves names to IP addresses.

### DHCP
Assigns IP addressing dynamically.

### NAT
Translates private addresses to public addresses.

### PAT
Maps multiple internal IPs to one public IP using ports.

### SOC relevance
DNS tunneling, rogue DHCP servers, ARP spoofing, and NAT behavior can reveal malicious communication.

---

## <span style="color:#7C3AED">8. VLAN, VPN, and Secure Connectivity</span>

### VLAN
Logical segmentation of networks without physical isolation.

### VPN
Secure tunnel for remote access or site-to-site communication.

### VPN security
- IPsec or TLS
- MFA
- Split tunneling controls
- Device posture checks

---

## <span style="color:#00C2FF">9. Application and Service Protocols</span>

### HTTP / HTTPS
Web communication over port 80/443.

### SMTP / POP3 / IMAP
Email protocols.

### FTP / SFTP / SSH
File transfer and remote administrative access.

### SNMP / ICMP / NTP / LDAP / RDP
Network monitoring, diagnostics, timing, identity queries, and remote desktop.

### SOC notes
- Unencrypted FTP is risky
- SMB and RDP are common lateral movement paths
- LDAP abuse is relevant for identity attacks

---

## <span style="color:#FFB000">10. Network Devices</span>

| Device | Role | Security Significance |
|---|---|---|
| Hub | Broadcast domain | Weak security |
| Bridge | Segment network | Limited modern use |
| Switch | LAN forwarding | VLAN and port security |
| Router | Inter-network routing | Path integrity and ACLs |
| Firewall | Policy enforcement | Core security control |
| NGFW | App-aware filtering | Threat detection and policy |
| Load Balancer | Scalability | L7 traffic distribution |
| Proxy | Traffic mediation | Content filtering |
| Reverse Proxy | Front-end service access | Security and TLS termination |
| IDS | Detects suspicious traffic | Monitoring |
| IPS | Blocks malicious traffic | Enforcement |
| WAF | App-layer protection | OWASP coverage |
| TAP | Passive monitoring | Network forensics |

---

## <span style="color:#32D74B">11. Network Security Concepts</span>

- Zero Trust networking
- Segmentation and micro-segmentation
- Firewall rules and ACLs
- NAC
- Secure DNS
- VPN security

### Example
A finance VLAN may allow only specific ports to domain controllers and payment services; all other east-west traffic is denied.

---

## <span style="color:#FF5F57">12. Network Attacks</span>

- DDoS / DoS
- DNS poisoning
- ARP spoofing
- MITM
- Packet injection
- DNS tunneling
- Smurf attack
- Ping flood
- SYN flood
- UDP flood

### Detection behaviors
- Sudden traffic spike from many IPs
- Abnormal DNS resolution patterns
- Multiple ARP replies from a host
- Unexpected TLS or ICMP bursts

---

## <span style="color:#7C3AED">SOC Detection Examples</span>

- Large outbound DNS query volume to odd domains
- Multiple failed connections to internal services
- Server receiving SYN floods
- Internal host sending encrypted traffic to unknown external IPs

---

## <span style="color:#00D4AA">Interview Questions</span>

- Explain the difference between a switch and a router.
- What is the purpose of NAT and PAT?
- How does a firewall enforce policy?
- Why does DNS monitoring matter for SOC investigations?
- What is micro-segmentation and why is it useful?

## <span style="color:#FFB000">Conclusion</span>

Network fundamentals are core to threat detection, investigation, and architecture design. A strong SOC analyst should be comfortable with routing, switching, segmentation, protocols, and common malicious traffic patterns.

---

### Quick study checklist
- [ ] OSI and TCP/IP models
- [ ] ARP, DNS, DHCP, NAT, PAT
- [ ] VLAN and secure remote access
- [ ] Firewalls, IDS/IPS, WAF, TAP
- [ ] DDoS and protocol-level attack patterns
