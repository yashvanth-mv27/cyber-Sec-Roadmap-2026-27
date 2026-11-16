# <span style="color:#00C2FF">05. Threats, Attacks, and TTPs</span>

> A practical overview of modern cyber threats and adversary behavior across endpoints, identities, networks, cloud, and AI systems.

## <span style="color:#32D74B">Overview</span>

Threats evolve quickly. Effective defenders need to understand malware categories, account attacks, network abuse, cloud misuse, supply chain risks, and new AI-related attack patterns.

---

## <span style="color:#FFB000">Malware Family Overview</span>

### Virus
A malicious program attached to a file or process; often self-replicating within host boundaries.

### Worm
Self-propagating malware that spreads across systems automatically.

### Trojan
Disguised as legitimate software while performing malicious operations.

### Rootkit
Hides malicious activity inside operating system components or kernel mechanisms.

### Ransomware
Encrypts data and demands payment; often combined with exfiltration and extortion.

### Spyware
Collects user or system activity covertly.

### Adware
Displays unwanted ads and may degrade privacy or system performance.

---

## <span style="color:#FF5F57">Account Attacks</span>

### Password spraying
Attempts a small set of common passwords against many accounts.

### Credential stuffing
Uses leaked username-password pairs against multiple services.

### Brute force
Repeated guessing of credentials.

### Phishing
Mass deception to trick users into revealing data or enabling execution.

### Spear phishing
Targeted phishing attacks against a specific user, role, or organization.

### SOC relevance
Identity attacks often produce failed logon bursts, suspicious MFA pushes, impossible travel, and unusual admin activity.

---

## <span style="color:#7C3AED">Network Attacks</span>

- DDoS
- MITM
- DNS poisoning
- Packet injection
- LDAP abuse
- Port scanning
- Protocol tunneling
- VPN abuse

### Detection signals
- High volume of failed connection attempts
- New external destinations
- Unexpected internal connections
- DNS anomalies
- Decryption or tunneling patterns

---

## <span style="color:#00D4AA">Cloud Attacks</span>

- IAM privilege escalation
- Misconfigured storage buckets
- Token theft and replay
- API abuse
- Exploit of serverless functions
- Lateral movement between cloud resources

### SOC response
Review cloud audit logs, IAM changes, policy drift, suspicious API usage, and unusual resource creation.

---

## <span style="color:#FFB000">Supply Chain Attacks</span>

Attackers compromise a trusted supplier or dependency to reach multiple victims.

Common patterns:
- Compromised package repositories
- Tampered vendor software
- Malicious CI/CD pipelines
- Signed but malicious updates

---

## <span style="color:#32D74B">Identity Attacks</span>

- Pass-the-hash
- Pass-the-ticket
- Kerberoasting
- Golden ticket or silver ticket abuse
- MFA fatigue
- OAuth abuse
- Shadow admin creation

### Detection focus
Authentication logs, privileged group changes, unusual sign-in locations, impossible travel, and service ticket anomalies.

---

## <span style="color:#FF5F57">AI-Based Attacks</span>

### LLM abuse
Attackers exploit models for malicious content generation, malware assistance, or social engineering.

### Prompt injection
Hidden instructions manipulate AI system behavior or expose sensitive data.

### Deepfake attacks
Synthetic audio or video used to impersonate trusted users or executives.

### Model poisoning
Manipulating training data or model updates to influence outputs.

### Data leakage
Compromise of private prompts, training data, or secrets via model misuse.

---

## <span style="color:#7C3AED">Current and Emerging Threats</span>

- Ransomware-as-a-service
- Living-off-the-land attacks
- Adversary-in-the-middle phishing
- Data extortion campaigns
- Cloud-native attacker tradecraft
- AI-enabled social engineering
- Identity-based intrusion at scale

---

## <span style="color:#00C2FF">MITRE ATT&CK Mapping Examples</span>

| Threat | ATT&CK mapping |
|---|---|
| Phishing | Initial Access |
| PowerShell execution | Execution |
| Registry run key | Persistence |
| Token manipulation | Privilege Escalation |
| Process Hollowing | Defense Evasion |
| Kerberoasting | Credential Access |
| RDP to remote servers | Lateral Movement |
| Data staging and exfiltration | Collection/Exfiltration |
| Ransomware | Impact |

---

## <span style="color:#FFB000">Threat Hunting Opportunities</span>

- Investigate suspicious login bursts and MFA fatigue
- Hunt for abnormal PowerShell or script execution
- Check for changes to scheduled tasks and services
- Review cloud policy changes and external access configuration
- Look for unusual DNS and data transfer patterns

---

## <span style="color:#00D4AA">Interview Questions</span>

- What is the difference between phishing and spear phishing?
- Why is password spraying effective?
- What is a supply chain attack and why is it dangerous?
- How does ransomware differ from malware generally?
- Why is AI-based social engineering a growing concern?

---

## <span style="color:#00C2FF">Conclusion</span>

Threats now span identity, endpoint, network, cloud, and AI systems. SOC defenders need to think beyond malware alone and understand the attack chain, access patterns, and adversary tradecraft used across modern environments.
