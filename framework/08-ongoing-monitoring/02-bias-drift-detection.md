# 02 — Bias Drift Detection

## Sources

| Source | Reference |
|--------|-----------|
| Data & AI Ethics Framework | Principle 3: Fairness (ongoing) |
| CDEI AI Assurance Portfolio | Impact Evaluation (post-deployment) |
| Turing Institute FAST | Fairness: maintained over time |
| AISI Evaluations | Longitudinal capability tracking |

## Purpose

Bias is not static. Model behaviour can drift over time due to updated model versions, changing data distributions, or evolving user patterns. AISI research showed LLM capabilities changed dramatically over just two years (microbiology accuracy from 5% to 60%). Continuous fairness monitoring is essential.

## Monitoring Requirements

### Ongoing fairness metrics

- [ ] Demographic parity tracked across protected characteristics
- [ ] Equalized odds monitored over time
- [ ] Counterfactual tests repeated at defined intervals
- [ ] New bias patterns investigated as they emerge

### Triggers for investigation

- [ ] Fairness metric deviation beyond defined threshold
- [ ] User complaints related to bias or discrimination
- [ ] Model version updates by the supplier
- [ ] Changes in user demographics or usage patterns
- [ ] External reports of bias in the same model

### Model update monitoring

- [ ] Supplier notifies of model updates (per contract requirements)
- [ ] Bias testing repeated after each significant model update
- [ ] Performance comparison: pre-update vs. post-update
- [ ] Re-evaluation against all fairness criteria

### Reporting

- [ ] Bias monitoring results included in quarterly reviews
- [ ] Significant findings escalated to SRO
- [ ] EIA updated if new impacts identified
- [ ] ATRS record updated if system behaviour changes

## Output

1. Bias monitoring dashboard
2. Alert thresholds for fairness metrics
3. Investigation and escalation process
