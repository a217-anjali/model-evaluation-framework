# Introduction

This section provides the foundations for the Model Evaluation Framework for LLMs in the UK public sector. It covers what AI assurance means, the principles that guide evaluation, how to determine the right level of rigour for your project, and how this framework connects to companion frameworks already published across government.

---

## AI Assurance

AI assurance is the process of measuring, evaluating, and communicating the trustworthiness of AI systems. It combines technical assurance with socio-technical assurance.

Three terms are often used interchangeably but mean different things:

- **Testing** generates evidence
- **Evaluation** interprets that evidence in context
- **Assurance** provides confidence that systems are safe, fair, and accountable

This framework focuses on model evaluation — how well an AI system performs and behaves in its intended use, including accuracy, reliability, bias, and robustness.

---

## Pillars

Seven principles underpin this framework, aligned with the AI Playbook, Service Standard, and Data & AI Ethics Framework.

1. **Risk-proportionate, trustworthy and safe AI** — Controls scale with potential harm, impact, and autonomy. Align with the five cross-sectoral principles: safety, transparency, fairness, accountability, and contestability.

2. **Evidence-first evaluation by design** — Embed evaluation plans at the outset. Define what you will measure before you build. No evidence, no deployment.

3. **Model-agnostic verification and validation** — Methods should work across both classical ML and generative models, applied differently depending on the model type and its failure modes.

4. **Secure by design** — Data minimisation, provenance, and least-privilege across the stack and lifecycle. Address AI-specific threats: data poisoning, prompt injection, jailbreaks, and PII leakage.

5. **Human-centred, impact-focused deployment** — AI tools must deliver clear value. Human factors, accessibility, and explainability are prioritised for end users and staff.

6. **Reproducible and auditable** — Every run can be reconstructed. Every output can be traced to its inputs. Logs and artefacts are tamper-proof.

7. **Continuous improvement** — Evaluation is ongoing — pre-production, canary, and post-deployment — not a one-off gate.

---

## Risk Tiering

This framework uses four risk tiers to scale evaluation effort proportionately. The tiers align with the risk appetite levels defined in the [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit).

| Tier | Risk Appetite | Example | Controls |
|------|--------------|---------|----------|
| **R1** | Minimal | Internal summarisation | Basic offline eval, logs, lightweight checks |
| **R2** | Cautious | Staff productivity tools | Expanded eval, bias screen, red-team lite |
| **R3** | Open | Benefits triage, citizen advice | Formal evaluation, domain SME panels, human-in-the-loop |
| **R4** | Eager | Safety decisions, vulnerable cohorts | Independent audit, canary with kill-switch, quarterly re-certification |

Your tier is determined by the highest risk appetite level across your significant risk categories. If any category scores R3, your project is R3 — you do not average down. Use the [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit) to assign your tier.

The tier determines everything: governance gate depth, evidence catalogue size, testing scope, human oversight level, ATRS and DPIA requirements, review cadence, and re-certification frequency.

---

## How the Frameworks Fit Together

Three frameworks work together. Each has one job.

| Framework | What it does |
|-----------|-------------|
| **This framework** | What to evaluate, when, and what evidence to produce |
| [Cross-Gov AI Testing Framework](https://testing-ai-standards.github.io/cross-gov-ai-testing-framework/) | How to test — 9 modules with techniques and metrics per AI type |
| [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit) | How to assess risk — 9 categories, 100+ questions, scoring, treatment |
In practice, a team would: start here to understand their risk tier and what to evaluate; use the Risk Management Toolkit to identify and score risks; follow this framework's lifecycle phase by phase; use the Cross-Gov Testing Framework when they need to run a specific test; collect the evidence artefacts required for their tier; and pass each governance gate with signed-off evidence before moving to the next phase.

The [Magenta Book](https://www.gov.uk/government/publications/the-magenta-book) covers impact evaluation, which is complementary but separate. This framework shows where impact evaluation connects at each lifecycle stage.

---

## Pages in this section

| Page | What it covers |
|------|---------------|
| [AI Assurance in Brief](assurance.md) | Definition, key distinctions, further reading |
| [Pillars](pillars.md) | Seven principles in detail |
| [Risk Tiering](risk-tiering.md) | R1–R4 tiers, how to assign, what each tier requires |
| [How Frameworks Fit Together](frameworks.md) | The four-framework stack, when to use which, 14 source documents |

---

## Source Documents

This framework is built on 14 published UK government sources:

| Document | Publisher |
|----------|-----------|
| [Service Standard](https://www.gov.uk/service-manual/service-standard) | GDS |
| [Service Manual](https://www.gov.uk/service-manual) | GDS |
| [AI Playbook](https://www.gov.uk/government/publications/ai-playbook-for-the-uk-government) | GDS/CDDO |
| [Data and AI Ethics Framework](https://www.gov.uk/government/publications/data-ethics-framework) | GDS/DSIT |
| [Ethics, Transparency and Accountability Framework](https://www.gov.uk/government/publications/ethics-transparency-and-accountability-framework-for-automated-decision-making) | DSIT/CDEI |
| [AI Regulation White Paper](https://www.gov.uk/government/publications/ai-regulation-a-pro-innovation-approach) | DSIT |
| [Algorithmic Transparency Recording Standard](https://www.gov.uk/government/collections/algorithmic-transparency-recording-standard-hub) | DSIT/CDEI |
| [Guidelines for AI Procurement](https://www.gov.uk/government/publications/guidelines-for-ai-procurement) | Office for AI |
| [AI Safety Institute Evaluations](https://www.gov.uk/government/publications/ai-safety-institute-approach-to-evaluations) | AISI |
| [Technology Code of Practice](https://www.gov.uk/guidance/the-technology-code-of-practice) | GDS/Cabinet Office |
| [CDEI AI Assurance Techniques](https://www.gov.uk/guidance/cdei-portfolio-of-ai-assurance-techniques) | CDEI/RTA |
| [Understanding AI Ethics and Safety](https://www.gov.uk/guidance/understanding-artificial-intelligence-ethics-and-safety) | Alan Turing Institute |
| [ICO AI Guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/) | ICO |
| [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit) | GDS/DSIT |
