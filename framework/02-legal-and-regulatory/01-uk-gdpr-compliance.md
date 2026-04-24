# 01 — UK GDPR Compliance

## Sources

| Source | Reference |
|--------|-----------|
| ICO AI Guidance | Full AI and data protection guidance |
| ETA Framework | Point 4: Handle data safely |
| Data & AI Ethics Framework | Principle 4: Privacy |
| AI Playbook | Principle 2: Lawful, ethical, responsible use |
| Technology Code of Practice | Point 7: Make privacy integral |
| Service Standard | Point 9: Create a secure service which protects users' privacy |

## Purpose

Any LLM processing personal data in the UK public sector must comply with the UK GDPR and Data Protection Act 2018. This is a legal obligation, not guidance.

## Requirements

### Lawful basis (Article 6)

- [ ] A lawful basis for processing personal data is identified and documented
- [ ] If relying on consent, it is freely given, specific, informed, and unambiguous
- [ ] If relying on public task (Article 6(1)(e)), the specific legal power is identified
- [ ] The lawful basis is recorded in the Record of Processing Activities (ROPA)

### Special category data (Article 9)

- [ ] If processing special category data (race, health, religion, etc.), an Article 9 condition is identified
- [ ] Appropriate policy document is in place if relying on substantial public interest

### Automated decision-making (Article 22)

- [ ] Assessment completed: does the LLM make solely automated decisions with legal or significant effects?
- [ ] If yes: explicit consent obtained, or processing is necessary for a contract, or authorised by law
- [ ] Meaningful human review is available (not rubber-stamping)
- [ ] Data subjects are informed of automated decision-making
- [ ] Right to contest the decision is provided

### Data Protection Impact Assessment (DPIA)

Required when AI processing is likely to result in a high risk to individuals. ICO states DPIAs are required for:
- [ ] Systematic and extensive profiling with significant effects
- [ ] Large-scale processing of special category data
- [ ] Innovative use of new technologies (LLM deployments typically qualify)

DPIA must assess:
- [ ] Necessity and proportionality of processing
- [ ] Risks to individuals' rights and freedoms
- [ ] Measures to mitigate those risks
- [ ] Whether to consult the ICO (if high residual risk remains)

### Individual rights

The following rights apply to LLM processing:
- [ ] Right to be informed (privacy notice covers AI processing)
- [ ] Right of access (individuals can request data used in AI systems)
- [ ] Right to rectification (inaccurate training/input data can be corrected)
- [ ] Right to erasure (where applicable)
- [ ] Right not to be subject to solely automated decisions (Article 22)
- [ ] Right to meaningful human review of automated decisions
- [ ] Right to challenge/contest automated decisions

### Privacy by design (per TCoP Point 7, SS Point 9)

- [ ] Data protection built in from the start, not bolted on
- [ ] Default settings are the most privacy-protective
- [ ] Personal data in prompts is minimised
- [ ] LLM outputs are checked for inadvertent disclosure of personal data
- [ ] Model cannot be prompted to reveal training data containing personal information

## Output

1. Completed DPIA (use template in 09-templates/)
2. Updated privacy notice
3. Article 22 assessment
4. Documented lawful basis
