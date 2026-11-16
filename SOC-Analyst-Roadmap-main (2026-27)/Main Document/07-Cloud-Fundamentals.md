# <span style="color:#00C2FF">07. Cloud Fundamentals</span>

> Core cloud architecture, IAM, logging, workloads, and cloud attack paths.

## <span style="color:#32D74B">Overview</span>

Modern SOCs operate in hybrid and multi-cloud environments. Cloud fundamentals explain how services are deployed, how identity is granted, and how defenders monitor workloads and access patterns.

---

## <span style="color:#FFB000">Cloud Concepts</span>

### IaaS
Infrastructure as a Service, such as compute, storage, and networking.

### PaaS
Platform as a Service for managed app infrastructure.

### SaaS
Software delivered as a service with platform managed by the provider.

### Regions and Availability Zones
Compute and service placement influence resilience and latency.

### Identity and access
Cloud access is governed by IAM, roles, policies, and permissions boundaries.

### Shared responsibility model
The provider secures the platform; the customer secures the workloads, data, and configurations.

---

## <span style="color:#FF5F57">Core Cloud Security Components</span>

- IAM / RBAC / resource policies
- VPC / subnet architecture
- Security groups and network ACLs
- Cloud firewall and WAF controls
- SIEM and log ingestion
- Secrets and key management
- Data encryption and key rotation
- Workload protection and patching

---

## <span style="color:#7C3AED">AWS, Azure, and GCP</span>

### AWS
- IAM roles and policies
- EC2, S3, Lambda
- CloudTrail, GuardDuty, Config

### Azure
- Entra ID, Azure RBAC
- VMs, App Services, AKS
- Azure Monitor, Defender for Cloud

### GCP
- IAM and service accounts
- Compute Engine, Kubernetes Engine
- Cloud Audit Logs and Security Command Center

---

## <span style="color:#00D4AA">Cloud Logging and Monitoring</span>

Essential signals:
- API activity
- Console logins
- Policy changes
- Resource provisioning
- Identity changes
- Privilege escalation events
- Suspicious outbound traffic

### SOC value
Cloud telemetry is required to detect lateral movement, abuse of admin roles, and compromised workloads.

---

## <span style="color:#FFB000">Common Cloud Attacks</span>

- IAM privilege escalation
- Publicly exposed storage or services
- Token theft and replay
- Misconfigured security groups
- Malicious container deployment
- Serverless abuse
- Secret exfiltration
- Abuse of service principals or managed identities

---

## <span style="color:#32D74B">Cloud Hardening</span>

- Enforce least privilege
- Require MFA for privileged accounts
- Rotate secrets regularly
- Enable centralized logging
- Use network segmentation
- Keep images and runtimes patched
- Monitor for disabled controls or drift

---

## <span style="color:#FF5F57">Cloud SOC Use Cases</span>

- Detect a new admin role assignment
- Investigate a workstation connecting to unknown cloud resources
- Review outbound traffic from an EC2 instance to a suspicious domain
- Hunt for suspicious API calls from a service principal
- Validate access to high-value storage buckets

---

## <span style="color:#7C3AED">Interview Questions</span>

- What is the shared responsibility model?
- Why are IAM permissions and role design critical?
- What is the difference between security groups and NACLs?
- Why do cloud environments require centralized logging?
- What signals indicate a cloud privilege escalation?

---

## <span style="color:#00C2FF">Conclusion</span>

Cloud environments are dynamic, scalable, and identity-centric. SOC teams need strong cloud fundamentals to secure workloads, detect attacker misuse, and design resilient multi-cloud defenses.
