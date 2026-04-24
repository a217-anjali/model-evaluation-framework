# Regulatory Mapping

Which framework applies where — a quick-reference guide.

---

## By Organisation Type

| Organisation Type | Mandatory Frameworks | Recommended Frameworks |
|------------------|---------------------|----------------------|
| **Government department** | ATRS, Service Standard, TCoP, ETA, DEF, AI Playbook | AISI methodology, CDEI Assurance, Turing SAFE-D |
| **Arm's-length body (public-facing)** | ATRS, Service Standard, DEF, AI Playbook | ETA, TCoP, CDEI Assurance |
| **Arm's-length body (internal)** | DEF, AI Playbook | ATRS (recommended), ETA |
| **Local authority** | DEF, Equality Act | ATRS (recommended), Service Standard, AI Playbook |
| **NHS body** | DEF, Equality Act, sector regulation (CQC/MHRA) | ATRS (recommended), AI Playbook |
| **Police force** | DEF, Equality Act, sector regulation (HMICFRS) | ATRS (recommended), AI Playbook |

## By Use Case

| Use Case | Key Frameworks | Key Concerns |
|----------|---------------|-------------|
| **Citizen-facing chatbot** | SS, ATRS, ETA, DEF, ICO | Accuracy, accessibility, contestability, WCAG 2.2 |
| **Internal document summarisation** | AI Playbook, DEF | Data handling, security, lower governance burden |
| **Benefits/entitlement decisions** | ETA, ICO (Art 22), Equality Act, ATRS | Automated decisions, human oversight, contestability |
| **Healthcare advice** | CQC/MHRA, ICO, DEF, ETA | Patient safety, clinical validation, special category data |
| **Recruitment screening** | Equality Act, ICO, DEF | Bias across protected characteristics, Article 22 |
| **Content generation (comms)** | AI Playbook, DEF, ATRS | Hallucination, brand, misinformation |
| **Code generation (internal)** | AI Playbook | Security, IP, lower governance burden |
| **Legal/policy research** | AI Playbook, DEF | Accuracy, hallucination, no automated decisions |
| **Translation services** | SS, DEF, Equality Act | Accuracy, cultural sensitivity, accessibility |

## By Risk Level

| Risk Level | Characteristics | Required Governance |
|-----------|----------------|-------------------|
| **Low** | Internal use, no decisions about people, no personal data | AI Playbook basics, team awareness |
| **Medium** | Supports (not makes) decisions, limited personal data | DEF, DPIA, bias testing, human-on-the-loop |
| **High** | Citizen-facing, influences significant decisions, personal data | Full framework: ETA 7-point, ATRS, DPIA, EIA, red-teaming, human-in-the-loop |
| **Critical** | Sole/primary decision-maker, legal effects, special category data | All of the above + ministerial sign-off, independent audit, Article 22 safeguards |

## By Lifecycle Stage

| Stage | Applicable Frameworks | Key Activities |
|-------|----------------------|---------------|
| **Discovery** | SS Point 1, AI Playbook Principle 6 | User research, problem definition |
| **Alpha** | ETA Points 1-2, DEF, DPIA | Prototyping, bias testing, DPIA |
| **Beta** | Full framework | Red-teaming, security testing, service assessment |
| **Live** | ETA Point 7, SS Points 8/10/14 | Monitoring, quarterly reviews, performance publishing |
| **Retirement** | CDEI lifecycle, PROC Consideration 10 | Decommissioning, knowledge transfer |
