<div align="center">

# 🛡️ SOC ANALYST ROADMAP
### 2026–27 · From first alert to security architecture

**LEARN THE SIGNALS　·　INVESTIGATE WITH EVIDENCE　·　ENGINEER THE DEFENSE**

[![Roadmap](https://img.shields.io/badge/ROADMAP-2026%E2%80%9327-0B1020?style=for-the-badge&logo=github&logoColor=white)](#-roadmap-dashboard)
[![Foundation](https://img.shields.io/badge/01%E2%80%9310-FOUNDATION-0284C7?style=for-the-badge&logo=bookstack&logoColor=white)](#-blue-foundation--core-skills)
[![SOC](https://img.shields.io/badge/11%E2%80%9322-SOC%20ENGINEERING-15803D?style=for-the-badge&logo=shield&logoColor=white)](#-green-soc--engineering)
[![Advanced](https://img.shields.io/badge/23%E2%80%9338-ADVANCED%20DEFENSE-6D28D9?style=for-the-badge&logo=target&logoColor=white)](#-violet-advanced--architecture)

[🧭 Roadmap](#-complete-roadmap) · [🎓 Certifications](#-certification-pathways) · [🔭 Future skills](#-future-security-drivers) · [🧰 Tools](#-trusted-references--tools)

</div>

> [!IMPORTANT]
> **Authorized defensive learning only.** Use systems and data you own or have explicit permission to assess. Practice in isolated labs, use synthetic or public training data, and never publish credentials, secrets, or customer data.

---

## 📊 Roadmap dashboard

| Learning stages | Focus | Suggested evidence of progress |
|---|---|---|
| 🔹 **01–10 · Foundation** | Network, operating systems, security, cloud and SOC architecture basics | Notes, diagrams, foundational labs |
| 🟩 **11–22 · SOC practice** | Operations, SIEM/XDR, detection, DFIR, automation and career development | Case reports, tested detections, lab portfolio |
| 🟪 **23–38 · Advanced** | Platform engineering, AI, resilience, governance and leadership | Architecture decisions, threat models, project demos |

**Progression:** `FOUNDATIONS → SOC ANALYST → DETECTION ENGINEER → SECURITY ENGINEER → SECURITY ARCHITECT / LEADER`

```mermaid
flowchart LR
    A[🌐 Network & OS] --> B[🛡️ Security fundamentals]
    B --> C[🚨 SOC operations]
    C --> D[🔎 SIEM, XDR & detection]
    D --> E[🧭 DFIR & threat hunting]
    E --> F[☁️ Cloud, identity & platform]
    F --> G[⚙️ Automation & data engineering]
    G --> H[🤖 AI / LLM / agent security]
    H --> I[🏛️ Architecture & leadership]
```

> **Visual note:** This README uses a dark, cyber-inspired badge palette and text-first dashboard instead of external GIFs or large image embeds. GitHub controls the page theme; badge colors provide consistent visual cues in either theme. Markdown does not support dependable CSS animation, so section dividers are static for accessibility and reliable rendering.

## 🧭 Complete roadmap

Explore the 38 learning topics from the `SOC-Analyst-Roadmap-main (2026-27)` materials. Each link opens its guide. This README is a navigation and learning overview.

### 🔹 Blue · Foundation & core skills

| # | Learning track | Focus |
|---|---|---|
| 01 | 🌐 [Network Fundamentals](SOC-Analyst-Roadmap-main%20(2026-27)/01-Network-Fundamentals.md) | Protocols, routing, network visibility, segmentation |
| 02 | 💻 [Operating System Fundamentals](SOC-Analyst-Roadmap-main%20(2026-27)/02-Operating-System-Fundamentals.md) | Windows, Linux, macOS, processes, services, logs |
| 03 | 🛡️ [Security Fundamentals](SOC-Analyst-Roadmap-main%20(2026-27)/03-Security-Fundamentals.md) | Security principles, access control, cryptography, risk |
| 04 | 🧭 [Cyber Kill Chain and MITRE](SOC-Analyst-Roadmap-main%20(2026-27)/04-Cyber-Kill-Chain-and-MITRE.md) | Adversary behavior, ATT&CK, defensive use cases |
| 05 | 🚩 [Threats, Attacks, and TTPs](SOC-Analyst-Roadmap-main%20(2026-27)/05-Threats-Attacks-and-TTPs.md) | Threat patterns across endpoints, identity, cloud, supply chains |
| 06 | 🪪 [Active Directory Fundamentals](SOC-Analyst-Roadmap-main%20(2026-27)/06-Active-Directory-Fundamentals.md) | Directory services, authentication, defensive visibility |
| 07 | ☁️ [Cloud Fundamentals](SOC-Analyst-Roadmap-main%20(2026-27)/07-Cloud-Fundamentals.md) | AWS, Azure, GCP, cloud identity and logging |
| 08 | 🤖 [AI Security Fundamentals](SOC-Analyst-Roadmap-main%20(2026-27)/08-AI-Security-Fundamentals.md) | AI/ML concepts, risks, responsible security |
| 09 | ⚙️ [Automation and Orchestration](SOC-Analyst-Roadmap-main%20(2026-27)/09-Automation-and-Orchestration.md) | Playbooks, SOAR concepts, human-approved automation |
| 10 | 🏗️ [SOC Architecture Guide](SOC-Analyst-Roadmap-main%20(2026-27)/10-SOC-Architecture-Guide.md) | SOC building blocks, operating models and architecture |

### 🟩 Green · SOC & engineering

| # | Learning track | Focus |
|---|---|---|
| 11 | 🚨 [Enterprise SOC Operations](SOC-Analyst-Roadmap-main%20(2026-27)/11-Enterprise-SOC-Operations.md) | Triage, escalation, service levels, metrics |
| 12 | 🎯 [Detection Engineering](SOC-Analyst-Roadmap-main%20(2026-27)/12-Detection-Engineering.md) | Detection logic, testing, tuning, quality |
| 13 | 🪟 [Microsoft Sentinel & Defender XDR](SOC-Analyst-Roadmap-main%20(2026-27)/13-Microsoft-Sentinel-Defender-XDR.md) | SIEM/XDR concepts and investigation workflows |
| 14 | 📊 [Splunk, SentinelOne, and Akamai](SOC-Analyst-Roadmap-main%20(2026-27)/14-Splunk-SentinelOne-Akamai.md) | SIEM, endpoint and web security telemetry |
| 15 | 🔐 [Identity & Cloud Security](SOC-Analyst-Roadmap-main%20(2026-27)/15-Identity-Cloud-Security.md) | Identity controls and cloud security operations |
| 16 | 🩹 [Vulnerability & Exposure Management](SOC-Analyst-Roadmap-main%20(2026-27)/16-Vulnerability-Exposure-Management.md) | Exposure context, prioritization, remediation |
| 17 | 🔬 [DFIR & Threat Hunting](SOC-Analyst-Roadmap-main%20(2026-27)/17-DFIR-Threat-Hunting.md) | Evidence handling, investigation, hunt methodology |
| 18 | 🔁 [SOAR & Security Automation](SOC-Analyst-Roadmap-main%20(2026-27)/18-SOAR-Security-Automation.md) | Safe, auditable response automation |
| 19 | 🧠 [AI, LLM, RAG, and Agent Security](SOC-Analyst-Roadmap-main%20(2026-27)/19-AI-LLM-RAG-Agent-Security.md) | AI application risks, retrieval and agent boundaries |
| 20 | 🏢 [Enterprise SOC Architecture](SOC-Analyst-Roadmap-main%20(2026-27)/20-Enterprise-SOC-Architecture.md) | Scalable SOC platforms, resilience, governance |
| 21 | 🧪 [SOC Labs & Projects](SOC-Analyst-Roadmap-main%20(2026-27)/21-SOC-Labs-Projects.md) | Structured defensive practice and portfolio projects |
| 22 | 🎓 [SOC Career & Certifications](SOC-Analyst-Roadmap-main%20(2026-27)/22-SOC-Career-Certifications.md) | Role progression, skills and certifications |

### 🟪 Violet · Advanced & architecture

| # | Learning track | Focus |
|---|---|---|
| 23 | 🧑‍💻 [Principal Security Engineering](SOC-Analyst-Roadmap-main%20(2026-27)/23-Principal-Security-Engineering.md) | Organization-wide security platforms and strategy |
| 24 | 🔒 [Zero Trust Architecture](SOC-Analyst-Roadmap-main%20(2026-27)/24-Zero-Trust-Architecture.md) | Identity-first access, policy and continuous evaluation |
| 25 | ☸️ [Cloud-Native Kubernetes Security](SOC-Analyst-Roadmap-main%20(2026-27)/25-Cloud-Native-Kubernetes-Security.md) | Workload, cluster and container security |
| 26 | 📦 [Software Supply Chain & AppSec](SOC-Analyst-Roadmap-main%20(2026-27)/26-Software-Supply-Chain-AppSec.md) | Secure development, dependencies, software provenance |
| 27 | 📡 [Platform Detection Engineering](SOC-Analyst-Roadmap-main%20(2026-27)/27-Platform-Detection-Engineering.md) | Detection platforms, data quality and scale |
| 28 | 🪪 [Advanced Identity Attack Paths](SOC-Analyst-Roadmap-main%20(2026-27)/28-Advanced-Identity-Attack-Paths.md) | Identity relationships, privilege paths, defensive analysis |
| 29 | 🧬 [Advanced DFIR & Malware](SOC-Analyst-Roadmap-main%20(2026-27)/29-Advanced-DFIR-Malware.md) | Forensic artifacts, timelines, safe analysis concepts |
| 30 | 🤖 [AI Agentic Security](SOC-Analyst-Roadmap-main%20(2026-27)/30-AI-Agentic-Security.md) | Agent permissions, prompt threats, trust boundaries |
| 31 | 🗃️ [Security Data Engineering](SOC-Analyst-Roadmap-main%20(2026-27)/31-Security-Data-Engineering.md) | Security data pipelines, schemas, observability |
| 32 | 🎯 [Exposure Management & CTEM](SOC-Analyst-Roadmap-main%20(2026-27)/32-Exposure-Management-CTEM.md) | Continuous exposure discovery and risk prioritization |
| 33 | ♻️ [Resilience & Ransomware Architecture](SOC-Analyst-Roadmap-main%20(2026-27)/33-Resilience-Ransomware-Architecture.md) | Recovery readiness, resilience and incident coordination |
| 34 | 🏭 [OT, IoT & Edge Security](SOC-Analyst-Roadmap-main%20(2026-27)/34-OT-IoT-Edge-Security.md) | Operational technology, connected devices and safety |
| 35 | 🔑 [Privacy, Cryptography & PQC](SOC-Analyst-Roadmap-main%20(2026-27)/35-Privacy-Cryptography-PQC.md) | Privacy engineering, key management, post-quantum readiness |
| 36 | ⚖️ [Architecture Governance & GRC](SOC-Analyst-Roadmap-main%20(2026-27)/36-Architecture-Governance-GRC.md) | Architecture reviews, risk and governance |
| 37 | 🧭 [Security Leadership 2027](SOC-Analyst-Roadmap-main%20(2026-27)/37-Security-Leadership-2027.md) | Technical strategy, communication, team leadership |
| 38 | 🛡️ [Vulnerability, Zero-Day & WAF Defense](SOC-Analyst-Roadmap-main%20(2026-27)/Vulnerability-Zero-Day-and-WAF/README.md) | Defensive vulnerability and web application protection |

---

## 🎓 Certification pathways

Choose certifications based on your target role, current experience, region, budget and employer requirements. Certifications complement hands-on capability; they do not replace practical evidence. Always check the official provider page for current exam objectives, prerequisites, pricing and renewal policies.

| Stage / direction | Examples to research | Good companion evidence |
|---|---|---|
| 🌱 **Starting out** | [CompTIA Security+](https://www.comptia.org/certifications/security) · [ISC2 Certified in Cybersecurity](https://www.isc2.org/certifications/cc) | Networking notes, basic security lab write-ups |
| 🚨 **SOC analyst / incident response** | [CompTIA CySA+](https://www.comptia.org/certifications/cybersecurity-analyst) · [GIAC GCIH](https://www.giac.org/certifications/certified-incident-handler-gcih/) | Triage cases, timelines, incident reports |
| 🔎 **Microsoft security operations** | [Microsoft SC-200](https://learn.microsoft.com/credentials/certifications/security-operations-analyst/) | Sentinel / Defender investigation portfolio |
| 📊 **Splunk operations** | [Splunk certification paths](https://www.splunk.com/en_us/training/certification-track.html) | Search examples, dashboards, detection tuning notes |
| ☁️ **Cloud security** | [AWS Security certification](https://aws.amazon.com/certification/certified-security-specialty/) · [Microsoft security credentials](https://learn.microsoft.com/credentials/browse/?products=azure) · [Google Cloud security training](https://cloud.google.com/learn/certification) | Cloud logging review and secure configuration project |
| ☸️ **Kubernetes / cloud-native** | [Kubernetes certification](https://training.linuxfoundation.org/certification/) (review current security-focused options) | Threat model, workload-security design and lab evidence |
| 🏛️ **Senior architecture / leadership** | [CISSP](https://www.isc2.org/certifications/cissp) · [CISM](https://www.isaca.org/credentialing/cism) | Architecture decisions, risk communication, leadership examples |

> Certification names, availability and exam details can change. Some credentials have experience requirements; verify eligibility directly with the issuing organization before planning an exam.

## 🔭 Future security drivers

Security work will keep changing as organizations adopt new platforms and attackers adapt. Build durable fundamentals, then revisit these areas regularly:

| Emerging driver | Defensive learning focus |
|---|---|
| 🤖 **AI and autonomous agents** | Model and agent threat modeling, data boundaries, tool permissions, human oversight, evaluation and auditability |
| ☁️ **Cloud-native and platform engineering** | Workload identity, containers, Kubernetes controls, software delivery pipelines and runtime visibility |
| 🪪 **Identity-first security** | Phishing-resistant authentication, privileged access, machine identities and identity attack-path analysis |
| 🔗 **Software supply-chain risk** | Dependency governance, SBOMs, provenance, build integrity and secure-by-design practices |
| 📈 **Security data and detection at scale** | Data quality, telemetry coverage, privacy-aware analytics, detection testing and operational metrics |
| 🧩 **Continuous exposure management** | Asset context, exploitability, business impact, remediation validation and risk ownership |
| ♻️ **Cyber resilience** | Recoverability, immutable backups, crisis exercises, continuity planning and tested response procedures |
| 🏭 **OT, IoT and edge systems** | Safety and availability requirements, asset visibility, segmentation and vendor coordination |
| 🔐 **Privacy and cryptographic change** | Data minimization, key lifecycle, crypto agility and post-quantum migration awareness |
| 🌍 **Regulation and third-party risk** | Governance, evidence, supplier assurance, privacy obligations and jurisdiction-specific requirements |

## 🗺️ Future learning plan

Use this adaptable sequence as a guide—not a fixed timetable. Move forward when you can explain and demonstrate the learning outcome.

| Phase | Learning goal | Suggested deliverable |
|---|---|---|
| **1 · Establish** | Strengthen networking, Linux/Windows, identity and security principles | Personal knowledge map and isolated lab plan |
| **2 · Operate** | Practice alert triage, evidence capture, escalation and communication | Three synthetic or training-case investigation reports |
| **3 · Detect** | Learn query languages, ATT&CK mapping, detection testing and tuning | Small detection pack with test cases and limitations |
| **4 · Investigate** | Develop DFIR, threat-hunting, cloud and identity skills | Hunt report and cloud/identity visibility review |
| **5 · Engineer** | Explore automation, security data, platform and AI security | Human-approved automation demo and AI threat model |
| **6 · Design** | Develop architecture, resilience, governance and leadership skills | Architecture diagram, decision record and presentation |
| **7 · Refresh** | Reassess skills and references as threats, technology and standards evolve | Quarterly learning review and updated portfolio |

## 🧪 Labs & portfolio

Build practical evidence as you learn. Use authorized labs and document assumptions and limitations.

| Project | Portfolio evidence |
|---|---|
| 📝 SOC investigation walkthrough | Incident timeline, evidence notes and lessons learned |
| 🎯 Detection-as-code starter pack | Scoped detections, test cases and tuning notes |
| 🔎 Threat-hunting report | Hypothesis, data sources, findings and lab queries |
| ☁️ Cloud logging review | Telemetry coverage diagram and visibility gaps |
| ⚙️ SOAR approval workflow | Safe simulation, human approval, audit trail and rollback |
| 🤖 AI application threat model | Trust boundaries, risk scenarios and mitigations for a toy application |
| 🏗️ Architecture decision record | Diagram, assumptions, trade-offs and follow-up actions |

## 🧰 Trusted references & tools

Official documentation and learning resources are a good starting point. Tool names are examples to explore—not endorsements or a requirement to use them all.

| Area | References |
|---|---|
| 🧭 Frameworks | [MITRE ATT&CK](https://attack.mitre.org/) · [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework) · [CISA KEV Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) |
| 🎯 Detection | [Sigma](https://sigmahq.io/) · [Microsoft Sentinel docs](https://learn.microsoft.com/azure/sentinel/) · [Splunk Security Content](https://research.splunk.com/) |
| 🌐 Network visibility | [Wireshark docs](https://www.wireshark.org/docs/) · [Zeek docs](https://docs.zeek.org/) |
| 🔬 Investigation | [Velociraptor docs](https://docs.velociraptor.app/) · [Security Onion docs](https://docs.securityonion.net/) |
| 🧪 Safe learning | [MITRE ATT&CK resources](https://attack.mitre.org/resources/) · [CISA resources](https://www.cisa.gov/resources-tools) · Vendor training tenants and isolated home labs |

## 📂 Source materials

- [📚 Main Documents index](SOC-Analyst-Roadmap-main%20(2026-27)/Main-Documents/README.md)
- [🗺️ Roadmap resources](SOC-Analyst-Roadmap-main%20(2026-27)/ROADMAP/)
- [🖼️ Diagrams](SOC-Analyst-Roadmap-main%20(2026-27)/DIAGRAMS/)
- [✅ Safe integration instructions](SOC-Analyst-Roadmap-main%20(2026-27)/INSTRUCTIONS.md)

<div align="center">

[![Evidence](https://img.shields.io/badge/PRINCIPLE-Evidence%20before%20conclusions-0B1020?style=flat-square&labelColor=2563EB)](#)
[![Least privilege](https://img.shields.io/badge/PRINCIPLE-Least%20privilege-0B1020?style=flat-square&labelColor=16A34A)](#)
[![Resilience](https://img.shields.io/badge/PRINCIPLE-Resilience%20by%20design-0B1020?style=flat-square&labelColor=7C3AED)](#)

**Built for curious defenders — from first alert to security architecture. 💙**

</div>
