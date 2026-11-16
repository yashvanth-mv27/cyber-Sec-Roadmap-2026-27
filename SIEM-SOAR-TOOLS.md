# SIEM & SOAR Tools

SIEM platforms help teams collect, normalize, search, and correlate security events. SOAR platforms coordinate enrichment and response workflows. Product capabilities, licensing, and deployment options change; confirm details in current vendor documentation.

## SIEM / XDR examples

| Platform | Common learning areas | Official starting point |
|---|---|---|
| Microsoft Sentinel | Cloud SIEM, KQL, connectors, analytics, workbooks | [Microsoft Sentinel documentation](https://learn.microsoft.com/azure/sentinel/) |
| Splunk Enterprise Security | Search, data models, detections, investigation workflows | [Splunk Security](https://www.splunk.com/en_us/products/enterprise-security.html) |
| Elastic Security | Search, endpoint telemetry, detection rules, timelines | [Elastic Security](https://www.elastic.co/security) |
| Google Security Operations | Security analytics, investigation, detection and response | [Google SecOps](https://cloud.google.com/chronicle/docs) |
| Wazuh | Open-source security monitoring and log analysis | [Wazuh documentation](https://documentation.wazuh.com/) |

## SOAR / case workflow examples

| Platform / resource | Common learning areas | Official starting point |
|---|---|---|
| Microsoft Sentinel automation | Playbooks, connectors, approval and incident workflows | [Automation in Sentinel](https://learn.microsoft.com/azure/sentinel/automation/automation) |
| Cortex XSOAR | Case management, integrations, and orchestration concepts | [Cortex XSOAR documentation](https://docs-cortex.paloaltonetworks.com/r/Cortex-XSOAR) |
| Tines | No-code security workflow automation | [Tines documentation](https://www.tines.com/docs/) |
| Shuffle | Open-source security automation platform | [Shuffle documentation](https://shuffler.io/docs) |

## Design principles

- Define log sources, ownership, retention, privacy, and data-quality expectations.
- Normalize timestamps and fields; document missing telemetry and parsing limitations.
- Test detections with approved synthetic or lab data, including benign cases.
- Begin automation with reversible, low-impact enrichment and explicit audit logging.
- Require human approval for disruptive actions such as disabling accounts or isolating endpoints.
- Include timeouts, error paths, access controls, rollback procedures, and periodic review.

> Use only authorized environments and approved integrations. Do not paste real credentials, customer records, or sensitive incident data into public tools or demo tenants.
