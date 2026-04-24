---
layout: default
title: Risk Tiering
parent: Introduction
nav_order: 3
---

# Risk Tiering

Every AI deployment carries different levels of risk. This framework uses four risk tiers to scale evaluation effort proportionately. The tiers align with the risk appetite levels defined in the [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit).

---

## The four tiers

| Tier | Risk Appetite | Example Use Case | Typical Controls |
|------|--------------|-----------------|-----------------|
| **R1** | Minimal | Internal content search, low-consequence summarisation | Basic offline eval; logs; lightweight privacy and security checks |
| **R2** | Cautious | Staff productivity tools, non-critical internal advice | Expanded offline eval; calibration; bias screen; red-team lite; monitoring SLOs |
| **R3** | Open | Benefits triage, sensitive citizen advice, eligibility checks | Formal E2VT; domain SME panels; comprehensive red-teaming; human-in-the-loop |
| **R4** | Eager | Safety/security decisions, legal exposure, vulnerable cohorts | Independent assurance; external audit; canary with kill-switch; quarterly re-certification |

---

## How to assign your tier

Use the **AI Risk Management Toolkit** to assess and score your risks. The toolkit provides:

- **9 risk categories**: financial, legal, transparency, fairness, accountability, contestability, robustness, security, and people/environment
- **100+ risk identification questions** to surface specific risks
- **Likelihood scoring** (1–5): from Rare (<5%) to Almost Certain (>80%)
- **Impact scoring** (1–5): from Negligible to Catastrophic, with quantified thresholds
- **Risk appetite definitions** per category at each level

Your overall tier is determined by the highest risk appetite level across your significant risk categories. If any category scores at R3 (Open), your project is R3 — you do not average down.

[AI Risk Management Toolkit on GOV.UK](https://www.gov.uk/government/publications/ai-risk-management-toolkit){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

---

## What the tier determines

| Element | R1 | R2 | R3 | R4 |
|---------|----|----|----|----|
| Governance gates | Automated | Mostly automated | Manual review | Manual + independent |
| Evidence catalogue | Slim | Standard | Comprehensive | Full + external audit |
| Testing depth | Modules 1, 2, 6 | + Modules 3, 5 | All 9 modules | All + external red-team |
| Human oversight | Optional | Human-on-the-loop | Human-in-the-loop | + independent review |
| ATRS record | Recommended | Recommended | Required | Required |
| DPIA | If personal data | Likely required | Required | Required |
| EIA | Screening | Screening | Full EIA | Full EIA + ongoing |
| Quarterly review | Light-touch | Standard | Formal | Formal + external |
| Re-certification | On change | Annual | Bi-annual | Quarterly |
