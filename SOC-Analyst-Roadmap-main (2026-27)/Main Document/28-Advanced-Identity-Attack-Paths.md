# Advanced Identity and Attack-Path Defense

**Track:** Advanced / Architect / Principal engineer  ·  **Status:** Reference design, not production validated

## What this discipline covers
Analyze Active Directory and Entra ID trust relationships, Kerberos delegation, service principals, OAuth permissions, token replay, hybrid sync, privilege graphs and lateral movement paths.

## Why senior engineers must know it
A senior engineer translates threat models and business constraints into controls that are operable, testable and cost-aware. An architect additionally evaluates trade-offs across teams, vendors, trust boundaries, data flows, resilience and governance.

## Architecture method
1. **Define the system:** users, workloads, assets, data classifications and dependencies.
2. **Identify trust boundaries:** internet, endpoint, identity, workload, cloud control plane, third-party services and AI tools as applicable.
3. **Model abuse cases:** attacker goals, entry points, privilege escalation, lateral movement, data access and recovery impact.
4. **Select controls:** preventive, detective, responsive and recovery layers with explicit owners.
5. **Specify telemetry:** events, field schema, collection method, freshness, retention, quality and cost.
6. **Define failure modes:** missing logs, unavailable identity providers, automation failures, false positives and human approval delays.
7. **Validate safely:** positive and negative tests in an authorized lab; document evidence and assumptions.
8. **Operate and improve:** SLOs, exception process, tabletop exercises, control testing, architecture reviews and continuous feedback.

## 2027 practical design challenge
Map a synthetic attack path from an overprivileged application to a sensitive resource and recommend controls.

## Expected deliverables
Privilege graph; evidence timeline; access review; remediation priority. Add a diagram, validation matrix, expected-versus-observed results and an implementation backlog.

## Key design trade-off
Removing a single privilege may not close alternative attack paths.

## Sample design review questions
- Which identities or services can bypass this control, and how is that audited?
- What is the business impact of an unavailable dependency or a false positive?
- Which telemetry proves that the control is working, and what is missing?
- How would the design scale to ten times the event volume?
- How are access, data residency, secrets, privacy and evidence retention handled?
- Who owns exceptions, rollback, incident response and periodic control testing?

## Suggested study and lab sequence
**Week 1:** Read authoritative product/security documentation and sketch the architecture.  
**Week 2:** Build a minimal synthetic lab and record baseline events.  
**Week 3:** Simulate safe failure/abuse cases and capture test results.  
**Week 4:** Tune, write an architecture decision record and present findings.

## Reference starting points
- [MITRE ATT&CK](https://attack.mitre.org/) for adversary behavior and detection coverage.
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework) for governance and outcomes.
- [CISA](https://www.cisa.gov/) for defensive guidance and advisories.
- Primary vendor documentation for implementation-specific features, schemas and limits.

> **Evidence standard:** Proposed architecture and examples are not validated implementations. Record lab platform versions, tests and reviewer sign-off before marking them tested.
