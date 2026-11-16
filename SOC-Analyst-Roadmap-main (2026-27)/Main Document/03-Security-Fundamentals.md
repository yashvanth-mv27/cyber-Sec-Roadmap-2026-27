# <span style="color:#00C2FF">03. Security Fundamentals</span>

> Core security concepts, identity, controls, and risk management needed for SOC operations and security architecture.

## <span style="color:#32D74B">Overview</span>

Security fundamentals help define what needs to be protected, how trust is established, and what controls reduce risk. These concepts form the foundation of every detection, design decision, and response workflow.

---

## <span style="color:#FFB000">Core Principles</span>

### CIA Triad
- Confidentiality: keep data accessible only to authorized users
- Integrity: prevent unauthorized modification
- Availability: ensure services continue to function appropriately

### Defense in Depth
Use multiple layers of defense so a single failure does not compromise the system.

### Zero Trust
Never trust a network or user by default; verify identity and access continuously.

### Non-Repudiation
Evidence that an action occurred and cannot be denied by the actor.

---

## <span style="color:#FF5F57">Identity and Access</span>

### Authentication
The process of proving identity.

Examples:
- Passwords
- MFA
- Certificates
- Biometrics
- Device-based identity

### Authorization
The process of determining what an authenticated identity can do.

### Accounting
Logging and tracking what actions occurred, who performed them, and from where.

### Identity Management
Govern user lifecycle, roles, approvals, access review, and identity governance.

---

## <span style="color:#7C3AED">Security Controls</span>

### Administrative controls
Policies, procedures, training, governance, and risk decisions.

### Technical controls
Firewalls, AV, EDR, IAM, encryption, endpoint controls, SIEM.

### Physical controls
Locks, access badges, CCTV, environmental safeguards, secure facilities.

---

## <span style="color:#00D4AA">Risk Management</span>

Risk is the combination of:
- Threat
- Vulnerability
- Impact
- Likelihood

### Risk process
- Identify assets and threats
- Assess vulnerabilities
- Estimate impact and likelihood
- Prioritize mitigation controls
- Monitor residual risk

### SOC role
Analysts help measure risk through detection coverage, telemetry gaps, incident frequency, exposure, and operational impact.

---

## <span style="color:#FFB000">Vulnerability Management</span>

- Asset inventory
- Vulnerability discovery
- Scoring and prioritization
- Patch and remediation planning
- Validation and exception handling

### Common sources
- Vulnerability scanners
- EDR or threat intelligence feeds
- Infrastructure compliance checks
- Third-party dependencies

---

## <span style="color:#32D74B">Patch Management</span>

Patch management ensures systems are updated to reduce exploit risk.

### Best practices
- Prioritize critical and internet-facing assets
- Test patches in staging environments
- Validate rollback procedures
- Monitor for regressions

### SOC impact
Unsupported or unpatched systems increase exploitability and detection noise.

---

## <span style="color:#FF5F57">Cryptography</span>

### Hashing
Creates a fixed-size fingerprint of data.

Examples:
- SHA-256
- SHA-1 (legacy)
- MD5 (legacy, insecure)

### Encryption
Protects confidentiality and integrity.

Examples:
- Symmetric encryption
- Asymmetric encryption
- TLS
- VPN encryption

### PKI
Public Key Infrastructure manages digital certificates and trust chains.

### Digital Certificates
Used for code signing, TLS, machine identity, and secure communications.

---

## <span style="color:#7C3AED">Key Security Topics</span>

- IAM and least privilege
- Segmentation and lateral movement prevention
- Secure administration and MFA
- Data classification and handling
- Secure SDLC
- Security awareness and governance

---

## <span style="color:#00C2FF">Detection and Operational Relevance</span>

Security fundamentals guide detection engineering:

- What should be monitored?
- Which identity actions are suspicious?
- What data must be protected?
- Which controls are expected to be present?
- How should risk be measured and communicated?

---

## <span style="color:#FFB000">Interview Questions</span>

- Explain the CIA triad with examples.
- What is the difference between authentication and authorization?
- Why is defense in depth important?
- How does zero trust change architecture design?
- Why are digital certificates important in enterprise security?

---

## <span style="color:#00D4AA">Conclusion</span>

Security fundamentals are the language of defense. SOC analysts, engineers, and architects rely on these principles to design controls, investigate incidents, and communicate risk clearly.
