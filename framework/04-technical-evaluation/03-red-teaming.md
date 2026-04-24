# 03 — Red-Teaming

## Sources

| Source | Reference |
|--------|-----------|
| AISI Evaluations | Red-Teaming technique, Human Uplift Evaluations |
| ETA Framework | Point 1: Test to avoid unintended outcomes (red team testing) |
| CDEI AI Assurance Portfolio | Performance Testing |

## Purpose

The ETA Framework requires "red team testing assuming systems can cause harm" with "independent qualified testers." AISI methodology uses domain experts who spend time interacting with models to test capabilities and break safeguards.

## AISI Red-Teaming Methodology (Adapted)

### Step 1: Scope definition

- [ ] Define the risk domains to test (from AISI's four categories):
  - Misuse (can the LLM help bad actors?)
  - Societal impacts (bias, discrimination, psychological effects)
  - Autonomous behaviour (if applicable)
  - Safeguard robustness (can guardrails be bypassed?)
- [ ] Identify domain-specific risks for this particular deployment

### Step 2: Team assembly

- [ ] Recruit domain experts (not just security testers)
- [ ] Include diverse perspectives (demographic, professional, technical)
- [ ] Testers must be independent of the development team (per ETA Point 1)
- [ ] Brief testers on the LLM's intended use case and context

### Step 3: Testing execution

- [ ] Testers interact with the LLM attempting to:
  - Produce harmful or inappropriate outputs
  - Generate biased or discriminatory responses
  - Bypass safety guardrails
  - Extract sensitive information
  - Produce outputs that would mislead citizens
  - Generate factually incorrect advice on the service domain
- [ ] Test with realistic user scenarios, not just adversarial prompts
- [ ] Document all successful and unsuccessful attempts

### Step 4: Human uplift evaluation (per AISI)

- [ ] Compare what a person can achieve with the LLM vs. without it
- [ ] Assess whether the LLM provides meaningful uplift for harmful activities
- [ ] Focus on the specific domain context (e.g., can it help someone game a benefits system?)

### Step 5: Reporting

- [ ] Catalogue all vulnerabilities found
- [ ] Severity rating for each finding
- [ ] Reproducibility assessment
- [ ] Remediation recommendations

## ETA Framework Requirements

- [ ] Testing assumes the system is capable of causing harm (ETA Point 1)
- [ ] Testing is conducted before deployment, not after
- [ ] Testers are independent and qualified
- [ ] Results inform the go/no-go decision (see Section 07)

## Output

1. Red-team test report with findings
2. Vulnerability catalogue with severity ratings
3. Remediation plan
4. Residual risk assessment
