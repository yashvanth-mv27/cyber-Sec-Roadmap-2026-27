# Topic workflow diagrams

These conceptual, defensive diagrams show how common security topics connect to people, telemetry, tools, decisions, and feedback. Product names are examples; exact connectors and features depend on licensing and configuration. Use authorized labs and synthetic/public training data.

## Windows endpoint to SIEM

```mermaid
flowchart LR
    W[Windows endpoint and server events] --> A[Approved agent or forwarder]
    A --> C[Collector / secure transport]
    C --> V[Validate source, time, and schema]
    V --> N[Normalize and enrich asset / identity context]
    N --> S[(SIEM / security data lake)]
    S --> D[Detection and investigation]
    D --> F[Analyst feedback and tuning]
```

## Linux host to SIEM

```mermaid
flowchart LR
    L[Linux auth, audit, system and service logs] --> F[Approved forwarder]
    F --> C[Collector with transport and access controls]
    C --> P[Parse and validate timestamps / fields]
    P --> E[Enrich host, owner, and environment]
    E --> S[(SIEM / data lake)]
    S --> Q[Queries, detections, and case workflow]
```

## Firewall and network sensor to SIEM

```mermaid
flowchart LR
    FW[Firewall / DNS / proxy / network sensor] --> C[Syslog or supported connector]
    PCAP[Authorized metadata or training PCAP] --> NS[Network analysis sensor]
    NS --> C
    C --> N[Normalize source, destination, action, time]
    N --> R[Retention and access policy]
    R --> SIEM[(SIEM)]
    SIEM --> A[Correlate with identity, endpoint, and asset context]
```

## Email security investigation

```mermaid
flowchart TD
    U[User report or mail-security alert] --> M[Preserve message metadata and scope]
    M --> C[Check sender context, authentication results, URL and attachment verdicts]
    C --> E[Correlate recipient, identity, and endpoint events]
    E --> D{Evidence supports malicious activity?}
    D -->|No / unclear| H[Document rationale; request more evidence or close]
    D -->|Yes| I[Escalate; follow approved message and account response]
    I --> V[Verify affected scope and recovery]
    H --> L[Lessons and tuning]
    V --> L
```

## EDR / XDR to SIEM and case management

```mermaid
flowchart LR
    EP[Endpoint telemetry] --> X[EDR / XDR analytics]
    X -->|Alert and context| C[Supported connector / API]
    C --> S[(SIEM and case management)]
    S --> A[Analyst validates alert and scope]
    A -->|Approved request| R[EDR response workflow]
    R --> EP
    A --> F[Feedback, detection tuning, and audit]
```

## Cloud and identity audit to SIEM

```mermaid
flowchart LR
    ID[Identity sign-in and audit events] --> COL[Provider connector / approved collector]
    CP[Cloud control-plane activity] --> COL
    DATA[Data access and workload audit] --> COL
    COL --> G[Least-privilege ingestion and schema checks]
    G --> S[(SIEM / governed data lake)]
    S --> C[Correlate user, device, resource, and risk context]
    C --> A[Analyst review and authorized response]
    A --> FB[Audit, retention, and lessons]
```

## Threat intelligence to detection workflow

```mermaid
flowchart LR
    R[Defined intelligence requirement] --> SRC[Approved sources and provenance]
    SRC --> Q[Quality, confidence, relevance, expiry, deduplication]
    Q --> E[Enrichment with organizational context]
    E --> DEC{Useful and safe to operationalize?}
    DEC -->|No| DOC[Document limitation / retain for analysis]
    DEC -->|Yes| DET[Controlled hunt or detection test]
    DET --> HUMAN[Analyst validation before blocking or response]
    HUMAN --> OUT[Feedback, expiry, and audit]
```

## SOAR: alert to controlled action

```mermaid
flowchart TD
    A[SIEM / EDR alert] --> T[Create case and deduplicate]
    T --> EN[Automated enrichment: asset, identity, reputation, related events]
    EN --> R[Evaluate playbook conditions and data quality]
    R --> H{Action impact and confidence}
    H -->|Low risk, reversible, pre-approved| AUTO[Run bounded action with audit and timeout]
    H -->|Disruptive or uncertain| APPROVAL[Analyst / incident lead approval]
    H -->|Insufficient evidence| WAIT[Request evidence; no containment]
    APPROVAL --> AUTO
    AUTO --> VERIFY[Verify result and capture evidence]
    WAIT --> CASE[Update case and notify owner]
    VERIFY --> CASE
    CASE --> FB[Review errors, outcomes, and playbook quality]
```

## Detection-engineering feedback loop

```mermaid
flowchart LR
    H[Threat model, hunt, incident, or requirement] --> SPEC[Behavior, scope, ATT&CK context, success criteria]
    SPEC --> DATA[Required telemetry and data-quality checks]
    DATA --> TEST[Positive, negative, and edge-case tests]
    TEST --> REVIEW[Peer review and risk assessment]
    REVIEW --> DEPLOY[Versioned, staged deployment with rollback]
    DEPLOY --> MEASURE[Coverage, precision, latency, cost, analyst impact]
    MEASURE --> H
```

## Diagram conventions

- Arrows represent logical data or decision flow, not a product-specific deployment guarantee.
- A human approval gate is explicit before disruptive actions such as disabling accounts or isolating business-critical systems.
- Add trust boundaries, data residency, ownership, retention, failure handling, and cost when adapting these diagrams to a real architecture.
- For the broader learning, triage, incident response, and cloud-native diagrams, see [FLOWCHARTS.md](FLOWCHARTS.md).
