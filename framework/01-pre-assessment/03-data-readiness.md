# 03 — Data Readiness Assessment

## Sources

| Source | Reference |
|--------|-----------|
| AI Procurement Guidelines | Consideration 3: Data assessment |
| Data & AI Ethics Framework | Principle 4: Privacy |
| Data & AI Ethics Framework | Principle 3: Fairness (data representativeness) |
| Turing Institute SAFE-D | Data Stewardship |
| ETA Framework | Point 4: Handle data safely |
| ICO AI Guidance | Data minimisation, lawful basis |

## Purpose

Assess whether the data environment is ready for an LLM deployment — covering data quality, governance, bias risk, and legal basis for processing.

## Requirements

### Data governance

- [ ] Data ownership and stewardship are clearly assigned
- [ ] Data sharing agreements are in place where needed
- [ ] Legal basis for data processing is identified (UK GDPR Article 6)
- [ ] Special category data processing conditions are met if applicable (Article 9)
- [ ] Data retention policies are defined
- [ ] Data provenance is documented

### Data quality

- [ ] Input data quality has been assessed (completeness, accuracy, timeliness)
- [ ] Training data representativeness has been evaluated across demographics
- [ ] Known data gaps and limitations are documented
- [ ] Data pre-processing steps are recorded

### Bias in data (per DEF Principle 3)

Four types of data bias to assess:
- [ ] **Representation bias** — Are all relevant groups adequately represented?
- [ ] **Societal bias** — Does the data reflect existing societal inequalities?
- [ ] **Aggregation bias** — Are distinct groups inappropriately combined?
- [ ] **Measurement bias** — Are the metrics/proxies appropriate and unbiased?

### Data minimisation (per ICO guidance)

- [ ] Only data necessary and proportionate to the purpose is processed
- [ ] Privacy-enhancing technologies considered (anonymisation, pseudonymisation, synthetic data)
- [ ] Personal data in prompts is minimised or stripped where possible

## Output

A data readiness report covering:
1. Data governance status
2. Data quality assessment
3. Bias risk assessment across four dimensions
4. Data minimisation measures
5. Gaps and remediation plan
