# Proposed Integrated Structure

## Model Evaluation Framework for LLMs in the UK Public Sector
### Integrating E2VT + Lifecycle Guide + Use Case Approach

---

## Design Principles for This Structure

1. **Lifecycle is the spine** — everything hangs off service phases (Design -> Develop -> Deploy -> Monitor -> Retire)
2. **Risk tiering throughout** — every section shows what's needed at R1 vs R4, not one-size-fits-all
3. **Use cases make it real** — two worked examples run through the entire framework
4. **Concise assurance** — one paragraph + references, not chapters of explanation
5. **Techniques linked to evidence** — published GOV.UK methods linked to specific artefacts
6. **Modular** — core spine + linked modules, not one long document

---

## Proposed Structure

```
framework/
│
├── 00-introduction/
│   ├── README.md                           # Purpose, scope, how to use (1 page)
│   ├── assurance-in-brief.md               # What is AI assurance — ONE short paragraph
│   │                                         + table of references (replaces E2VT Ch 1-3)
│   ├── pillars.md                          # 7 E2VT pillars as concise principles
│   │                                         (service-standard style, not essay style)
│   └── risk-tiering.md                     # R1-R4 risk tiers with control mapping
│                                             (from E2VT — decides depth for everything)
│
├── 01-use-cases/
│   ├── README.md                           # Why use cases, how to read them
│   ├── use-case-low-risk.md                # Worked example: internal summarisation (R1-R2)
│   │                                         Full lifecycle walkthrough showing minimum
│   │                                         requirements at each stage
│   └── use-case-high-risk.md               # Worked example: public-facing AI voice (R3-R4)
│                                             Full lifecycle walkthrough showing full E2VT
│                                             Reference gov voice for AI voice evaluations
│
├── 02-lifecycle/
│   │
│   ├── phase-1-design/
│   │   ├── README.md                       # Phase overview + Governance Gate 1
│   │   ├── problem-definition.md           # Is an LLM the right solution?
│   │   ├── user-needs-research.md          # Service Standard Point 1
│   │   ├── data-readiness.md               # Data quality, bias, governance
│   │   ├── team-composition.md             # Multidisciplinary team + RACI
│   │   ├── risk-assessment.md              # Risk tier assignment (R1-R4)
│   │   ├── evaluation-plan.md              # NEW: What will be evaluated, when, how
│   │   │                                     (E2VT "evidence-first by design")
│   │   └── impact-evaluation-link.md       # NEW: Theory of change, baseline,
│   │                                         connection to Magenta Book
│   │
│   │   >>> GOVERNANCE GATE 1: Evidence catalogue + risk register completed
│   │   >>> Artefacts: Use-case risk register, evidence catalogue template,
│   │   >>>            data lineage docs, data quality report
│   │
│   ├── phase-2-develop/
│   │   ├── README.md                       # Phase overview + Governance Gate 2
│   │   ├── accuracy-and-hallucination.md   # Factual accuracy, hallucination rates
│   │   ├── bias-testing.md                 # Output fairness across demographics
│   │   ├── safety-and-security.md          # Prompt injection, data leakage, jailbreaks
│   │   ├── explainability.md               # Can outputs be understood?
│   │   ├── test-harnesses.md               # NEW: Golden sets, red-team corpora,
│   │   │                                     protected-attribute slices, synthetic data,
│   │   │                                     human rating protocols (Cohen's kappa >= 0.7)
│   │   │                                     (from E2VT Section 4.2)
│   │   ├── ux-research-dev.md              # NEW: Human-AI interaction testing,
│   │   │                                     oversight interface design,
│   │   │                                     human-AI decision boundary evaluation
│   │   └── impact-evaluation-link.md       # NEW: Process evaluation design
│   │
│   │   >>> GOVERNANCE GATE 2: Bias/robustness thresholds evidenced
│   │   >>> Artefacts: Model card, evaluation plan, offline accuracy metrics,
│   │   >>>            bias/fairness screens, calibration results, threat model
│   │
│   ├── phase-3-deploy/
│   │   ├── README.md                       # Phase overview + Governance Gate 3
│   │   ├── legal-compliance.md             # UK GDPR, Equality Act, human rights,
│   │   │                                     sector regs (consolidated from old Section 02)
│   │   ├── ethics-and-fairness.md          # DEF principles, EIA, environmental impact
│   │   │                                     (consolidated from old Section 03)
│   │   ├── red-teaming.md                  # AISI methodology, adversarial testing
│   │   ├── performance-benchmarks.md       # Domain-specific task performance
│   │   ├── security-pen-testing.md         # Pen tests, privacy stress tests
│   │   ├── transparency.md                 # ATRS record, plain-language explanation
│   │   ├── human-oversight.md              # Human-in-the-loop design, override mechanisms
│   │   ├── contestability.md               # Citizen challenge and redress
│   │   ├── ux-research-deploy.md           # NEW: User experience testing,
│   │   │                                     oversight interface testing,
│   │   │                                     accessibility audit
│   │   ├── pre-deployment-checklist.md     # ETA 7-point gate
│   │   ├── service-assessment.md           # 14-point Service Standard
│   │   └── sign-off.md                     # Ministerial / SRO approval
│   │
│   │   >>> GOVERNANCE GATE 3: Deployment blocked without complete evaluation
│   │   >>> Artefacts: Deployment eval summary, pen-test reports, red-team reports,
│   │   >>>            incident response plan, ATRS record, signed checklist
│   │
│   ├── phase-4-operate/
│   │   ├── README.md                       # Phase overview + Governance Gate 4
│   │   ├── performance-monitoring.md       # KPIs, drift detection, dashboards
│   │   ├── bias-drift-detection.md         # Ongoing fairness monitoring
│   │   ├── continuous-evaluation.md        # NEW: Scheduled re-evaluation
│   │   │                                     (toxicity, hallucination, bias drift,
│   │   │                                     accuracy with live data — from E2VT)
│   │   ├── incident-response.md            # Preparation, response, recovery,
│   │   │                                     lessons learned (expanded from E2VT 3.10-3.12)
│   │   ├── quarterly-review.md             # Formal review cycle
│   │   ├── ux-research-live.md             # NEW: User satisfaction, cognitive impact,
│   │   │                                     retention measurement, feedback loops
│   │   └── impact-evaluation-link.md       # NEW: Outcome measurement, RCT/QED,
│   │                                         connection to impact evaluation team
│   │
│   │   >>> GOVERNANCE GATE 4: Continuous assurance + readiness review
│   │   >>> Artefacts: Monitoring dashboards, incident logs, version updates
│   │   >>>            with audit trail, signed assurance case
│   │
│   └── phase-5-retire/
│       ├── README.md                       # End-of-life process
│       ├── decommissioning.md              # Data disposal, service continuity, archive
│       └── impact-evaluation-link.md       # NEW: Final impact assessment
│
├── 03-techniques/
│   │   # NEW SECTION: Links published GOV.UK methods to specific objectives
│   │   # This is the "how to do it" layer that generates evidence
│   │
│   ├── README.md                           # How to use this section:
│   │                                         Objective -> Technique -> Evidence
│   ├── accuracy-techniques.md              # Methods for measuring accuracy
│   │                                         Sources: AISI automated assessments,
│   │                                         CDEI performance testing
│   │                                         Output: Accuracy report (evidence artefact)
│   ├── bias-techniques.md                  # Methods for testing bias
│   │                                         Sources: CDEI bias audit, AISI societal
│   │                                         impacts, DEF fairness metrics
│   │                                         Output: Bias audit report (evidence artefact)
│   ├── red-team-techniques.md              # Methods for adversarial testing
│   │                                         Sources: AISI red-teaming, AISI human
│   │                                         uplift, ETA Point 1
│   │                                         Output: Red-team report (evidence artefact)
│   ├── security-techniques.md              # Methods for security testing
│   │                                         Sources: NCSC, OWASP Top 10 for LLMs,
│   │                                         AISI safeguards
│   │                                         Output: Security assessment (evidence artefact)
│   ├── explainability-techniques.md        # Methods for achieving explainability
│   │                                         Sources: Turing SAFE-D, AI Procurement
│   │                                         Guidelines
│   │                                         Output: Model card, user-facing explanation
│   ├── fairness-techniques.md              # Methods for fairness measurement
│   │                                         Sources: DEF (demographic parity,
│   │                                         equalized odds), Turing 4 dimensions
│   │                                         Output: EIA, fairness metrics report
│   └── monitoring-techniques.md            # Methods for ongoing monitoring
│                                             Sources: CDEI impact evaluation,
│                                             ETA Point 7
│                                             Output: Monitoring dashboard, drift reports
│
├── 04-governance/
│   │   # Consolidated governance (concise, not sprawling)
│   │
│   ├── raci-matrix.md                      # Who does what (from E2VT)
│   ├── governance-gates.md                 # 4 gates: criteria, artefacts, sign-off
│   ├── accountability-structure.md         # SRO, review boards, escalation
│   └── procurement.md                      # Supplier assessment, contract clauses
│                                             (including E2VT assurance clauses:
│                                             sovereign options, right to audit,
│                                             portability)
│
├── 05-evidence-catalogue/
│   │   # NEW: From E2VT Section 4.1
│   │   # What artefacts to collect at each tier
│   │
│   ├── README.md                           # How the catalogue works, tier mapping
│   ├── data-artefacts.md                   # Data cards, lineage, quality profiles
│   ├── model-artefacts.md                  # Model cards, training config, calibration
│   ├── system-artefacts.md                 # Test cases, FMEA, UX notes, safety filters
│   ├── security-artefacts.md               # Threat model, pen-test, red-team logs
│   ├── monitoring-artefacts.md             # Dashboards, runbooks, rollback records
│   └── assurance-case.md                   # Structured argument:
│                                             requirements -> evidence -> conclusion
│
├── 06-templates/
│   ├── dpia-template.md
│   ├── eia-template.md
│   ├── atrs-template.md
│   ├── risk-assessment-template.md
│   ├── evaluation-scorecard.md
│   ├── evidence-catalogue-template.md      # NEW: Blank evidence catalogue per tier
│   ├── model-card-template.md              # NEW
│   └── data-card-template.md               # NEW
│
├── 07-reference/
│   ├── uk-frameworks-index.md              # All 13+ sources with links
│   ├── glossary.md
│   ├── regulatory-mapping.md               # By org type, use case, risk level
│   ├── alignment-map.md                    # Source -> section mapping
│   ├── kpis.md                             # NEW: Full KPI catalogue
│   │                                         (ATRS coverage, eval integration,
│   │                                         incident readiness, public trust,
│   │                                         efficiency, error reduction,
│   │                                         cognitive impact, user satisfaction)
│   └── lifecycle-comparison.md             # NEW: Model eval vs impact eval
│                                             at each lifecycle stage — shows scope
│                                             and handoff to impact evaluation team
```

---

## What Changed vs Current Structure

| Current (10 sections) | New (7 sections) | Why |
|----------------------|-------------------|-----|
| 00-overview | 00-introduction | Slimmed down — assurance is 1 paragraph, not pages |
| *Not present* | **01-use-cases** | **NEW** — two worked examples (low risk, high risk) |
| 01 to 08 (by topic) | **02-lifecycle** (by phase) | **Reorganised** — lifecycle is the spine, not topic silos |
| *Scattered across sections* | **03-techniques** | **NEW** — published GOV.UK methods -> evidence artefacts |
| 05-transparency, 06-procurement | **04-governance** | **Consolidated** — RACI, gates, accountability, procurement |
| *Not present* | **05-evidence-catalogue** | **NEW** — from E2VT 4.1, what artefacts to collect per tier |
| 09-templates | 06-templates | Expanded with model card, data card, evidence catalogue |
| 10-reference | 07-reference | Expanded with KPIs, lifecycle comparison |

---

## How It Reads for a Team

**Step 1:** Read `00-introduction/risk-tiering.md` — "We're building X, that's R2"

**Step 2:** Read `01-use-cases/use-case-low-risk.md` — "This looks like our project, here's what a team like ours did"

**Step 3:** Follow `02-lifecycle/` phase by phase:
- At each phase, the file tells you what to do
- Risk tier tells you how deeply to do it
- Governance gate tells you what evidence you need before moving on

**Step 4:** When you need to actually run a test, go to `03-techniques/` — "I need to test for bias, here's the published method and what evidence it produces"

**Step 5:** Check `05-evidence-catalogue/` — "Do I have all the artefacts for my tier?"

**Step 6:** Pass the governance gate and move to the next phase

---

## Key Integrations

### E2VT Content Integrated

| E2VT Element | Where It Goes |
|-------------|---------------|
| Risk Tiering R1-R4 | `00-introduction/risk-tiering.md` — applies across everything |
| 4 Governance Gates | `02-lifecycle/` — one gate per phase boundary |
| Evidence Catalogue | `05-evidence-catalogue/` — dedicated section |
| RACI Matrix | `04-governance/raci-matrix.md` |
| Test Harnesses | `02-lifecycle/phase-2-develop/test-harnesses.md` |
| KPIs | `07-reference/kpis.md` |
| Procurement clauses | `04-governance/procurement.md` |
| 7 Pillars | `00-introduction/pillars.md` (concise, service-standard style) |

### Your Suggestions Integrated

| Suggestion | Where It Goes |
|-----------|---------------|
| Concise assurance | `00-introduction/assurance-in-brief.md` — 1 paragraph + refs |
| Lifecycle approach | `02-lifecycle/` — the entire spine |
| Use cases (low + high risk) | `01-use-cases/` — two worked examples |
| Gov voice reference | `01-use-cases/use-case-high-risk.md` |
| Full lifecycle (model + impact) | `impact-evaluation-link.md` at each phase |
| UX research scope | `ux-research-*.md` at develop, deploy, and operate phases |
| Published techniques -> evidence | `03-techniques/` — the "how to do it" layer |

---

## Impact Evaluation Touchpoints (for handoff to impact team)

| Phase | Model Evaluation (this framework) | Impact Evaluation (Magenta Book) |
|-------|----------------------------------|----------------------------------|
| Design | Problem definition, data readiness | Theory of change, baseline measurement |
| Develop | Accuracy, bias, robustness testing | Process evaluation design |
| Deploy | Red-team, security, service assessment | Outcome measurement begins |
| Operate | Drift, monitoring, continuous eval | Impact measurement (RCT/QED) |
| Retire | End-of-life report | Final impact assessment |

---

## UX Research Scope (across lifecycle)

| Phase | UX Research Activities |
|-------|----------------------|
| Design | User needs discovery, attitudes toward AI, accessibility needs |
| Develop | Human-AI interaction testing, oversight interface design, decision boundary evaluation |
| Deploy | User experience testing, accessibility audit, oversight interface testing |
| Operate | User satisfaction, cognitive impact measurement, retention/recall assessment, feedback loops |
