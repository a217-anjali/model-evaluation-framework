# 01 — Accuracy and Hallucination Testing

## Sources

| Source | Reference |
|--------|-----------|
| AI Playbook | Principle 1: Understand AI and its limitations (hallucination, no true reasoning) |
| AISI Evaluations | Automated Capability Assessments |
| Service Standard | Point 10: Define what success looks like and publish performance data |
| CDEI AI Assurance Portfolio | Performance Testing |

## Purpose

The AI Playbook explicitly identifies hallucination — where models prioritise plausibility over factual accuracy — as a core LLM limitation. This must be quantified before deployment.

## Known LLM Limitations (per AI Playbook)

1. **Hallucination** — Models generate plausible but false information
2. **No true reasoning** — Models predict next tokens, not reasoned conclusions
3. **Bias reproduction** — Models replicate biased patterns from training data
4. **No domain expertise** — Insufficient accuracy in specialised fields without specific training
5. **Limited context awareness** — Models lack real-world understanding
6. **Explainability challenges** — Neural networks operate as "black boxes"

## Testing Requirements

### Factual accuracy

- [ ] Test against a curated dataset of known-correct answers in the target domain
- [ ] Measure accuracy rate (correct responses / total responses)
- [ ] Identify categories where accuracy is lowest
- [ ] Compare accuracy with and without retrieval augmentation (RAG)
- [ ] Test with domain expert review of a statistically significant sample

### Hallucination rate

- [ ] Measure frequency of fabricated facts, citations, or statistics
- [ ] Test for confident-sounding but incorrect responses
- [ ] Measure hallucination rate under different prompt styles
- [ ] Test edge cases and rare scenarios (where hallucination is most likely)
- [ ] Assess whether users can identify hallucinated content

### Domain-specific accuracy

- [ ] Test with domain experts in the specific public sector context
- [ ] Assess accuracy on domain terminology and processes
- [ ] Test with recent information (post-training cutoff)
- [ ] Assess performance degradation on niche or uncommon queries

### Reasoning and consistency

- [ ] Test logical consistency across related queries
- [ ] Test mathematical/numerical accuracy where relevant
- [ ] Assess whether the model admits uncertainty appropriately
- [ ] Test for contradictions when the same question is asked differently

## Metrics (per SS Point 10)

| Metric | Description | Target |
|--------|-------------|--------|
| Accuracy rate | % of factually correct responses | Define per use case |
| Hallucination rate | % of responses containing fabricated information | Define per use case |
| Domain accuracy | % correct on domain-specific test set | Define per use case |
| Uncertainty calibration | Does the model express doubt when it should? | Qualitative assessment |
| Refusal rate | % of queries appropriately refused | Define per use case |

## Output

1. Accuracy and hallucination test report with quantitative metrics
2. Domain-specific accuracy assessment
3. Performance thresholds defined for go/no-go decision
4. Published performance data (per SS Point 10)
