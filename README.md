<div align="center">

# 🛡️ Cyber Security ROADMAP
### 2026–27 · From first alert to resilient enterprise defense

**DETECT WITH CONTEXT　·　RESPOND WITH DISCIPLINE　·　LEAD WITH EVIDENCE**

[![FOUNDATION](https://img.shields.io/badge/01%E2%80%9310-FOUNDATION-0284C7?style=for-the-badge&logo=bookstack&logoColor=white)](#-complete-roadmap)
[![SOC OPERATIONS](https://img.shields.io/badge/11%E2%80%9322-SOC%20OPERATIONS-15803D?style=for-the-badge&logo=shield&logoColor=white)](#-soc-operations-kpi-framework)
[![ADVANCED DEFENSE](https://img.shields.io/badge/23%E2%80%9338-ADVANCED%20DEFENSE-6D28D9?style=for-the-badge&logo=target&logoColor=white)](#-architecture-maturity-model)

[📊 Operations KPIs](#-soc-operations-kpi-framework) · [👥 Team roles](#-team-and-role-matrix) · [🏛️ Maturity](#-architecture-maturity-model) · [🧭 Leadership](#-leadership-roadmap) · [🧰 Tool guides](#-root-level-defensive-tool-guides)

</div>

> [!IMPORTANT]
> **Authorized defensive learning only.** Use systems and data you own or have explicit permission to monitor or assess. Practice in isolated labs, use synthetic or public training data, and never publish credentials, secrets, or customer data.

---

## 📟 Executive SOC overview

> **KPI strip — measurement framework, not live repository metrics.** Establish baselines and targets from your organization’s risk, staffing, business hours, telemetry, and regulatory needs. Do not compare teams without consistent definitions and context.

<div align="center">

![Coverage](https://img.shields.io/badge/01%20%E2%80%A2%20VISIBILITY-Telemetry%20coverage-0B1020?style=for-the-badge&labelColor=2563EB)
![Detection](https://img.shields.io/badge/02%20%E2%80%A2%20DETECTION-Quality%20%26%20validation-0B1020?style=for-the-badge&labelColor=0891B2)
![Response](https://img.shields.io/badge/03%20%E2%80%A2%20RESPONSE-Time%20%26%20outcomes-0B1020?style=for-the-badge&labelColor=16A34A)
![Resilience](https://img.shields.io/badge/04%20%E2%80%A2%20RESILIENCE-Recovery%20readiness-0B1020?style=for-the-badge&labelColor=7C3AED)

</div>

| Executive measure | Example definition | Leadership question |
|---|---|---|
| **Telemetry coverage** | In-scope critical assets reporting the required, usable security data | Which important services or identities are not visible to responders? |
| **Detection quality** | Tested detections, actionable alert rate, false-positive review, and known coverage gaps | Are detections reliable, explainable, and mapped to relevant risks? |
| **Response performance** | Time to acknowledge, investigate, contain, and recover—segmented by severity and service hours | Where do handoffs, approvals, or missing evidence create delay? |
| **Case outcomes** | Case volume, severity, recurrence, root-cause themes, and closure quality | Are incidents preventing recurrence or only closing tickets? |
| **Exposure remediation** | Risk-prioritized remediation age and validation status for critical exposures | Are owners reducing material risk within agreed timeframes? |
| **Automation assurance** | Workflow success/failure, human approval, audit completeness, and rollback readiness | Is automation safe, measurable, and recoverable when it fails? |
| **Resilience** | Exercise findings, recovery test results, and tracked corrective actions | Can critical services recover under realistic incident conditions? |

**Executive review cadence:** operational review for current workload and blockers · monthly trend review for outcomes and control gaps · quarterly risk and investment review with accountable owners.

## 🧭 Roadmap dashboard

| Learning stage | Mission | Evidence to build |
|---|---|---|
| 🔹 **01–10 · Foundation** | Network, operating systems, security, cloud and SOC architecture basics | Knowledge map, foundational labs, diagrams |
| 🟩 **11–22 · SOC operations** | Triage, SIEM/XDR, detection, DFIR, automation and career growth | Case reports, tested detections, portfolio |
| 🟪 **23–38 · Advanced defense** | Platform engineering, AI, resilience, governance and leadership | Threat models, architecture records, project demos |

`FOUNDATIONS → SOC ANALYST → DETECTION ENGINEER → SECURITY ENGINEER → SECURITY ARCHITECT / LEADER`

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

---

## 👥 Team and role matrix

Roles vary by organization; one person may cover multiple responsibilities. Define clear decision rights, escalation routes, and coverage expectations for your own operating model.

| Role | Primary responsibilities | Key interfaces | Example outcomes |
|---|---|---|---|
| **SOC L1 / Monitoring Analyst** | Validate alerts, enrich context, document evidence, escalate to playbooks | Service desk, L2, incident coordinator | Complete triage record; timely escalation |
| **SOC L2 / Incident Analyst** | Investigate incidents across endpoint, identity, network, and cloud | L1, DFIR, IT/service owners | Evidence-based incident assessment and response recommendation |
| **SOC L3 / Incident Lead** | Coordinate complex investigations, scope impact, guide containment and recovery | Incident commander, legal/privacy, business owners | Shared incident picture, decisions, recovery tracking |
| **Detection Engineer** | Build, test, tune, document, and retire analytics | SOC analysts, data platform, threat intelligence | Reliable detections with tests, ownership, and coverage rationale |
| **Threat Hunter / Intelligence Analyst** | Form hypotheses, assess intelligence, identify telemetry gaps | Detection engineering, incident response, risk teams | Reproducible hunt findings and actionable context |
| **DFIR Specialist** | Preserve and analyze evidence under approved procedures | Incident lead, legal/privacy, system owners | Defensible findings, timeline, and documented limitations |
| **SOAR / Platform Engineer** | Maintain ingestion, integrations, workflows, access, and platform reliability | Detection, IT, cloud, identity teams | Governed and observable security platform and automation |
| **SOC Manager / Director** | Set service model, staffing, priorities, metrics, quality, and improvement | CISO, business leadership, technology owners | Risk-aligned operating plan and transparent performance review |
| **Security Architect / Principal Engineer** | Set target patterns, trust boundaries, resilience, and technical guardrails | Product/platform leaders, GRC, executives | Reusable architecture decisions tied to business risk |

**Governance principle:** investigation teams recommend actions; designated business and technical owners authorize actions according to incident policy and impact. Keep high-impact containment decisions auditable.

## 🏛️ Architecture maturity model

Use this as a discussion aid, not a certification or universal score. Assess each capability separately, record evidence, and prioritize improvements by risk and feasibility.

| Level | Name | Typical characteristics | Next-step focus |
|---|---|---|---|
| **1** | **Ad hoc** | Reactive alert handling; unclear ownership; inconsistent records; limited visibility | Identify critical assets, assign owners, establish incident intake and evidence practices |
| **2** | **Repeatable** | Documented triage and escalation; core log sources; basic case tracking and access control | Standardize severity, playbooks, retention, and quality review |
| **3** | **Defined** | Governed SOC processes; detection lifecycle; cross-domain telemetry; regular exercises and reporting | Add coverage objectives, testing, threat-informed prioritization, and service ownership |
| **4** | **Measured** | Data quality and operational outcomes measured; detection tests; controlled automation; recovery evidence | Use trend analysis to tune investment, reduce systemic gaps, and validate resilience |
| **5** | **Adaptive** | Continuous improvement across identity, cloud, endpoint, applications, and AI; architecture aligned to changing risk | Sustain independent validation, learning loops, and accountable risk decisions |

**Assessment dimensions:** people and operating model · telemetry and data governance · detection and response · identity/cloud/platform coverage · automation safety · resilience and recovery · metrics and executive oversight.

## 🧭 Leadership roadmap

A practical progression from technical contribution to organization-wide security leadership:

| Step | Leadership capability | Practice / artifact |
|---|---|---|
| **1 · Own a case** | Communicate facts, confidence, impact, and open questions clearly | Concise incident brief and evidence timeline |
| **2 · Improve a workflow** | Find repeated friction and coordinate a measured improvement | Before/after process map with quality and risk considerations |
| **3 · Lead a technical initiative** | Set scope, owners, milestones, dependencies, and acceptance criteria | Detection, telemetry, or resilience project plan |
| **4 · Design a service** | Balance coverage, staffing, technology, privacy, reliability, and cost | SOC service definition and operating-level measures |
| **5 · Influence architecture** | Explain trust boundaries, trade-offs, exceptions, and residual risk | Architecture decision record and review presentation |
| **6 · Advise executives** | Translate security signals into business impact, choices, and accountable decisions | One-page risk brief with options and recommended action |
| **7 · Build sustainable capability** | Develop people, succession, exercises, governance, and continuous learning | Skills matrix, tabletop lessons, and quarterly improvement plan |

**Leadership habits:** make uncertainty explicit · preserve evidence · invite challenge · assign an owner and due date to decisions · communicate impact without overstating certainty · learn from incidents without blame.

---

## 🧭 Complete roadmap

Explore the 38 learning topics from the `SOC-Analyst-Roadmap-main (2026-27)` materials. Each link opens its guide. Root-level tool guides are linked separately below; the roadmap folder remains unchanged.

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

## 🧰 Root-level defensive tool guides

These standalone guides live in the repository root—not inside the roadmap folder.

| Guide | Covers |
|---|---|
| 🧭 [Threat Intelligence Tools](THREAT-INTELLIGENCE-TOOLS.md) | MISP, OpenCTI, VirusTotal, OTX, CISA KEV, STIX/TAXII |
| 🔎 [Threat Hunting Tools](THREAT-HUNTING-TOOLS.md) | Sentinel, Splunk, Elastic, Zeek, osquery, Velociraptor, ATT&CK Navigator |
| 🔬 [DFIR & Forensics Tools](DFIR-FORENSICS-TOOLS.md) | Autopsy, Volatility 3, Plaso, KAPE, Velociraptor, evidence handling |
| 📊 [SIEM & SOAR Tools](SIEM-SOAR-TOOLS.md) | Sentinel, Splunk, Elastic, Google SecOps, Wazuh, XSOAR, Tines, Shuffle |
| 🤖 [AI SOC Tools](AI-SOC-TOOLS.md) | Intezer and other AI-assisted SOC examples, evaluation and safe adoption |

## 🎓 Certification pathways

Select certifications according to your goals, experience, region, budget, and employer requirements. They complement hands-on capability; they do not replace practical evidence. Confirm current exams, eligibility, and renewal rules with each issuer.

| Direction | Examples to research | Pair with |
|---|---|---|
| 🌱 Starting out | [CompTIA Security+](https://www.comptia.org/certifications/security) · [ISC2 CC](https://www.isc2.org/certifications/cc) | Networking notes and foundational lab write-ups |
| 🚨 SOC / incident response | [CompTIA CySA+](https://www.comptia.org/certifications/cybersecurity-analyst) · [GIAC GCIH](https://www.giac.org/certifications/certified-incident-handler-gcih/) | Triage cases, timelines, incident reports |
| 🔎 Microsoft security operations | [Microsoft SC-200](https://learn.microsoft.com/credentials/certifications/security-operations-analyst/) | Sentinel / Defender investigation portfolio |
| 📊 Splunk operations | [Splunk certification paths](https://www.splunk.com/en_us/training/certification-track.html) | Search examples, dashboards, tuning notes |
| ☁️ Cloud security | [AWS Security Specialty](https://aws.amazon.com/certification/certified-security-specialty/) · [Microsoft credentials](https://learn.microsoft.com/credentials/browse/?products=azure) · [Google Cloud certifications](https://cloud.google.com/learn/certification) | Cloud logging and configuration review |
| 🏛️ Senior architecture / leadership | [CISSP](https://www.isc2.org/certifications/cissp) · [CISM](https://www.isaca.org/credentialing/cism) | Architecture decisions, risk communication, leadership examples |

## 🔭 Future security drivers

| Driver | Defensive learning focus |
|---|---|
| 🤖 AI and autonomous agents | Threat modeling, data boundaries, tool permissions, oversight and evaluation |
| ☁️ Cloud-native platforms | Workload identity, containers, Kubernetes controls and runtime visibility |
| 🪪 Identity-first security | Phishing-resistant authentication, privileged access, machine identities |
| 🔗 Software supply chain | Dependency governance, SBOMs, provenance and build integrity |
| 📈 Security data engineering | Data quality, telemetry coverage, privacy-aware analytics and detection testing |
| 🧩 Continuous exposure management | Asset context, exploitability, business impact and remediation validation |
| ♻️ Cyber resilience | Recovery readiness, crisis exercises and tested response procedures |
| 🏭 OT, IoT and edge | Safety, availability, asset visibility and segmentation |
| 🔐 Privacy and cryptographic change | Data minimization, key lifecycle, crypto agility and post-quantum readiness |
| 🌍 Governance and third-party risk | Evidence, supplier assurance, privacy obligations and risk ownership |

## 🗺️ Future learning plan

| Phase | Goal | Suggested deliverable |
|---|---|---|
| **1 · Establish** | Networking, operating systems, identity and security principles | Knowledge map and isolated lab plan |
| **2 · Operate** | Triage, evidence, escalation and communication | Synthetic-case investigation reports |
| **3 · Detect** | Query languages, ATT&CK mapping, detection tests and tuning | Small detection pack with limitations |
| **4 · Investigate** | DFIR, hunting, cloud and identity skills | Hunt report and visibility review |
| **5 · Engineer** | Automation, security data, platforms and AI security | Human-approved automation demo and AI threat model |
| **6 · Design** | Architecture, resilience, governance and leadership | Architecture diagram and decision record |
| **7 · Refresh** | Reassess skills as technology and standards evolve | Quarterly learning review and updated portfolio |

## 📂 Roadmap source materials

- [📚 Main Documents index](SOC-Analyst-Roadmap-main%20(2026-27)/Main-Documents/README.md)
- [🗺️ Roadmap resources](SOC-Analyst-Roadmap-main%20(2026-27)/ROADMAP/)
- [🖼️ Diagrams](SOC-Analyst-Roadmap-main%20(2026-27)/DIAGRAMS/)
- [✅ Safe integration instructions](SOC-Analyst-Roadmap-main%20(2026-27)/INSTRUCTIONS.md)

<div align="center">

[![Evidence](https://img.shields.io/badge/PRINCIPLE-Evidence%20before%20conclusions-0B1020?style=flat-square&labelColor=2563EB)](#)
[![Least privilege](https://img.shields.io/badge/PRINCIPLE-Least%20privilege-0B1020?style=flat-square&labelColor=16A34A)](#)
[![Resilience](https://img.shields.io/badge/PRINCIPLE-Resilience%20by%20design-0B1020?style=flat-square&labelColor=7C3AED)](#)

**Built for curious defenders and accountable security leaders.**

</div>
