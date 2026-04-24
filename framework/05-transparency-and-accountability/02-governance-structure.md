# 02 — Governance Structure

## Sources

| Source | Reference |
|--------|-----------|
| ETA Framework | Point 3: Be clear who is responsible |
| Data & AI Ethics Framework | Principle 2: Accountability |
| AI Playbook | Principle 10: Organisational alignment and assurance |
| AI Regulation White Paper | Principle 4: Accountability and governance |
| Service Standard | Point 6: Have a multidisciplinary team |
| Turing Institute | Process-Based Governance (PBG) Framework |

## Purpose

The ETA Framework requires ministerial approval for significant automated decisions and senior owners assigned to major processes. The DEF requires clear roles, responsibilities, and governance structures. This section defines the governance framework for the LLM deployment.

## Governance Roles

| Role | Responsibility | Accountability Source |
|------|---------------|---------------------|
| **Minister** | Sign-off for significant automated decisions | ETA Point 3 |
| **Senior Responsible Owner (SRO)** | Overall accountability for the LLM | DEF Principle 2, ETA Point 3 |
| **AI Review Board** | Authorisation and ongoing oversight | AIP Principle 10 |
| **Data Owner** | Data governance and quality | DEF Principle 2 |
| **AI Asset Owner** | Model lifecycle management | DEF Principle 2 |
| **Data Protection Officer** | GDPR compliance | ICO, UK GDPR |
| **Delivery Team** | Day-to-day operation and monitoring | SS Point 6 |

## Governance Requirements

### Accountability chain

- [ ] SRO named and documented
- [ ] Reporting line from delivery team to SRO is clear
- [ ] AI Review Board or programme board established
- [ ] Terms of reference defined for governance bodies
- [ ] Meeting cadence established (minimum quarterly per ETA Point 7)

### Audit and traceability

- [ ] All LLM-informed decisions logged with audit trail
- [ ] Logs include: input, output, timestamp, user, decision made
- [ ] Logs are retained per data retention policy
- [ ] Audit trail is accessible for review and investigation

### Escalation

- [ ] Escalation procedures documented for incidents
- [ ] Thresholds defined for when issues escalate to SRO / Minister
- [ ] Communication plan for significant incidents
- [ ] Documented review and escalation processes (per AIP Principle 10)

### Process-Based Governance (per Turing Institute PBG)

- [ ] Responsible team roles defined at each lifecycle stage
- [ ] Critical workflow intervention points identified
- [ ] Evaluation timeframes set
- [ ] Activity logging protocols in place

### Key principle (per DEF)

> "The public body remains responsible for all data and algorithm-assisted decisions" — even when using third-party LLMs.

## Output

1. Governance structure document with named roles
2. Terms of reference for AI Review Board
3. Escalation procedure
4. Audit trail specification
