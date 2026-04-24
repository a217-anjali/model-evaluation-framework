# 02 — Safety and Security

## Sources

| Source | Reference |
|--------|-----------|
| AI Playbook | Principle 3: Secure AI implementation |
| AI Regulation White Paper | Principle 1: Safety, security and robustness |
| Technology Code of Practice | Point 6: Make things secure |
| Service Standard | Point 9: Create a secure service which protects users' privacy |
| AISI Evaluations | Safeguards evaluation, Agent evaluations |
| ETA Framework | Point 1: Test to avoid unintended outcomes |

## Purpose

LLMs introduce specific security threats beyond traditional software. The AI Playbook identifies data poisoning, prompt injection, hallucinations, and perturbation attacks as AI-specific threats. AISI found that basic prompting techniques can bypass LLM safeguards, and sophisticated jailbreaks require only a couple of hours.

## AI-Specific Threats (per AI Playbook Principle 3)

| Threat | Description | Test Method |
|--------|-------------|-------------|
| Prompt injection | Malicious prompts that override system instructions | Adversarial prompt testing |
| Data leakage | LLM reveals training data or user data from other sessions | Extraction testing |
| Data poisoning | Compromised training/fine-tuning data | Training data audit |
| Jailbreaking | Bypassing safety guardrails | Red-team jailbreak testing |
| Perturbation attacks | Small input changes causing large output changes | Robustness testing |
| Hallucination as security risk | Fabricated URLs, code, or instructions that could cause harm | Hallucination security audit |
| Indirect prompt injection | Malicious content in retrieved documents (RAG) | RAG pipeline testing |

## Testing Requirements

### Prompt injection resistance

- [ ] Test direct prompt injection (overriding system prompts)
- [ ] Test indirect prompt injection (malicious content in external data)
- [ ] Test with known jailbreak techniques
- [ ] Test escalation paths (can the model be gradually manipulated?)
- [ ] AISI finding: basic techniques bypass safeguards — testing must go beyond basics

### Data leakage prevention

- [ ] Test whether the model reveals system prompts
- [ ] Test whether the model reveals other users' data
- [ ] Test whether the model reveals training data containing personal information
- [ ] Test output filtering for sensitive data patterns (NI numbers, addresses, etc.)

### Content safety

- [ ] Content filtering implemented and tested
- [ ] Output validation checks in place
- [ ] Harmful content generation tested and blocked
- [ ] Model refuses inappropriate requests reliably

### Infrastructure security

- [ ] Comply with Government Cyber Security Strategy (2022-2030)
- [ ] Follow CDDO "Secure by Design" principles
- [ ] Meet the Cyber Security Standard
- [ ] API authentication and access controls in place
- [ ] Logging and monitoring of all LLM interactions
- [ ] Rate limiting to prevent abuse

### AISI Agent evaluation (if applicable)

If the LLM has autonomous capabilities (tool use, web access, etc.):
- [ ] Assess autonomous action scope and limits
- [ ] Test for unintended tool use
- [ ] Evaluate ability to be constrained when instructed
- [ ] Test for deceptive behaviour

## Output

1. Security assessment report
2. Penetration test results (AI-specific)
3. Threat model documentation
4. Security control mapping
