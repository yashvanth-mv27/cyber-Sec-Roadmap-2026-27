# DFIR and Threat Hunting

> Proposed additive chapter. Lab validation status: NOT TESTED.

## Why this matters
Enterprise defenders need repeatable processes, evidence-based decisions and measurable control effectiveness.

## Topics covered
Hypothesis-driven hunting, process chains, persistence, credential theft indicators, lateral movement, evidence preservation, timeline reconstruction, memory/disk triage and incident reporting.

## Practical investigation workflow
1. Define the risk and observable hypothesis.
2. Identify required telemetry, fields, retention and permissions.
3. Collect a safe synthetic event sample and establish a baseline.
4. Correlate events across endpoint, identity, network and cloud when applicable.
5. Evaluate benign alternatives, false positives and missing telemetry.
6. Document severity, affected assets, evidence and escalation criteria.
7. Obtain approval for any disruptive response, then verify and record outcomes.
8. Review detection gaps, costs, lessons learned and ownership.

## Lab deliverables
- Architecture or event-flow diagram
- Sample input and expected output
- Investigation timeline and case notes
- Detection idea or rule pseudocode
- Positive and negative test cases
- Tuning notes, rollback plan and limitations

## Review checklist
- [ ] Primary vendor documentation linked
- [ ] ATT&CK mapping verified where relevant
- [ ] No real credentials or customer records included
- [ ] Detection query executed in a permitted lab
- [ ] False-positive and false-negative limitations recorded
- [ ] Responsible owner and next review date assigned

## Further expansion
Add vendor-specific screenshots, tested KQL/SPL, playbooks, JSON schemas and verified lab evidence in future commits. Do not claim production readiness from documentation alone.
