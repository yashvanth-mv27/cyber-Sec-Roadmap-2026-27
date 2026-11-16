# Scenario-driven SOC alert triage framework

Use this framework for authorized training, tabletop exercises, and real incidents under organizational policy. Scenarios below are fictional and focus on defensive analysis. They intentionally avoid live payloads, real credentials, and instructions to target systems.

## The analyst's question framework: SCOPE

- **S — Signal:** What exactly triggered the alert? Which rule, data source, time range, and fields are present? Is ingestion healthy?
- **C — Context:** Who/what is involved? What are asset criticality, user role, business hours, recent changes, and expected behavior?
- **O — Other evidence:** What related endpoint, identity, network, email, application, and cloud events corroborate or contradict it?
- **P — Potential impact and scope:** What is confirmed, suspected, and unknown? Are other accounts, hosts, data, or services involved?
- **E — Escalation and evidence:** What severity and owner apply? What evidence must be preserved? What action is authorized, by whom, and how will it be verified?

For interviews, structure the response as: **signal → validation → investigation → scope/impact → confidence → escalation/action → documentation → lessons**. State assumptions and missing evidence explicitly.

## Scenario 1: unusual sign-in followed by sensitive activity

**Training alert:** An identity analytic flags an unfamiliar sign-in context. Later audit records show access to a sensitive application. This is a lead, not proof of account compromise.

**Ask:** Are the timestamps and identity records complete? Is the sign-in context actually unusual for this user? Was there an approved travel, device, or network change? Did authentication controls succeed? What application actions followed, and were they expected? Are there corroborating endpoint or identity alerts? What is the scope and data sensitivity?

**Defensive workflow:** validate identity and source data; compare with the user's baseline and approved changes; correlate authentication and application audit events; contact the service owner through approved channels where appropriate; preserve relevant records; escalate based on evidence and impact. Any session revocation or account restriction follows the incident policy and approval model. Verify the effect and coordinate recovery.

**Practice disposition:** classify as benign, suspicious/needs more evidence, or credible incident; include facts, uncertainty, severity rationale, evidence sources, owner, and next action.

## Scenario 2: endpoint detection with uncertain business impact

**Training alert:** An endpoint product reports behavior requiring investigation on a workstation used by a business team.

**Ask:** Is the device identity and timestamp reliable? What process/parent context and signed-software information are available from the console? Is there a related user report, change ticket, or application deployment? Are there related network or identity events? Is the system business-critical? What evidence can be collected under policy?

**Defensive workflow:** validate the alert in the endpoint console; correlate host and user context; compare with known approved activity; use safe, vendor-supported investigation views; preserve evidence as required; consult the system owner and incident lead. Isolation or remediation must follow authorized procedures, with service-impact and rollback considerations. Verify containment and monitor recovery.

## Scenario 3: reported suspicious email

**Training alert:** A user reports a message that asks for an urgent business action and includes a link or attachment.

**Ask:** Is the report genuine and what message identifiers are available? Which recipients received the same message? What do headers and authentication results indicate? Were links opened or attachments handled? Are identity or endpoint events correlated? Is there evidence of account or device impact?

**Defensive workflow:** preserve message metadata; determine recipient scope using authorized mail tools; correlate security verdicts and user/endpoint evidence; follow approved quarantine/removal procedures if warranted; escalate if interaction or compromise is supported; communicate safely with affected users and document results.

## Scenario 4: cloud control-plane change outside expected pattern

**Training alert:** A cloud audit analytic identifies an unusual configuration or permission change.

**Ask:** Which account, principal, resource, and control-plane event are involved? Is the actor expected to perform this change? Is there a change request? Were credentials or a workload identity used? What downstream resources or data could be affected? Are logs complete across relevant accounts/projects/subscriptions?

**Defensive workflow:** verify audit provenance and scope; correlate identity and workload context; consult the cloud owner; preserve audit records; assess exposure and business impact. Revert or restrict access only through approved change/incident authority. Validate the final configuration and monitor for recurrence.

## Scenario 5: correlated network and endpoint anomalies

**Training alert:** A network analytic and an endpoint analytic both produce alerts for the same asset in a short time window.

**Ask:** Do the events share a trustworthy host identity and time basis? Are these known maintenance, testing, or software-update activities? What DNS/proxy/firewall metadata is available? What did the endpoint sensor actually observe? Are neighboring assets affected? What is the confidence and business criticality?

**Defensive workflow:** normalize the timeline, verify source quality, correlate only relevant telemetry, test benign explanations, and document the boundary between observed events and inference. Escalate if independent evidence supports risk. Do not treat a reputation match or single anomaly as conclusive.

## Severity and decision record

Use the organization's severity definitions. A useful decision record includes:

| Field | Record |
|---|---|
| Case identity | Alert/case ID, rule version, analyst, timestamps and timezone |
| Scope | Users, assets, cloud resources, applications, and time range examined |
| Evidence | Source, event identifiers, collection method, provenance, and gaps |
| Assessment | Observed facts, hypotheses, confidence, alternative explanations, impact |
| Decision | Disposition, severity rationale, escalation owner, approvals required |
| Actions | Requested/approved actions, actor, time, result, verification and rollback |
| Follow-up | Customer/user communications, detection tuning, lessons, owner and due date |

## Tabletop exercise scorecard

Score 0–2 for each: evidence validation; hypothesis discipline; scope; impact prioritization; privacy/evidence handling; escalation and approval; communication; safe action choice; verification; learning actions. A low score identifies a process or training improvement, not an individual failure.

## Interview practice prompts

1. An alert is high severity but the telemetry is incomplete. What do you do first and why?
2. Two data sources conflict on event time. How do you construct a reliable timeline?
3. A manager asks you to disable an account immediately, but the available evidence is weak. How do you respond?
4. What evidence would raise or lower your confidence in an identity alert?
5. How do you communicate a likely incident while separating confirmed facts from hypotheses?
6. A SOAR playbook reports success but the target system did not change. How do you detect and handle that failure?
7. What would you include in a post-incident detection improvement?

## Safety note

Use synthetic or explicitly authorized data. Do not paste secrets, personal data, or live incident details into public issues or training materials. Follow your organization's incident command, legal, privacy, and evidence-retention procedures.
