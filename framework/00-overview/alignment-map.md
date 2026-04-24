# Master Alignment Map

This document shows exactly how every framework section traces back to UK government sources.

## Legend

- **SS** = Service Standard (14 points) [S1]
- **SM** = Service Manual [S2]
- **AIP** = AI Playbook (10 principles) [S3]
- **DEF** = Data & AI Ethics Framework (7 principles) [S4]
- **ETA** = Ethics, Transparency & Accountability Framework (7 points) [S5]
- **WP** = AI Regulation White Paper (5 principles) [S6]
- **ATRS** = Algorithmic Transparency Recording Standard [S7]
- **PROC** = AI Procurement Guidelines (10 considerations) [S8]
- **AISI** = AI Safety Institute Evaluations [S9]
- **TCoP** = Technology Code of Practice (13 points) [S10]
- **CDEI** = CDEI AI Assurance Portfolio [S11]
- **TURING** = Turing Institute FAST/SAFE-D [S12]
- **ICO** = ICO AI Guidance [S13]

---

## Section 01: Pre-Assessment

| File | Requirement | Source(s) |
|------|------------|-----------|
| 01-problem-definition.md | Assess whether an LLM is the right solution | AIP Principle 6, PROC Consideration 6, SS Point 11 |
| 02-user-needs-research.md | Understand user needs before building | SS Point 1, SS Point 2, SM User Research, AIP Principle 1 |
| 03-data-readiness.md | Assess data quality, bias, governance | PROC Consideration 3, DEF Principle 4, TURING Data Stewardship |
| 04-team-composition.md | Assemble multidisciplinary team | SS Point 6, ETA Point 2, PROC Consideration 2, AIP Principle 9 |

## Section 02: Legal & Regulatory

| File | Requirement | Source(s) |
|------|------------|-----------|
| 01-uk-gdpr-compliance.md | Lawful basis, Article 22, DPIAs | ICO AI Guidance, ETA Point 4, DEF Principle 4, AIP Principle 2 |
| 02-equality-act.md | Protected characteristics, EIAs, PSED | ETA Point 2, ETA Point 6, DEF Principle 3, WP Principle 3 |
| 03-human-rights.md | Human rights implications | ETA Point 6, WP Principle 3, AIP Principle 2 |
| 04-sector-specific-regulation.md | FCA, CQC, Ofsted etc. | WP (context-specific regulation), AIP Principle 10 |

## Section 03: Ethics & Fairness

| File | Requirement | Source(s) |
|------|------------|-----------|
| 01-data-ethics-framework.md | Apply 7 ethical principles | DEF (all 7 principles), AIP Principle 2 |
| 02-bias-audit.md | Test for demographic parity, equalized odds | DEF Principle 3, CDEI Bias Audit, AISI Societal Impacts, TURING Fairness |
| 03-equality-impact-assessment.md | Assess impact on protected groups | ETA Point 2, DEF Principle 3, SS Point 5 |
| 04-environmental-impact.md | Compute costs, carbon footprint | DEF Principle 7, TCoP Point 12, TURING Sustainability |

## Section 04: Technical Evaluation

| File | Requirement | Source(s) |
|------|------------|-----------|
| 01-accuracy-and-hallucination.md | Factual accuracy, hallucination rates | AIP Principle 1, AISI Automated Assessments, SS Point 10 |
| 02-safety-and-security.md | Prompt injection, data leakage, poisoning | AIP Principle 3, TCoP Point 6, WP Principle 1, SS Point 9 |
| 03-red-teaming.md | Adversarial testing by domain experts | AISI Red-Teaming, ETA Point 1, CDEI Performance Testing |
| 04-performance-benchmarks.md | Domain-specific task performance | AISI Automated Assessments, CDEI Performance Testing, SS Point 10 |
| 05-bias-testing.md | Output fairness across demographics | AISI Societal Impacts, CDEI Bias Audit, DEF Principle 3, TURING Fairness |
| 06-explainability.md | Can outputs be understood by users? | WP Principle 2, DEF Principle 1, TURING Explainability, SS Point 4 |

## Section 05: Transparency & Accountability

| File | Requirement | Source(s) |
|------|------------|-----------|
| 01-atrs-record.md | Publish algorithmic transparency record | ATRS (mandatory), AIP Principle 7, DEF Principle 1 |
| 02-governance-structure.md | SRO, review boards, escalation | ETA Point 3, DEF Principle 2, AIP Principle 10, SS Point 6 |
| 03-human-oversight.md | Human-in-the-loop at critical points | AIP Principle 4, ETA Point 3, ICO Article 22, WP Principle 4 |
| 04-contestability.md | Citizen challenge and redress | WP Principle 5, ETA Point 5, ICO Individual Rights, SS Point 3 |
| 05-plain-language-explanation.md | Accessible public descriptions | ETA Point 5, DEF Principle 1, WP Principle 2, SS Point 4 |

## Section 06: Procurement

| File | Requirement | Source(s) |
|------|------------|-----------|
| 01-supplier-assessment.md | Vendor ethics, capability, transparency | PROC Considerations 5/9, AIP Principle 8, TCoP Point 11 |
| 02-contract-requirements.md | ATRS, knowledge transfer, IP, liability | PROC Consideration 10, DEF Third-Party Requirements, ATRS |
| 03-build-vs-buy.md | Open source vs proprietary evaluation | TCoP Points 3/4, PROC Consideration 8, SS Point 12 |

## Section 07: Deployment Gate

| File | Requirement | Source(s) |
|------|------------|-----------|
| 01-pre-deployment-checklist.md | 7-point go/no-go gate | ETA (all 7 points), CDEI Conformity Assessment |
| 02-service-assessment.md | Meet the 14-point Service Standard | SS (all 14 points), TCoP Point 13, SM Service Assessments |
| 03-ministerial-sign-off.md | Approval for significant automated decisions | ETA Point 3, AIP Principle 10 |

## Section 08: Ongoing Monitoring

| File | Requirement | Source(s) |
|------|------------|-----------|
| 01-performance-monitoring.md | Track KPIs, accuracy, drift | ETA Point 7, SS Point 10, AIP Principle 5, TURING Sustainability |
| 02-bias-drift-detection.md | Monitor fairness over time | DEF Principle 3, CDEI Impact Evaluation, TURING Fairness |
| 03-quarterly-review.md | Formal review cycle | ETA Point 7, AIP Principle 5 |
| 04-incident-response.md | When things go wrong | AIP Principle 4, WP Principle 1, SS Point 14 |
| 05-end-of-life.md | Decommissioning plan | PROC Consideration 10, CDEI Lifecycle (Retirement stage) |

## Section 09: Templates

| Template | Required By |
|----------|------------|
| dpia-template.md | ICO AI Guidance, ETA Point 4, DEF Principle 4 |
| eia-template.md | ETA Point 2, DEF Principle 3, Equality Act 2010 |
| atrs-template.md | ATRS (mandatory for government departments, Dec 2024) |
| risk-assessment-template.md | CDEI Risk Assessment, ETA Point 1 |
| evaluation-scorecard.md | Consolidated scoring against all frameworks |

---

## Service Standard: Full 14-Point Mapping

| SS Point | Description | Framework Section(s) |
|----------|------------|---------------------|
| 1. Understand users and their needs | User research before building | 01-pre-assessment/02-user-needs-research |
| 2. Solve a whole problem for users | LLM fits the full user journey | 01-pre-assessment/01-problem-definition |
| 3. Joined up experience across channels | Consistency between AI and non-AI channels | 05-transparency/04-contestability |
| 4. Make the service simple to use | AI reduces complexity, not adds it | 04-technical/06-explainability, 05-transparency/05-plain-language |
| 5. Make sure everyone can use the service | Accessibility, no bias exclusion, WCAG 2.2 | 03-ethics/03-equality-impact-assessment |
| 6. Have a multidisciplinary team | Include ethicists, domain experts, not just tech | 01-pre-assessment/04-team-composition, 05-transparency/02-governance |
| 7. Use agile ways of working | Iterative development, phased rollout | 07-deployment/02-service-assessment |
| 8. Iterate and improve frequently | Monitor and retrain based on feedback | 08-monitoring/01-performance-monitoring |
| 9. Create a secure service | Prompt injection, data leakage, privacy | 04-technical/02-safety-and-security |
| 10. Define success and publish performance data | Measurable AI metrics, publish results | 04-technical/04-performance-benchmarks, 08-monitoring/01-performance-monitoring |
| 11. Choose the right tools and technology | Is an LLM genuinely the right choice? | 01-pre-assessment/01-problem-definition |
| 12. Make new source code open | Publish service code, document model choices | 06-procurement/03-build-vs-buy |
| 13. Use open standards and common components | ATRS compliance, GOV.UK patterns | 05-transparency/01-atrs-record |
| 14. Operate a reliable service | Fallbacks, uptime, vendor outage planning | 08-monitoring/04-incident-response |

## AI Playbook: Full 10-Principle Mapping

| AIP Principle | Description | Framework Section(s) |
|--------------|------------|---------------------|
| 1. Understand AI and its limitations | Know what LLMs can't do | 01-pre-assessment/01-problem-definition, 04-technical/01-accuracy |
| 2. Lawful, ethical, responsible use | Legal and ethical compliance | 02-legal (all), 03-ethics (all) |
| 3. Secure AI implementation | AI-specific security threats | 04-technical/02-safety-and-security |
| 4. Meaningful human control | Human-in-the-loop | 05-transparency/03-human-oversight |
| 5. Full AI lifecycle management | Monitor, retrain, decommission | 08-monitoring (all) |
| 6. Right tool for the job | Don't over-engineer with AI | 01-pre-assessment/01-problem-definition |
| 7. Open and collaborative | ATRS, share learnings | 05-transparency/01-atrs-record |
| 8. Work with commercial partners | Procurement alignment | 06-procurement (all) |
| 9. Skills and expertise | Team capability | 01-pre-assessment/04-team-composition |
| 10. Organisational alignment | Governance and assurance | 05-transparency/02-governance, 07-deployment/03-ministerial-sign-off |

## Data & AI Ethics Framework: Full 7-Principle Mapping

| DEF Principle | Description | Framework Section(s) |
|--------------|------------|---------------------|
| 1. Transparency | Explain how AI works | 05-transparency/01-atrs, 05-transparency/05-plain-language |
| 2. Accountability | Clear governance and ownership | 05-transparency/02-governance |
| 3. Fairness | Prevent bias and discrimination | 03-ethics/02-bias-audit, 04-technical/05-bias-testing |
| 4. Privacy | UK GDPR, data minimisation | 02-legal/01-uk-gdpr-compliance |
| 5. Safety | Reliable, no harm | 04-technical/02-safety-and-security |
| 6. Societal Impact | Public good, wider effects | 03-ethics/03-equality-impact-assessment |
| 7. Environmental Sustainability | Compute and carbon costs | 03-ethics/04-environmental-impact |

## ETA Framework: Full 7-Point Mapping

| ETA Point | Description | Framework Section(s) |
|----------|------------|---------------------|
| 1. Test to avoid unintended outcomes | Red-teaming, staged testing | 04-technical/03-red-teaming, 07-deployment/01-checklist |
| 2. Deliver fair services | Bias bounties, diverse teams, EIAs | 03-ethics/02-bias-audit, 03-ethics/03-eia |
| 3. Be clear who is responsible | SRO, ministerial sign-off | 05-transparency/02-governance, 07-deployment/03-sign-off |
| 4. Handle data safely | GDPR, DPIAs, data protection by design | 02-legal/01-uk-gdpr-compliance |
| 5. Help users understand impact | Plain-language, feedback loops | 05-transparency/04-contestability, 05-transparency/05-plain-language |
| 6. Ensure legal compliance | Legal sign-off from inception | 02-legal (all) |
| 7. Build something future-proof | Quarterly reviews, continuous monitoring | 08-monitoring/03-quarterly-review |

## AI Regulation White Paper: Full 5-Principle Mapping

| WP Principle | Description | Framework Section(s) |
|-------------|------------|---------------------|
| 1. Safety, security, robustness | Reliable, no harm | 04-technical/02-safety-and-security |
| 2. Transparency and explainability | Users understand AI decisions | 04-technical/06-explainability, 05-transparency/05-plain-language |
| 3. Fairness | No discrimination | 03-ethics/02-bias-audit, 04-technical/05-bias-testing |
| 4. Accountability and governance | Clear responsibility chains | 05-transparency/02-governance |
| 5. Contestability and redress | Citizens can challenge decisions | 05-transparency/04-contestability |

## AISI Evaluation Techniques: Full Mapping

| AISI Technique | Description | Framework Section(s) |
|---------------|------------|---------------------|
| 1. Automated Capability Assessments | Broad benchmark testing | 04-technical/04-performance-benchmarks |
| 2. Red-Teaming | Domain experts break safeguards | 04-technical/03-red-teaming |
| 3. Human Uplift Evaluations | Does AI help bad actors? | 04-technical/03-red-teaming |
| 4. AI Agent Evaluations | Autonomous behaviour testing | 04-technical/02-safety-and-security |

## Technology Code of Practice: Key Points Mapping

| TCoP Point | Description | Framework Section(s) |
|-----------|------------|---------------------|
| 1. Define user needs | User research | 01-pre-assessment/02-user-needs |
| 2. Accessible and inclusive | WCAG 2.2, no exclusion | 03-ethics/03-eia |
| 3. Open and use open source | Prefer open models/code | 06-procurement/03-build-vs-buy |
| 4. Use open standards | Standard APIs, avoid lock-in | 06-procurement/03-build-vs-buy |
| 6. Make things secure | Security assessment | 04-technical/02-safety-and-security |
| 7. Make privacy integral | Privacy-by-design | 02-legal/01-uk-gdpr-compliance |
| 11. Define purchasing strategy | Procurement approach | 06-procurement/01-supplier-assessment |
| 12. Make technology sustainable | Energy/compute costs | 03-ethics/04-environmental-impact |
| 13. Meet the Service Standard | Full SS compliance | 07-deployment/02-service-assessment |
