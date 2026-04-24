# 04 — Environmental Impact

## Sources

| Source | Reference |
|--------|-----------|
| Data & AI Ethics Framework | Principle 7: Environmental Sustainability |
| Technology Code of Practice | Point 12: Make your technology sustainable |
| Turing Institute SAFE-D | Sustainability |

## Purpose

LLMs have significant computational and energy costs. The DEF (Principle 7) requires that public sector AI deployments minimise environmental impact and support long-term planetary wellbeing. TCoP Point 12 makes sustainability a criterion for spend control approvals.

## Requirements

### Compute and energy assessment

- [ ] Estimated inference costs per query (tokens, compute time)
- [ ] Estimated daily/monthly query volume
- [ ] Total energy consumption estimated for planned usage
- [ ] Carbon footprint calculated (considering data centre location and energy mix)
- [ ] Cost-per-query documented

### Sustainable choices

- [ ] Assessed whether a smaller, more efficient model could achieve the same outcome
- [ ] Considered model distillation or fine-tuning to reduce inference cost
- [ ] Evaluated on-premise vs. cloud hosting environmental tradeoff
- [ ] Considered caching strategies to reduce redundant inference
- [ ] Batch processing evaluated where real-time inference is not required

### Proportionality

- [ ] Environmental cost is proportionate to the public benefit delivered
- [ ] Comparison made with the environmental cost of the non-AI alternative

## Output

Environmental impact assessment documenting:
1. Estimated energy consumption and carbon footprint
2. Sustainable design choices made
3. Proportionality justification
