# Threat Hunting Tools

Threat hunting is a hypothesis-driven, authorized review of defensive telemetry. Use tools only in environments you own or are permitted to monitor, and keep hunts scoped, documented, and privacy-aware.

## Defensive toolset

| Tool / resource | Typical use | Learning focus |
|---|---|---|
| [Microsoft Sentinel](https://learn.microsoft.com/azure/sentinel/) | Search and correlate cloud and enterprise security logs | KQL, data connectors, workbooks, and analytic rule tuning |
| [Splunk Security Content](https://research.splunk.com/) | Review searches, analytic stories, and investigation content | SPL, data models, source quality, and validation |
| [Elastic Security](https://www.elastic.co/security) | Search endpoint and other security telemetry | KQL/EQL, timelines, endpoint events, and detection rules |
| [Zeek](https://docs.zeek.org/) | Produce structured network-activity logs for defenders | Connection, DNS, HTTP, and TLS metadata in a lab |
| [osquery](https://www.osquery.io/) | Query endpoint state through a SQL-like interface | Fleet authorization, query scope, and change control |
| [Velociraptor](https://docs.velociraptor.app/) | Authorized endpoint visibility and forensic collection | Access controls, artifact review, collection scope, and audit trails |
| [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) | Visualize behaviors, coverage, and hunt hypotheses | Distinguish technique mapping from proof of detection |

## A simple hunt loop

1. State a testable defensive hypothesis and define the authorized scope.
2. Identify the data sources, time window, and known visibility gaps.
3. Query minimally and preserve the query, assumptions, and timestamps.
4. Validate notable results with independent evidence; record benign explanations.
5. Document findings and confidence, then propose a detection or telemetry improvement.
6. Review impact and privacy; get approval before any response or containment action.

## Portfolio idea

Write a hunt report using synthetic or approved lab data: hypothesis, scope, data sources, query description, findings, false-positive considerations, ATT&CK mapping where relevant, and recommended next steps. Do not publish sensitive logs or real indicators.
