# SOC and Security Architecture Flowcharts

Reusable Mermaid flowcharts for the learning paths and defensive operations described in this repository. GitHub renders these diagrams directly in Markdown. They are conceptual reference diagrams; adapt components, retention, access controls, and escalation criteria to your environment.

## 1. Learning journey: beginner to security architect

```mermaid
flowchart TD
    A[Beginner: computing, networking, security basics] --> B[Build a safe home lab]
    B --> C[SOC Analyst L1: monitor, triage, document]
    C --> D[SOC Analyst L2: investigate, scope, contain]
    D --> E[SOC Analyst L3: lead complex incidents]
    D --> H[Threat Hunter: form and test hypotheses]
    D --> I[Detection Engineer: author and validate detections]
    E --> J[Security Engineer: operate and improve controls]
    H --> J
    I --> J
    J --> K[Cloud Security Engineer]
    J --> L[SOC Architect]
    K --> M[Security Architect]
    L --> M
    C -. Practice and feedback .-> B
    H -. Findings become detections .-> I
    I -. Gaps inform hunts .-> H
```

## 2. SOC telemetry and log pipeline

```mermaid
flowchart LR
    subgraph Sources[Security telemetry sources]
        WIN[Windows endpoints and servers]
        LIN[Linux systems]
        NET[Firewalls, DNS, proxy, network sensors]
        MAIL[Email security]
        EDR[EDR and XDR]
        CLOUD[Cloud platforms and SaaS]
        IAM[Identity providers]
        TI[Threat intelligence feeds]
    end
    WIN --> COL[Collectors and forwarders]
    LIN --> COL
    NET --> COL
    MAIL --> COL
    EDR --> COL
    CLOUD --> COL
    IAM --> COL
    TI --> COL
    COL --> PIPE[Secure ingestion pipeline]
    PIPE --> PARSE[Parse and validate]
    PARSE --> NORM[Normalize to common schema]
    NORM --> ENRICH[Enrich: asset, identity, geo, threat context]
    ENRICH --> STORE[(SIEM and data lake)]
    STORE --> DET[Rules, analytics, and correlation]
    DET --> QUEUE[Alert queue and case management]
    QUEUE --> SOAR[SOAR: approved enrichment and response workflows]
    SOAR --> STORE
    QUEUE --> SOC[Analyst triage and investigation]
    SOC --> OUT[Document outcome, lessons, and tuning]
    OUT --> DET
```

## 3. Alert triage and escalation

```mermaid
flowchart TD
    A[Alert received] --> B[Validate alert and data quality]
    B --> C{True positive?}
    C -- No --> D[Record benign or false-positive reason]
    D --> E[Suggest tuning or telemetry improvement]
    E --> Z[Close with evidence and rationale]
    C -- Yes --> F[Identify affected user, host, cloud resource, and time range]
    F --> G[Enrich with asset criticality, identity, and related events]
    G --> H{Potential active harm or high impact?}
    H -- Yes --> I[Escalate to incident lead; follow approved containment plan]
    H -- No --> J[Continue scoped investigation]
    I --> K[Preserve evidence and coordinate response]
    J --> L{Scope and confidence sufficient?}
    L -- No --> M[Collect additional logs and endpoint or cloud evidence]
    M --> J
    L -- Yes --> N[Classify, assign severity, and recommend action]
    N --> O[Communicate findings and next steps]
    K --> P[Track remediation and recovery]
    O --> P
    P --> Q[Post-incident review and detection improvements]
    Q --> Z
```

## 4. Incident response lifecycle

```mermaid
flowchart LR
    PREP[Prepare: roles, playbooks, access, backups] --> DETECT[Detect and report]
    DETECT --> ANALYZE[Analyze: validate, scope, prioritize]
    ANALYZE --> CONTAIN[Contain: approved, proportionate actions]
    CONTAIN --> ERADICATE[Eradicate: remove root cause and persistence]
    ERADICATE --> RECOVER[Recover: restore and monitor safely]
    RECOVER --> LESSONS[Lessons learned: owners, dates, evidence]
    LESSONS --> PREP
    ANALYZE -. Preserve evidence throughout .-> EVIDENCE[(Evidence handling and timeline)]
    CONTAIN -. Coordinate with stakeholders .-> COMMS[Incident communications]
    ERADICATE -. Validate remediation .-> VERIFY[Verification and heightened monitoring]
    VERIFY --> RECOVER
```

## 5. Detection engineering feedback loop

```mermaid
flowchart TD
    A[Threat model, hunt finding, incident, or intel] --> B[Define behavior and detection objective]
    B --> C[Identify required telemetry and data fields]
    C --> D{Telemetry available and trustworthy?}
    D -- No --> E[Document gap; plan collection or enrichment]
    E --> C
    D -- Yes --> F[Write query or analytic with ATT&CK context]
    F --> G[Test against representative benign and labeled data]
    G --> H{Useful signal with acceptable noise?}
    H -- No --> I[Refine logic, thresholds, exclusions, or context]
    I --> G
    H -- Yes --> J[Peer review, version, and safely deploy]
    J --> K[Monitor alert quality, coverage, and performance]
    K --> L[Analyst feedback and incident outcomes]
    L --> B
```

## 6. Threat intelligence lifecycle

```mermaid
flowchart LR
    R[Requirements: decision and collection questions] --> C[Collection from approved sources]
    C --> P[Process: normalize, deduplicate, assess provenance]
    P --> A[Analyze: confidence, relevance, context, expiry]
    A --> D[Disseminate to the right teams and controls]
    D --> U[Use: hunt, detection, risk decisions, response]
    U --> F[Feedback: usefulness, false positives, gaps]
    F --> R
    P --> REG[(Managed indicator and intelligence repository)]
    REG --> D
```

## 7. Cloud-native SOC reference flow

```mermaid
flowchart TB
    subgraph Env[Cloud and identity environments]
        ID[Identity and access activity]
        CTRL[Control-plane audit events]
        WORK[Workloads, containers, and serverless]
        DATA[Data access and storage events]
        NET[Network flow and security controls]
        SAAS[SaaS and productivity services]
    end
    ID --> COL[Cloud-native connectors and collectors]
    CTRL --> COL
    WORK --> COL
    DATA --> COL
    NET --> COL
    SAAS --> COL
    COL --> SEC[Validated ingestion with least-privilege access]
    SEC --> SIEM[(SIEM and security data lake)]
    SIEM --> RULES[Detections, analytics, and correlation]
    RULES --> CASE[Cases and incident workflow]
    CASE --> HUMAN[Analyst validation and incident coordination]
    HUMAN --> RESP[Approved response: revoke sessions, isolate, or remediate]
    RESP --> ENV
    SIEM --> GOV[Retention, access audit, data residency, and cost controls]
```

## 8. Phishing investigation workflow

```mermaid
flowchart TD
    A[User report or email alert] --> B[Capture message headers, URLs, attachments, and recipient scope]
    B --> C[Analyze sender authentication, message context, and indicators]
    C --> D{Malicious or suspicious?}
    D -- No --> E[Document rationale and safely release or close]
    D -- Yes --> F[Search for related messages and affected recipients]
    F --> G[Check URL, attachment, identity, and endpoint telemetry]
    G --> H{Evidence of interaction or account compromise?}
    H -- No --> I[Remove or quarantine messages; block indicators as appropriate]
    H -- Yes --> J[Escalate incident; protect account and affected endpoints]
    J --> K[Preserve evidence and investigate scope]
    I --> L[Notify users and record actions]
    K --> L
    L --> M[Add lessons to detections, controls, and awareness]
```

## Rendering and contribution notes

- Keep diagrams focused on one workflow and use descriptive node labels.
- Prefer Mermaid `flowchart` syntax for GitHub Markdown compatibility.
- Distinguish automated actions from analyst decisions; require authorization for disruptive containment.
- Validate Mermaid changes in GitHub preview before merging.
