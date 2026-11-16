# AI for SOC Tools & Guidance

AI-enabled security products can assist with summarization, search, enrichment, and analyst workflows. They do not replace evidence review, approved incident procedures, or human accountability. Product features and names evolve; verify current vendor documentation and data-processing terms.

## Examples to evaluate

| Product / resource | Potential SOC use | Evaluation considerations |
|---|---|---|
| [Intezer](https://intezer.com/) | AI-assisted malware analysis and security operations capabilities | Validate supported workflows, evidence citations, false-positive handling, data residency, and human review |
| [Microsoft Security Copilot](https://learn.microsoft.com/copilot/security/) | AI-assisted security investigation and Microsoft security workflows | Check tenant prerequisites, data protections, licensing, and analyst verification requirements |
| [Google Security Operations](https://cloud.google.com/chronicle/docs) | Security analytics and investigation capabilities, including evolving AI features | Confirm feature availability, access controls, logging, and regional terms |
| [CrowdStrike Charlotte AI](https://www.crowdstrike.com/platform/charlotte-ai/) | AI assistance within security operations workflows | Review product scope, permissions, auditability, data handling, and response safeguards |
| [MITRE ATLAS](https://atlas.mitre.org/) | Knowledge base for AI/ML threat modeling and defensive planning | Use to structure risk analysis; it is not a detection product |
| [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) | Reference for common LLM application risk areas | Apply to authorized design reviews and controlled test environments |

## Safe adoption checklist

1. Choose a narrow, low-risk analyst-assistance use case before automating actions.
2. Use approved data sources and confirm retention, residency, and model-training terms.
3. Keep role-based access, least privilege, audit logs, and clear data boundaries.
4. Require source-linked evidence and analyst verification for summaries and recommendations.
5. Test for inaccurate output, prompt injection, sensitive-data exposure, and failure modes using authorized test data.
6. Keep high-impact response actions behind explicit human approval and established incident procedures.
7. Measure quality, time saved, missed context, false positives, and user feedback; maintain a rollback path.

> Never send secrets, personal data, customer logs, or confidential incident details to an AI service unless that service and use are explicitly approved by your organization.
