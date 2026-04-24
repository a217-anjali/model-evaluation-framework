# 03 — Human Oversight

## Sources

| Source | Reference |
|--------|-----------|
| AI Playbook | Principle 4: Meaningful human control at the right stage |
| ETA Framework | Point 3: Be clear who is responsible |
| ICO AI Guidance | Article 22: Right to meaningful human review |
| AI Regulation White Paper | Principle 4: Accountability and governance |

## Purpose

The AI Playbook (Principle 4) requires "meaningful human control at the right stage" — not just nominal human oversight but genuine human intervention at critical decision points. The ICO requires that automated decisions with legal or significant effects include meaningful human review.

## Human-in-the-Loop Design

### Levels of human oversight

| Level | Description | When to Use |
|-------|-------------|-------------|
| **Full automation** | LLM operates without human review | Low-risk, non-consequential tasks only (e.g., internal summarisation) |
| **Human-on-the-loop** | Human monitors LLM outputs, intervenes when needed | Medium-risk tasks (e.g., draft correspondence for review) |
| **Human-in-the-loop** | Human reviews every LLM output before action | High-risk tasks (e.g., advice to citizens, case decisions) |
| **Human-only** | LLM not used | Highest-risk decisions, safety-critical contexts |

### Requirements

- [ ] Oversight level defined for each LLM use case
- [ ] Justification documented for the chosen oversight level
- [ ] Higher-risk decisions receive more human oversight (proportionate approach)
- [ ] Human reviewers have the authority and ability to override LLM outputs
- [ ] Human reviewers are trained on LLM limitations

### Meaningful review (per ICO)

"Meaningful" human review means:
- [ ] The reviewer has the authority to change the decision
- [ ] The reviewer has the competence to assess the LLM output
- [ ] The reviewer has access to relevant information beyond the LLM output
- [ ] The review is not a rubber-stamp exercise
- [ ] Sufficient time is allowed for genuine consideration

### AI Playbook Principle 4 requirements

- [ ] Human validation of high-risk decisions influenced by AI
- [ ] Intervention strategies documented to prevent harmful effects
- [ ] Full product testing before deployment
- [ ] Robust assurance and regular checks of live systems
- [ ] User feedback mechanisms that trigger human review
- [ ] Real-time human review available where instant responses are required

## Output

1. Human oversight model for each LLM use case
2. Reviewer role descriptions and competency requirements
3. Override procedures
4. Training plan for human reviewers
