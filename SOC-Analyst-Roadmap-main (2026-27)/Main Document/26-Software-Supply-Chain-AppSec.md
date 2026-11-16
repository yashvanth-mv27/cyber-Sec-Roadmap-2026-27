# Application Security and Software Supply Chain

**Track:** Advanced / Architect / Principal engineer  ·  **Status:** Reference design, not production validated

## What this discipline covers
Cover secure SDLC, threat modeling, SAST/DAST/SCA, SBOM, provenance, build attestations, artifact signing, secrets scanning, CI/CD hardening and dependency governance.

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
Design a pipeline that checks dependencies, generates an SBOM, verifies artifact provenance and gates high-risk releases.

## Expected deliverables
Pipeline flow; SBOM example; signing verification; exceptions policy. Add a diagram, validation matrix, expected-versus-observed results and an implementation backlog.

## Key design trade-off
A clean scanner result does not prove a dependency or artifact is trustworthy.

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
