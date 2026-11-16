# Threat Intelligence Tools

A defensive reference for collecting, organizing, enriching, and sharing threat intelligence. Intelligence is context—not proof by itself. Validate indicators against reliable sources, relevance, timestamps, and your own telemetry before taking action.

## Tool landscape

| Tool / resource | Typical defensive use | Notes |
|---|---|---|
| [MISP](https://www.misp-project.org/) | Share and manage threat-intelligence events, indicators, and relationships | Open-source platform; control sharing groups and sensitive data carefully |
| [OpenCTI](https://opencti.io/) | Connect intelligence entities, reports, observables, and relationships | Open-source platform with integrations; curate sources and confidence |
| [VirusTotal](https://www.virustotal.com/) | Enrich file hashes, domains, URLs, and IP addresses | Review service terms and data-sharing/privacy implications before submitting artifacts |
| [AlienVault OTX](https://otx.alienvault.com/) | Review and exchange community threat-intelligence pulses | Community submissions vary in quality; corroborate before action |
| [CISA KEV Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) | Prioritize known exploited vulnerabilities for remediation | Pair with asset exposure, business criticality, and vendor guidance |
| [MITRE ATT&CK](https://attack.mitre.org/) | Describe adversary behaviors and map intelligence to defensive coverage | A knowledge base, not an IOC feed; use it to structure analysis |

## A responsible intelligence workflow

1. Record the source, collection time, confidence, and expiration or review date.
2. Normalize and deduplicate observables; retain provenance and context.
3. Enrich using approved sources and confirm the data-handling terms.
4. Map relevant behaviors to ATT&CK and compare with available telemetry.
5. Share only with authorized audiences and appropriate handling markings.
6. Validate proposed blocks or detections in a controlled process; provide rollback and false-positive review.

> **Safety and privacy:** Do not upload confidential samples, customer data, credentials, or internal indicators to public services without authorization. Indicators can be stale, shared, or misattributed; avoid automatic blocking based only on a single feed.

## Further reading

- [STIX 2.1](https://oasis-open.github.io/cti-documentation/)
- [TAXII 2.1](https://oasis-open.github.io/cti-documentation/)
- [CISA Cybersecurity Advisories](https://www.cisa.gov/news-events/cybersecurity-advisories)
- [MITRE ATT&CK](https://attack.mitre.org/)
