# DFIR & Forensics Tools

Digital forensics and incident response (DFIR) require careful evidence handling, authorization, privacy controls, and repeatable documentation. Follow your organization’s incident-response and evidence-handling procedures; laws and requirements vary by jurisdiction.

## Defensive tools and references

| Tool / resource | Typical use | Handling reminders |
|---|---|---|
| [Autopsy](https://www.autopsy.com/) | Forensic examination of disk images and case artifacts | Work from verified copies; document hashes, versions, and examiner actions |
| [Volatility 3](https://volatility3.readthedocs.io/) | Memory-forensics framework for supported captures | Preserve original evidence and record profile/plugin assumptions |
| [Plaso / log2timeline](https://plaso.readthedocs.io/) | Build timelines from supported forensic sources | Preserve source timestamps and account for time-zone and clock differences |
| [KAPE](https://www.kroll.com/en/insights/publications/cyber/kroll-artifact-parser-extractor-kape) | Collect and parse selected Windows artifacts in authorized investigations | Collection changes system state; document scope and approvals |
| [Velociraptor](https://docs.velociraptor.app/) | Authorized endpoint collection and response workflows | Apply least privilege, narrow collection scope, and retain audit logs |
| [CyberChef](https://gchq.github.io/CyberChef/) | Decode, transform, and inspect data during analysis | Prefer offline/local use for sensitive content; transformations are not evidence by themselves |
| [NIST SP 800-86](https://csrc.nist.gov/pubs/sp/800/86/final) | Guidance for integrating forensics into incident response | Use alongside current organizational and legal requirements |

## Evidence-handling checklist

- Confirm authority, incident scope, and the evidence custodian.
- Preserve originals; analyze verified working copies where practical.
- Record acquisition method, timestamps, time zone, tool/version, and cryptographic hashes when appropriate.
- Maintain a chain-of-custody log and restrict access to case materials.
- Avoid executing unknown files on production systems; use isolated, approved analysis environments.
- Document limitations and distinguish observed facts from hypotheses.

> This is a learning reference, not legal advice or a substitute for an organization’s forensic policy. Never collect from systems without explicit authorization.
