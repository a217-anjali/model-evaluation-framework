# 01 — Problem Definition: Is an LLM the Right Solution?

## Sources

| Source | Reference |
|--------|-----------|
| AI Playbook | Principle 6: Select the right tool for the job |
| AI Procurement Guidelines | Consideration 6: Problem-focused requirements |
| Service Standard | Point 11: Choose the right tools and technology |
| Service Standard | Point 2: Solve a whole problem for users |
| GenAI Framework / AI Playbook | Inappropriate use cases for generative AI |

## Purpose

Before evaluating any LLM, determine whether an LLM is genuinely the right solution for the problem. The AI Playbook (Principle 6) explicitly states: not all problems require AI.

## Assessment Questions

### Is the problem well-suited to an LLM?

- [ ] Can you clearly articulate the user problem without referencing technology?
- [ ] Have you considered non-AI alternatives (rules-based systems, search, human processes)?
- [ ] Does the problem require natural language understanding or generation?
- [ ] Is approximate/probabilistic output acceptable, or is verified accuracy required?
- [ ] Can you define measurable success criteria for the LLM's performance?

### Inappropriate use cases (per AI Playbook)

The following scenarios are flagged as inappropriate for generative AI:

- [ ] Fully automated high-impact decisions with no human oversight
- [ ] Safety-critical applications where errors could cause physical harm
- [ ] Low-latency requirements where model inference is too slow
- [ ] Contexts requiring verifiable, citation-level accuracy
- [ ] High-explainability requirements where "black box" outputs are unacceptable
- [ ] Limited-data domains where the model has insufficient training coverage

### Service Standard alignment

- **SS Point 2**: Does the LLM solve a whole problem, or does it only address part of the user journey while creating new pain points?
- **SS Point 11**: Have you evaluated whether simpler technology would achieve the same outcome?

## Output

A documented decision record stating:
1. The user problem being addressed
2. Alternative solutions considered and why they were rejected
3. Why an LLM is the appropriate tool
4. Known limitations and risks of using an LLM for this purpose
5. Measurable success criteria
