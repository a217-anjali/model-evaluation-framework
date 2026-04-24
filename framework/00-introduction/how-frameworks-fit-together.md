# How the Frameworks Fit Together

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

## When to use which

| You need to... | Go to |
|----------------|-------|
| Know what to evaluate and when | This framework — `02-lifecycle/` |
| Run a specific test (bias, robustness, performance) | [Cross-Gov AI Testing Framework](https://testing-ai-standards.github.io/cross-gov-ai-testing-framework/) — pick the relevant module |
| Identify and score risks for your AI project | [AI Risk Management Toolkit](https://www.gov.uk/government/publications/ai-risk-management-toolkit) — 9 categories, 100+ questions |
| Understand governance gates and evidence requirements | This framework — `03-governance/` and `04-evidence-catalogue/` (drawn from E2VT) |
| Assign a risk tier (R1–R4) | This framework — `risk-tiering.md` (uses the toolkit's appetite levels) |
| Find legal/regulatory requirements | This framework — `02-lifecycle/phase-3-deploy/legal-compliance.md` |
| Understand impact evaluation | [Magenta Book](https://www.gov.uk/government/publications/the-magenta-book) — this framework shows where it connects via `impact-eval-touchpoint.md` files |

## How they connect in practice

A team building an AI service would:

1. **Start here** — read the introduction, pick a use case, assign a risk tier
2. **Use the AI Risk Management Toolkit** — at Phase 1 (Design) to identify and score risks
3. **Follow this framework's lifecycle** — phase by phase, gate by gate
4. **Use the Cross-Gov Testing Framework** — when this framework says "test for X", the bridge files (`testing-guidance.md`) point to the right Cross-Gov module
5. **Collect evidence per E2VT** — the evidence catalogue tells you what artefacts to produce at your tier
6. **Pass each governance gate** — with the required evidence signed off

## The Cross-Gov Testing Framework's 9 Modules

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

## Source documents underpinning this framework

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
