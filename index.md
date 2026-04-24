---
layout: default
title: Model Evaluation Framework for LLMs in the UK Public Sector
---

# Model Evaluation Framework for LLMs in the UK Public Sector

This framework helps UK public sector teams evaluate Large Language Models before, during, and after deployment. It tells you **what** to evaluate, **when** in the lifecycle, and **what evidence** to produce — scaled to the risk level of your use case.

## Table of Contents

- [Who this is for](#who-this-is-for)
- [How to use this framework](#how-to-use-this-framework)
- [Sections](#sections)
- [AI Assurance in Brief](#ai-assurance-in-brief)
- [Pillars](#pillars)
- [Risk Tiering](#risk-tiering)
  - [The four tiers](#the-four-tiers)
  - [How to assign your tier](#how-to-assign-your-tier)
  - [What the tier determines](#what-the-tier-determines)
- [How the Frameworks Fit Together](#how-the-frameworks-fit-together)
  - [When to use which](#when-to-use-which)
  - [How they connect in practice](#how-they-connect-in-practice)
  - [Cross-Gov Testing Framework modules](#cross-gov-testing-framework-modules)
  - [Source documents](#source-documents)

---

## Who this is for

Service owners, product owners, principal technologists, data scientists, ML engineers, safety and assurance teams, delivery leads, and DDaT governance.

## How to use this framework

1. Read the introduction to understand the pillars, risk tiers, and how frameworks connect
2. Find a use case that looks like yours
3. Assign your risk tier (R1–R4) using the AI Risk Management Toolkit
4. Follow the lifecycle phase by phase — each phase tells you what to do, the risk tier tells you how deeply, and bridge files point you to the right testing module
5. At each governance gate, check the evidence catalogue for your tier
6. Use templates to produce required documents

## Sections

| # | Section | What it does |
|---|---------|-------------|
| 00 | Introduction | Pillars, risk tiers, how frameworks connect |
| 01 | Use Cases | Two worked examples — low risk and high risk |
| 02 | Lifecycle | 5 phases with governance gates, testing guidance, UX research, and impact evaluation touchpoints |
| 03 | Governance | RACI, 4 gates, accountability, procurement |
| 04 | Evidence Catalogue | What artefacts to collect per risk tier |
| 05 | Templates | DPIA, EIA, ATRS, scorecard, model card, data card |
| 06 | Reference | 14 source documents, glossary, regulatory mapping, KPIs |

---

## AI Assurance in Brief

AI assurance is the process of measuring, evaluating, and communicating the trustworthiness of AI systems. It combines technical assurance (evaluation, validation, verification, and testing) with socio-technical assurance (explainability, ethics, governance, and human oversight) to give users, regulators, and the public confidence that AI systems are safe, fair, and accountable.

### Key distinction

- **Testing** generates evidence
- **Evaluation** interprets evidence in context
- **Assurance** provides confidence that systems are safe, fair, and accountable

### Further reading

| Resource | What it covers | Link |
|----------|---------------|------|
| Introduction to AI Assurance | Foundational concepts and the UK assurance ecosystem | [GOV.UK](https://www.gov.uk/government/publications/introduction-to-ai-assurance) |
| Roadmap to an Effective AI Assurance Ecosystem | How the UK is building assurance infrastructure | [GOV.UK](https://www.gov.uk/government/publications/the-roadmap-to-an-effective-ai-assurance-ecosystem) |
| CDEI Portfolio of AI Assurance Techniques | 8 assurance techniques with real-world examples | [GOV.UK](https://www.gov.uk/guidance/cdei-portfolio-of-ai-assurance-techniques) |
| Understanding AI Ethics and Safety | FAST/SAFE-D principles from the Alan Turing Institute | [GOV.UK](https://www.gov.uk/guidance/understanding-artificial-intelligence-ethics-and-safety) |
| AI Safety Institute Approach to Evaluations | How AISI evaluates frontier AI models | [GOV.UK](https://www.gov.uk/government/publications/ai-safety-institute-approach-to-evaluations) |

---

## Pillars

Seven principles underpin this framework. They are drawn from the E2VT operating model and aligned with the AI Playbook, Service Standard, and Data & AI Ethics Framework.

### 1. Risk-proportionate, trustworthy and safe AI

Controls scale with potential harm, impact, and autonomy. A low-risk internal tool does not need the same rigour as a public-facing benefits advisor. Align with the five cross-sectoral principles: safety, transparency, fairness, accountability, and contestability.

### 2. Evidence-first evaluation by design

Embed evaluation plans at the outset, not as an afterthought. Define what you will measure before you build. Claims require empirical proof and traceability — no evidence, no deployment.

### 3. Model-agnostic verification and validation

Verification and validation methods should work across both classical ML and generative models. Apply them differently depending on the model type and its failure modes, but the expectation of evidence applies equally.

### 4. Secure by design

Data minimisation, provenance, and least-privilege across the stack and lifecycle. Address AI-specific threats: data poisoning, prompt injection, jailbreaks, and PII leakage.

### 5. Human-centred, impact-focused deployment

AI tools must deliver clear value — improved services, reduced cost, or enhanced equity. Human factors, accessibility, and explainability are prioritised for end users and staff. Measure impact rigorously.

### 6. Reproducible and auditable

Every run can be reconstructed. Every model output can be traced to its inputs, data, and configuration. Logs and artefacts are tamper-proof. Every system action has an auditable trail.

### 7. Continuous improvement

Evaluation is ongoing — pre-production, canary, and post-deployment — not a one-off gate. Collect feedback, update models and evaluation plans, and share lessons across the public sector.

---

## Risk Tiering

Every AI deployment carries different levels of risk. This framework uses four risk tiers to scale evaluation effort proportionately. The tiers align with the risk appetite levels defined in the [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit).

### The four tiers

| Tier | Risk Appetite | Example Use Case | Typical Controls |
|------|--------------|-----------------|-----------------|
| **R1** | Minimal | Internal content search, low-consequence summarisation | Basic offline eval; logs; lightweight privacy and security checks; A/B only after sign-off |
| **R2** | Cautious | Staff productivity tools, non-critical internal advice | Expanded offline eval; calibration; bias screen; red-team lite; monitoring SLOs |
| **R3** | Open | Benefits triage, sensitive citizen advice, eligibility checks | Formal E2VT; domain SME panels; strong privacy/PII controls; comprehensive red-teaming; human-in-the-loop; change freeze windows |
| **R4** | Eager | Safety/security decisions, legal exposure, vulnerable cohorts | Independent assurance; external audit; formal E2VT with full test campaigns; canary with kill-switch; full traceability; quarterly re-certification |

### How to assign your tier

Use the **AI Risk Management Toolkit** to assess and score your risks. The toolkit provides:

- **9 risk categories** to investigate: financial, legal, transparency, fairness, accountability, contestability, robustness, security, and people/environment
- **100+ risk identification questions** to surface specific risks in your context
- **Likelihood scoring** (1–5): from Rare (<5%) to Almost Certain (>80%)
- **Impact scoring** (1–5): from Negligible to Catastrophic, with quantified thresholds (e.g., financial loss £10k–£50k = Minor, £200k–£1M = Major)
- **Risk appetite definitions** per category at each level (Averse, Minimal, Cautious, Open, Eager)

Your overall tier is determined by the highest risk appetite level across your significant risk categories. If any category scores at R3 (Open), your project is R3 — you do not average down.

This framework does not duplicate the toolkit's scoring methodology. Use it directly: [AI Risk Management Toolkit on GOV.UK](https://www.gov.uk/government/publications/ai-risk-management-toolkit)

### What the tier determines

| Framework Element | R1 | R2 | R3 | R4 |
|------------------|----|----|----|----|
| Governance gates | Automated | Mostly automated | Manual review | Manual + independent |
| Evidence catalogue | Slim | Standard | Comprehensive | Full + external audit |
| Testing depth | Cross-Gov Modules 1, 2, 6 | + Modules 3, 5 | + All 9 modules | All modules + external red-team |
| Human oversight | Human-on-the-loop optional | Human-on-the-loop | Human-in-the-loop | Human-in-the-loop + independent review |
| ATRS record | Recommended | Recommended | Required | Required |
| DPIA | Only if personal data | Likely required | Required | Required |
| EIA | Screening | Screening | Full EIA | Full EIA + ongoing |
| Quarterly review | Light-touch | Standard | Formal | Formal + external |
| Re-certification | On change only | Annual | Bi-annual | Quarterly |

---

## How the Frameworks Fit Together

Four frameworks work together. Each has one job. None duplicates another.

```
┌──────────────────────────────────────────────────────────────┐
│  THIS FRAMEWORK                                               │
│  What to evaluate, when, and what evidence to produce        │
│  Lifecycle · governance · legal · use cases                  │
├──────────────────────────────────────────────────────────────┤
│  CROSS-GOV AI TESTING FRAMEWORK                               │
│  How to test — 9 modules, techniques, metrics per AI type    │
├──────────────────────────────────────────────────────────────┤
│  AI RISK MANAGEMENT TOOLKIT                                   │
│  How to assess risk — identify, score, treat                 │
├──────────────────────────────────────────────────────────────┤
│  E2VT OPERATING MODEL                                         │
│  How deeply — risk tiers, gates, evidence catalogue, RACI    │
└──────────────────────────────────────────────────────────────┘
```

### When to use which

| You need to... | Go to |
|----------------|-------|
| Know what to evaluate and when | This framework — Lifecycle section |
| Run a specific test (bias, robustness, performance) | [Cross-Gov AI Testing Framework](https://testing-ai-standards.github.io/cross-gov-ai-testing-framework/) — pick the relevant module |
| Identify and score risks for your AI project | [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit) — 9 categories, 100+ questions |
| Understand governance gates and evidence requirements | This framework — Governance and Evidence Catalogue sections |
| Assign a risk tier (R1–R4) | This framework — [Risk Tiering](#risk-tiering) |
| Find legal/regulatory requirements | This framework — Lifecycle Phase 3 (Deploy) |
| Understand impact evaluation | [Magenta Book](https://www.gov.uk/government/publications/the-magenta-book) — this framework shows where it connects at each phase |

### How they connect in practice

A team building an AI service would:

1. **Start here** — read the introduction, pick a use case, assign a risk tier
2. **Use the AI Risk Management Toolkit** — at Phase 1 (Design) to identify and score risks
3. **Follow this framework's lifecycle** — phase by phase, gate by gate
4. **Use the Cross-Gov Testing Framework** — when this framework says "test for X", the bridge files point to the right Cross-Gov module
5. **Collect evidence per E2VT** — the evidence catalogue tells you what artefacts to produce at your tier
6. **Pass each governance gate** — with the required evidence signed off

### Cross-Gov Testing Framework modules

This framework references these modules by number throughout the lifecycle phases:

| Module | Focus |
|--------|-------|
| 1 | Data and input validation |
| 2 | Model functionality testing |
| 3 | Bias and fairness testing |
| 4 | Explainability and transparency |
| 5 | Robustness and adversarial testing |
| 6 | Performance and efficiency testing |
| 7 | Integration and system testing |
| 8 | User acceptance and ethical review |
| 9 | Continuous monitoring and improvement |

### Source documents

| # | Document | Publisher |
|---|----------|-----------|
| S1 | [Service Standard (14 points)](https://www.gov.uk/service-manual/service-standard) | GDS |
| S2 | [Service Manual](https://www.gov.uk/service-manual) | GDS |
| S3 | [AI Playbook (10 principles)](https://www.gov.uk/government/publications/ai-playbook-for-the-uk-government) | GDS/CDDO |
| S4 | [Data and AI Ethics Framework (7 principles)](https://www.gov.uk/government/publications/data-ethics-framework) | GDS/DSIT |
| S5 | [Ethics, Transparency and Accountability Framework (7 points)](https://www.gov.uk/government/publications/ethics-transparency-and-accountability-framework-for-automated-decision-making) | DSIT/CDEI |
| S6 | [AI Regulation White Paper (5 principles)](https://www.gov.uk/government/publications/ai-regulation-a-pro-innovation-approach) | DSIT |
| S7 | [Algorithmic Transparency Recording Standard](https://www.gov.uk/government/collections/algorithmic-transparency-recording-standard-hub) | DSIT/CDEI |
| S8 | [Guidelines for AI Procurement (10 considerations)](https://www.gov.uk/government/publications/guidelines-for-ai-procurement) | Office for AI |
| S9 | [AI Safety Institute Approach to Evaluations](https://www.gov.uk/government/publications/ai-safety-institute-approach-to-evaluations) | AISI |
| S10 | [Technology Code of Practice (13 points)](https://www.gov.uk/guidance/the-technology-code-of-practice) | GDS/Cabinet Office |
| S11 | [CDEI Portfolio of AI Assurance Techniques](https://www.gov.uk/guidance/cdei-portfolio-of-ai-assurance-techniques) | CDEI/RTA |
| S12 | [Understanding AI Ethics and Safety (FAST/SAFE-D)](https://www.gov.uk/guidance/understanding-artificial-intelligence-ethics-and-safety) | Alan Turing Institute |
| S13 | [ICO Guidance on AI and Data Protection](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/) | ICO |
| S14 | [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit) | GDS/DSIT |
