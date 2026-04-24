# Final Structure: Model Evaluation Framework for LLMs in the UK Public Sector

---

## How the Four Frameworks Fit Together

```
┌──────────────────────────────────────────────────────────────┐
│  This Framework                                               │
│  WHAT to evaluate, WHEN, and WHAT EVIDENCE to produce        │
│  Lifecycle spine + governance + legal + use cases             │
├──────────────────────────────────────────────────────────────┤
│  Cross-Gov AI Testing Framework                               │
│  HOW to test — 9 modules, techniques, metrics per AI type    │
│  https://testing-ai-standards.github.io/                      │
│  cross-gov-ai-testing-framework/                              │
├──────────────────────────────────────────────────────────────┤
│  AI Risk Management Toolkit                                   │
│  HOW to assess risk — identify, score (1-5), treat           │
│  9 risk categories, 100+ questions, quantified impact tables │
├──────────────────────────────────────────────────────────────┤
│  E2VT                                                         │
│  HOW DEEPLY — risk tiers, governance gates, evidence         │
│  catalogue, RACI, assurance case                              │
└──────────────────────────────────────────────────────────────┘
```

**No framework duplicates another. Each has one job.**

---

## Structure

```
framework/
│
├── 00-introduction/
│   ├── README.md
│   ├── assurance-in-brief.md
│   ├── pillars.md
│   ├── risk-tiering.md
│   └── how-frameworks-fit-together.md
│
├── 01-use-cases/
│   ├── README.md
│   ├── use-case-low-risk.md
│   └── use-case-high-risk.md
│
├── 02-lifecycle/
│   ├── phase-1-design/
│   ├── phase-2-develop/
│   ├── phase-3-deploy/
│   ├── phase-4-operate/
│   └── phase-5-retire/
│
├── 03-governance/
│   ├── raci-matrix.md
│   ├── governance-gates.md
│   ├── accountability.md
│   └── procurement.md
│
├── 04-evidence-catalogue/
│   ├── README.md
│   ├── data-artefacts.md
│   ├── model-artefacts.md
│   ├── system-artefacts.md
│   ├── security-artefacts.md
│   ├── monitoring-artefacts.md
│   └── assurance-case.md
│
├── 05-templates/
│
└── 06-reference/
```

---

## Section-by-Section Detail

### 00-introduction/

| File | Content | Length |
|------|---------|--------|
| **README.md** | Purpose, scope, audience, how to read this framework | 1 page |
| **assurance-in-brief.md** | One paragraph defining AI assurance + table of references. NOT chapters of explanation. Written in service-standard style. | Half page |
| **pillars.md** | E2VT's 7 pillars as concise one-liners with a short description each. Service-standard style (like the 14 points), not essay style. | 1 page |
| **risk-tiering.md** | R1-R4 tiers with control summary table. Links to AI Risk Management Toolkit for how to assign the tier (risk appetite definitions, scoring 1-5, 9 categories). Does NOT duplicate the toolkit's questions or scoring tables. | 1 page |
| **how-frameworks-fit-together.md** | Diagram + table showing what each framework does, when to use it, and how they connect. The "you are here" map. | 1 page |

---

### 01-use-cases/

| File | Content |
|------|---------|
| **README.md** | Why use cases, how to read them, how to pick which one matches your project |
| **use-case-low-risk.md** | **Worked example: internal document summarisation (R1-R2).** Walks through the entire lifecycle showing minimum requirements at each phase. Shows which governance gates are lightweight/automated. Points to specific Cross-Gov modules (1, 2, 6) for testing. Shows a slim evidence catalogue. Demonstrates: you don't need the full framework for low-risk work. |
| **use-case-high-risk.md** | **Worked example: public-facing AI voice service (R3-R4).** References gov voice for AI voice evaluations. Full lifecycle walkthrough showing comprehensive E2VT. All 4 governance gates with manual sign-off. Points to all 9 Cross-Gov modules. Full evidence catalogue. DPIA, EIA, ATRS all required. Demonstrates: this is what rigorous evaluation looks like end-to-end. |

---

### 02-lifecycle/

#### phase-1-design/ (Discovery / Alpha / Offline E2VT)

| File | Content | Sources |
|------|---------|---------|
| **README.md** | Phase overview. Gate 1 criteria and required artefacts. | E2VT Gate 1 |
| **problem-definition.md** | Is an LLM the right solution? Assessment questions. Inappropriate use cases. | AI Playbook P6, SS Point 11, SS Point 2 |
| **user-needs-research.md** | User research requirements. Attitudes to AI. Accessibility. Failure recovery. | SS Point 1, SS Point 2 |
| **data-readiness.md** | Data quality, governance, 4 types of bias in data, minimisation. | AI Procurement C3, DEF P4, Turing Data Stewardship |
| **team-and-raci.md** | Required roles table + RACI matrix for this phase. | SS Point 6, ETA Point 2, E2VT RACI |
| **risk-assessment.md** | Assign R1-R4 using AI Risk Management Toolkit. Link to toolkit's 9 categories, identification questions, and scoring. Do NOT duplicate the toolkit. | AI Risk Toolkit, E2VT risk tiering |
| **evaluation-plan.md** | What will be evaluated, when, how, by whom. Maps evaluation objectives to Cross-Gov testing modules. This is the bridge. | E2VT "evidence-first by design", Cross-Gov modules |
| **impact-eval-touchpoint.md** | Theory of change. Baseline measurement. Connection to Magenta Book. Handoff point to impact evaluation team. | Magenta Book |

**Gate 1:** Evidence catalogue template + risk register completed. Cannot proceed to build without these.

**Artefacts:** Use-case risk register, evidence catalogue (template), data lineage docs, data quality report, evaluation plan.

---

#### phase-2-develop/ (Beta / Offline E2VT)

| File | Content | Sources |
|------|---------|---------|
| **README.md** | Phase overview. Gate 2 criteria and required artefacts. | E2VT Gate 2 |
| **test-harnesses.md** | How to set up test infrastructure: golden sets, red-team corpora, protected-attribute slices, synthetic data, human rating protocols (Cohen's kappa >= 0.7). This is test INFRASTRUCTURE, not techniques. | E2VT 4.2 |
| **testing-guidance.md** | Bridge file. Maps evaluation objectives to Cross-Gov modules: accuracy -> Module 2, bias -> Module 3, robustness -> Module 5, explainability -> Module 4. Does NOT rewrite techniques. | Cross-Gov Testing Framework |
| **ux-research.md** | Human-AI interaction testing. Oversight interface design. Decision boundary evaluation. | SS Point 4, E2VT |
| **impact-eval-touchpoint.md** | Process evaluation design. | Magenta Book |

**Gate 2:** Bias/robustness thresholds evidenced before pre-prod release.

**Artefacts:** Model card, evaluation plan, offline accuracy/utility metrics, bias/fairness screens, calibration results, explainability plan, initial threat model.

---

#### phase-3-deploy/ (Private Beta / Controlled Testing)

| File | Content | Sources |
|------|---------|---------|
| **README.md** | Phase overview. Gate 3 criteria and required artefacts. | E2VT Gate 3 |
| **legal-compliance.md** | UK GDPR (Article 22, lawful basis, DPIA). Equality Act (EIA, PSED). Human rights. Sector-specific regulation. Consolidated — one file, not four. | ICO, ETA P4/P6, DEF P4, Equality Act |
| **ethics-and-fairness.md** | DEF 7 principles applied. Environmental impact. Consolidated — one file. | DEF, Turing SAFE-D |
| **transparency.md** | ATRS record (mandatory). Plain-language explanation. Presumption of publication. | ATRS, ETA P5, DEF P1, WP P2 |
| **human-oversight.md** | Levels of oversight (full auto / on-the-loop / in-the-loop / human-only). Meaningful review requirements. Contestability and redress mechanisms. | AIP P4, ICO Art 22, WP P5, ETA P5 |
| **testing-guidance.md** | Bridge file. Maps to Cross-Gov modules: red-team -> Module 5, security -> Module 5, integration -> Module 7, UAT -> Module 8. | Cross-Gov Testing Framework |
| **ux-research.md** | User experience testing. Accessibility audit (WCAG 2.2). Oversight interface testing. | SS Point 5, TCoP P2 |
| **pre-deployment-checklist.md** | ETA 7-point go/no-go gate. Sign-off table (SRO, legal, DPO, technical, minister if applicable). | ETA all 7 points |
| **service-assessment.md** | 14-point Service Standard compliance table with evidence pointers. Assessment process (4-hour panel, green/amber/red). | SS all 14 points, TCoP P13 |

**Gate 3:** Deployment blocked without complete evaluation and SLO sign-off.

**Artefacts:** Deployment evaluation summary, pen-test reports, red-team reports, ATRS record, incident response plan, signed checklist.

---

#### phase-4-operate/ (Public Beta / Canary / Live)

| File | Content | Sources |
|------|---------|---------|
| **README.md** | Phase overview. Gate 4 criteria. | E2VT Gate 4 |
| **monitoring.md** | KPIs table. Drift detection. Dashboards. Automated alerts. Publishing performance data. References Cross-Gov Module 9 for monitoring techniques. | ETA P7, SS P8/P10/P14, AIP P5 |
| **continuous-evaluation.md** | Scheduled re-evaluation: toxicity, hallucination, bias drift, accuracy with live data. Re-test triggers (model updates, data changes, complaints). | E2VT, CDEI Impact Evaluation |
| **incident-response.md** | Full incident lifecycle: preparation, response (kill switch, fallback), recovery, lessons learned, detection at scale. | AIP P4, WP P1, SS P14, E2VT 3.10-3.12 |
| **quarterly-review.md** | Formal review agenda: performance, fairness, incidents, user feedback, compliance, technology, governance, forward look. Decisions: continue / improve / pause / decommission. | ETA P7 |
| **ux-research.md** | User satisfaction. Cognitive impact and retention measurement. Feedback loops. | E2VT KPIs |
| **impact-eval-touchpoint.md** | Outcome measurement. RCT/QED where feasible. Handoff to impact evaluation team. | Magenta Book |

**Gate 4:** Continuous assurance and readiness review.

**Artefacts:** Monitoring dashboards, incident logs, version updates with audit trail, signed assurance case.

---

#### phase-5-retire/

| File | Content | Sources |
|------|---------|---------|
| **decommissioning.md** | Triggers for decommissioning. Data handling (retention, deletion from supplier). Service continuity. Knowledge preservation. ATRS updated. Governance stood down. | AI Procurement C10, CDEI Lifecycle |
| **impact-eval-touchpoint.md** | Final impact assessment. | Magenta Book |

---

### 03-governance/

| File | Content | Sources |
|------|---------|---------|
| **raci-matrix.md** | RACI for each activity area: risk tiering, model evaluation plan, impact evaluation plan, data ethics, red team, go-live, monitoring. | E2VT |
| **governance-gates.md** | All 4 gates in one place: criteria, required artefacts, sign-off roles, automated vs manual decision. Risk-proportionate: R1-R2 gates can be automated in CI/CD pipeline; R3-R4 require manual review. | E2VT |
| **accountability.md** | SRO, AI Review Board, escalation procedures. Key principle: "the public body remains responsible even when using third-party LLMs." | ETA P3, DEF P2, AIP P10 |
| **procurement.md** | Supplier assessment criteria. Contract clauses: ATRS info, right to audit red-team results, sovereign options and portability, knowledge transfer, no lock-in for evaluation. Build vs buy decision framework. | AI Procurement, E2VT, TCoP P3/P4 |

---

### 04-evidence-catalogue/

| File | Content | Sources |
|------|---------|---------|
| **README.md** | How the catalogue works. What's required per risk tier (R1 = slim, R4 = comprehensive). | E2VT 4.1 |
| **data-artefacts.md** | Data card, lineage/provenance graph, consent and lawful basis, quality profiles, drift baselines. | E2VT 4.1 |
| **model-artefacts.md** | Model card, training config and seeds, versioned weights, hyperparameters, calibration curves, uncertainty estimates, adversarial robustness report. | E2VT 4.1 |
| **system-artefacts.md** | End-to-end test cases, FMEA, UX research notes, accessibility checks, human override/escalation design, safety filter tests. | E2VT 4.1 |
| **security-artefacts.md** | Threat model (STRIDE/LINDDUN), pen-test results, red-team logs, prompt injection tests, PII leakage tests, encryption and key management evidence. | E2VT 4.1 |
| **monitoring-artefacts.md** | Monitoring dashboards, incident runbook, rollback records, change control records, post-incident reviews. | E2VT 4.1 |
| **assurance-case.md** | Structured argument linking requirements -> evidence -> conclusion. Similar to "definition of done" in agile. Goal Structuring Notation (optional). | E2VT 4.1 |

---

### 05-templates/

| Template | Required By |
|----------|------------|
| **dpia-template.md** | ICO, ETA P4, DEF P4 |
| **eia-template.md** | ETA P2, DEF P3, Equality Act 2010 |
| **atrs-template.md** | ATRS (mandatory Dec 2024) |
| **evaluation-scorecard.md** | Consolidated scoring against all frameworks |
| **evidence-catalogue-template.md** | E2VT 4.1 — blank catalogue per tier |
| **model-card-template.md** | E2VT, Cross-Gov Module 4 |
| **data-card-template.md** | E2VT, Cross-Gov Module 1 |

**No risk assessment template.** Teams use the AI Risk Management Toolkit's workbook directly — no duplication.

---

### 06-reference/

| File | Content |
|------|---------|
| **uk-frameworks-index.md** | All 14 source documents with links and status |
| **glossary.md** | Key terms and definitions |
| **regulatory-mapping.md** | By org type, use case, risk level, lifecycle stage |
| **alignment-map.md** | Master mapping: every source point -> framework section |
| **kpis.md** | Full KPI catalogue: ATRS coverage, eval integration, incident readiness, public trust, efficiency, error reduction, cognitive impact, user satisfaction |
| **lifecycle-comparison.md** | Model eval vs impact eval at each lifecycle stage — scope and handoff points |

---

## Source Documents (S1-S14)

| # | Document | Publisher |
|---|----------|-----------|
| S1 | Service Standard (14 points) | GDS |
| S2 | Service Manual | GDS |
| S3 | AI Playbook (10 principles) | GDS/CDDO |
| S4 | Data and AI Ethics Framework (7 principles) | GDS/DSIT |
| S5 | Ethics, Transparency and Accountability Framework (7 points) | DSIT/CDEI |
| S6 | AI Regulation White Paper (5 principles) | DSIT |
| S7 | Algorithmic Transparency Recording Standard | DSIT/CDEI |
| S8 | Guidelines for AI Procurement (10 considerations) | Office for AI |
| S9 | AI Safety Institute Approach to Evaluations | AISI |
| S10 | Technology Code of Practice (13 points) | GDS/Cabinet Office |
| S11 | CDEI Portfolio of AI Assurance Techniques | CDEI/RTA |
| S12 | Understanding AI Ethics and Safety (FAST/SAFE-D) | Alan Turing Institute |
| S13 | ICO Guidance on AI and Data Protection | ICO |
| S14 | AI Risk Management Toolkit | GDS/DSIT |

**Companion frameworks (referenced, not duplicated):**
- Cross-Gov AI Testing Framework (testing techniques and metrics)
- E2VT (risk tiers, gates, evidence catalogue, RACI)
- AI Risk Management Toolkit (risk identification, scoring, treatment)
- Magenta Book (impact evaluation)

---

## File Count

| Section | Files |
|---------|-------|
| 00-introduction | 5 |
| 01-use-cases | 3 |
| 02-lifecycle (5 phases) | 27 |
| 03-governance | 4 |
| 04-evidence-catalogue | 7 |
| 05-templates | 7 |
| 06-reference | 6 |
| **Total** | **59** |

---

## How a Team Uses This

**Step 1:** Read `00-introduction/` — understand the pillars, risk tiers, and how the four frameworks connect (5 mins)

**Step 2:** Read `01-use-cases/` — find the use case that looks like yours (10 mins)

**Step 3:** Go to `02-lifecycle/phase-1-design/risk-assessment.md` — use the AI Risk Management Toolkit to assign your risk tier (R1-R4)

**Step 4:** Follow `02-lifecycle/` phase by phase:
- Each phase tells you **what to do**
- Risk tier tells you **how deeply**
- `testing-guidance.md` bridge files tell you **which Cross-Gov module to use**
- `impact-eval-touchpoint.md` tells you **where impact evaluation connects**

**Step 5:** At each gate, check `04-evidence-catalogue/` — do you have the required artefacts for your tier?

**Step 6:** Pass the governance gate (`03-governance/governance-gates.md`) and move to the next phase

**Step 7:** Use `05-templates/` to produce the required documents

**No overlap. No duplication. Each framework does one job.**
