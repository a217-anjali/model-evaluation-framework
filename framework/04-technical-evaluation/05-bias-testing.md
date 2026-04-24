# 05 — Output Bias Testing

## Sources

| Source | Reference |
|--------|-----------|
| AISI Evaluations | Societal Impacts: representational bias, allocative bias |
| CDEI AI Assurance Portfolio | Bias Audit technique |
| Data & AI Ethics Framework | Principle 3: Fairness (demographic parity, equalized odds) |
| Turing Institute | Four dimensions of fairness |
| Service Standard | Point 5: Make sure everyone can use the service |

## Purpose

Technical testing of LLM outputs for bias, complementing the broader bias audit in Section 03. This section focuses on the quantitative, technical measurement of output fairness.

## AISI Empirical Findings

The following real-world biases have been found in LLMs by AISI:
- Career recommendations differing 93% vs 13% based on parental affluence
- Image models perpetuating stereotypes despite quality improvements
- Socioeconomic bias in opportunity recommendations

These findings should inform test design.

## Testing Protocol

### Counterfactual testing

- [ ] Create paired prompts identical except for demographic indicators
- [ ] Test across all nine protected characteristics
- [ ] Measure output differences quantitatively
- [ ] Flag any statistically significant disparities

### Fairness metrics (per DEF Principle 3)

| Metric | Definition | Threshold |
|--------|-----------|-----------|
| Demographic parity | Equal positive outcome rates across groups | Define per use case |
| Equalized odds | Equal true positive and false positive rates across groups | Define per use case |
| Disparate impact | Ratio of positive outcomes between groups (4/5ths rule) | Ratio > 0.8 |
| Predictive parity | Equal precision across groups | Define per use case |

### Domain-specific bias tests

- [ ] Test for bias in the specific service context (e.g., benefits advice, health information)
- [ ] Test with domain-specific scenarios where bias is most impactful
- [ ] Test with intersectional identities (e.g., race + gender combined)
- [ ] Test tone and formality consistency across demographic groups
- [ ] Test for stereotyping in open-ended responses

### Accessibility bias

- [ ] Test output readability across different literacy levels
- [ ] Test compatibility with assistive technologies
- [ ] Test with different English language proficiencies
- [ ] Test Welsh language capability if applicable

## Output

1. Quantitative bias test results with fairness metrics
2. Counterfactual test results across protected characteristics
3. Domain-specific bias findings
4. Comparison against defined fairness thresholds
