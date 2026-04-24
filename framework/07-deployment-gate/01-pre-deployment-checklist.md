# 01 — Pre-Deployment Checklist

## Sources

| Source | Reference |
|--------|-----------|
| ETA Framework | All 7 points — this is the primary deployment gate |
| CDEI AI Assurance Portfolio | Conformity Assessment |

## Purpose

This is the go/no-go gate before the LLM goes live. It consolidates the ETA Framework's 7-point checklist into a single sign-off document. All items must be completed — or explicitly risk-accepted with justification — before deployment.

## The 7-Point Gate (per ETA Framework)

### Point 1: Test to avoid unintended outcomes

- [ ] Staged prototyping completed
- [ ] Red-team testing conducted (see 04-technical/03-red-teaming)
- [ ] DPIA completed (see 02-legal/01-uk-gdpr-compliance)
- [ ] EIA completed (see 03-ethics/03-equality-impact-assessment)
- [ ] Independent, qualified testers used
- [ ] Testing assumed the system could cause harm

### Point 2: Deliver fair services for all users

- [ ] Bias audit completed (see 03-ethics/02-bias-audit)
- [ ] Bias testing across protected characteristics completed (see 04-technical/05-bias-testing)
- [ ] Multidisciplinary, diverse team assembled
- [ ] Diverse, quality datasets used
- [ ] Bias and safety bounties considered

### Point 3: Be clear who is responsible

- [ ] SRO named (see 05-transparency/02-governance-structure)
- [ ] Governance structure documented
- [ ] Ministerial sign-off obtained (if significant automated decisions)
- [ ] Full auditability in place
- [ ] Accountability embedded in existing governance

### Point 4: Handle data safely

- [ ] UK GDPR compliance confirmed (see 02-legal/01-uk-gdpr-compliance)
- [ ] Lawful basis documented
- [ ] DPIA completed
- [ ] Data protection by design implemented
- [ ] Article 22 assessment completed (if automated decisions)

### Point 5: Help users understand how systems impact them

- [ ] Plain-language explanation published (see 05-transparency/05-plain-language)
- [ ] ATRS record completed and published (see 05-transparency/01-atrs-record)
- [ ] Contestability mechanisms in place (see 05-transparency/04-contestability)
- [ ] Accountable officer designated for citizen queries
- [ ] Feedback loops accessible

### Point 6: Ensure legal compliance

- [ ] Legal advisor sign-off obtained
- [ ] UK GDPR compliance confirmed
- [ ] Equality Act 2010 compliance confirmed
- [ ] Human rights screening completed (see 02-legal/03-human-rights)
- [ ] Sector-specific regulations addressed (see 02-legal/04-sector-specific)

### Point 7: Build something future-proof

- [ ] Quarterly review schedule established (see 08-monitoring/03-quarterly-review)
- [ ] Continuous monitoring plan in place (see 08-monitoring/01-performance-monitoring)
- [ ] Bias drift detection planned (see 08-monitoring/02-bias-drift-detection)
- [ ] Incident response procedures documented (see 08-monitoring/04-incident-response)
- [ ] End-of-life plan documented (see 08-monitoring/05-end-of-life)

## Sign-Off

| Role | Name | Date | Decision (Go / No-Go / Conditional) |
|------|------|------|--------------------------------------|
| SRO | | | |
| Legal Advisor | | | |
| Data Protection Officer | | | |
| Technical Lead | | | |
| Minister (if applicable) | | | |

## Output

Signed pre-deployment checklist with go/no-go decision.
