# 04 — Incident Response

## Sources

| Source | Reference |
|--------|-----------|
| AI Playbook | Principle 4: Intervention strategies to prevent harmful effects |
| AI Regulation White Paper | Principle 1: Safety, security and robustness |
| Service Standard | Point 14: Operate a reliable service |

## Purpose

Define what happens when the LLM produces harmful outputs, experiences a security breach, or fails. The AI Playbook requires intervention strategies, and the Service Standard requires reliable operation including failure planning.

## Incident Categories

| Category | Severity | Example |
|----------|----------|---------|
| **Critical** | Immediate harm to citizens | Discriminatory decision, personal data leak, dangerous advice |
| **High** | Significant service degradation | Widespread inaccurate outputs, security breach, extended outage |
| **Medium** | Limited impact | Increased hallucination rate, performance degradation, isolated errors |
| **Low** | Minimal impact | Minor quality issues, cosmetic problems |

## Response Procedures

### Immediate response (Critical / High)

- [ ] LLM can be taken offline immediately (kill switch exists and is tested)
- [ ] Fallback to non-AI service path activated
- [ ] Affected users identified and notified
- [ ] SRO and relevant governance bodies informed
- [ ] ICO notified within 72 hours if personal data breach (per UK GDPR)

### Investigation

- [ ] Root cause analysis conducted
- [ ] Scope of impact determined
- [ ] Audit logs reviewed
- [ ] Supplier engaged if third-party model

### Remediation

- [ ] Fix implemented and tested
- [ ] Affected decisions reviewed and corrected where necessary
- [ ] Citizens who received incorrect information or decisions are contacted
- [ ] Monitoring enhanced to detect recurrence

### Post-incident

- [ ] Incident report completed
- [ ] Lessons learned documented
- [ ] Framework/processes updated if needed
- [ ] Reported at next quarterly review

## Fallback mechanisms (SS Point 14)

- [ ] Non-AI service path exists and is tested regularly
- [ ] Staff are trained to operate without the LLM
- [ ] Switchover procedure is documented and rehearsed
- [ ] Vendor API outage plan exists (if using third-party LLM)

## Output

1. Incident response plan
2. Escalation matrix
3. Fallback procedure
4. Incident report template
