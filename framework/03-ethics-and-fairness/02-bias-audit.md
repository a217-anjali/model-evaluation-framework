# 02 — Bias Audit

## Sources

| Source | Reference |
|--------|-----------|
| Data & AI Ethics Framework | Principle 3: Fairness (demographic parity, equalized odds) |
| CDEI AI Assurance Portfolio | Bias Audit technique |
| AISI Evaluations | Societal Impacts risk domain |
| Turing Institute | Fairness (four dimensions) |
| ETA Framework | Point 2: Deliver fair services |

## Purpose

Systematically assess LLM outputs for unfair bias across protected characteristics. The DEF explicitly names demographic parity and equalized odds as fairness metrics. AISI research found LLMs recommend diplomat careers 93% vs 13% based on parental affluence — demonstrating real-world bias risk.

## Bias Dimensions (per Turing Institute)

### 1. Data fairness
- [ ] Training data representativeness assessed across demographics
- [ ] Historical biases in training data identified
- [ ] Data gaps documented (which groups are underrepresented?)

### 2. Design fairness
- [ ] Model architecture does not introduce structural bias
- [ ] Prompt design tested for bias amplification
- [ ] System prompts reviewed for implicit bias

### 3. Outcome fairness
- [ ] LLM outputs compared across demographic groups for the same inputs
- [ ] Demographic parity assessed (equal positive outcome rates across groups)
- [ ] Equalized odds assessed (equal true positive and false positive rates across groups)
- [ ] Disparate impact measured

### 4. Implementation fairness
- [ ] Deployment context does not introduce bias (e.g., who has access to the service)
- [ ] User interface does not create barriers for specific groups
- [ ] Downstream decision-making processes do not amplify LLM bias

## Testing Methods

| Method | Description | Source |
|--------|-------------|--------|
| Counterfactual testing | Change demographic indicators in prompts, compare outputs | AISI |
| Red-team bias testing | Domain experts probe for discriminatory outputs | AISI, ETA |
| Statistical audit | Quantitative analysis of output distributions across groups | CDEI |
| Third-party audit | Independent external bias assessment | CDEI (recommended) |
| Bias bounties | Crowdsource discovery of discriminatory outputs | ETA Point 2 |

## AISI Findings to Test For

Based on AISI evaluation results:
- [ ] Career/opportunity recommendations tested for socioeconomic bias
- [ ] Language and tone consistency tested across racial/ethnic groups
- [ ] Gender stereotyping in generated content assessed
- [ ] Age-related bias in recommendations assessed

## Output

1. Bias audit report with quantitative metrics
2. Identified biases and severity ratings
3. Mitigation plan for each identified bias
4. Schedule for ongoing bias monitoring (see Section 08)
