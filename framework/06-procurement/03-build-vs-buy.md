# 03 — Build vs. Buy Decision

## Sources

| Source | Reference |
|--------|-----------|
| Technology Code of Practice | Point 3: Be open and use open source |
| Technology Code of Practice | Point 4: Make use of open standards |
| AI Procurement Guidelines | Consideration 8: Algorithm transparency (avoid vendor lock-in) |
| Service Standard | Point 12: Make new source code open |

## Purpose

Decide whether to build (host/fine-tune an open-source LLM), buy (use a proprietary API), or a hybrid approach. TCoP favours open source where possible. PROC warns against "black box" systems and vendor lock-in.

## Decision Framework

| Factor | Build (Open Source) | Buy (Proprietary API) |
|--------|-------------------|----------------------|
| **Transparency** | Full visibility into model | Limited visibility (black box risk) |
| **Vendor lock-in** | Low | High |
| **Cost model** | Upfront infrastructure cost | Pay-per-use |
| **Maintenance** | Organisation's responsibility | Supplier's responsibility |
| **Performance** | May be lower for frontier tasks | Typically higher for general tasks |
| **Security control** | Full control over data flow | Data leaves your infrastructure |
| **Customisation** | Full fine-tuning capability | Limited to prompting / vendor tools |
| **Speed to deploy** | Slower | Faster |
| **Skills required** | ML engineering capability needed | Lower technical barrier |

## Requirements

### If building / open source

- [ ] Hosting infrastructure meets government security standards
- [ ] Team has ML engineering capability to maintain the model
- [ ] Open-source licence is compatible with government use
- [ ] Service code is published as open source (SS Point 12)
- [ ] Model selection rationale documented

### If buying / proprietary API

- [ ] Vendor lock-in risk assessed and mitigated (PROC Consideration 8)
- [ ] Exit strategy defined (how to switch providers)
- [ ] Data processing location confirmed
- [ ] Sufficient transparency for ATRS compliance
- [ ] Standard APIs used where possible (TCoP Point 4)
- [ ] Explainability requirements met despite proprietary nature

### Open standards (TCoP Point 4)

- [ ] Standard data formats used for inputs/outputs
- [ ] Standard APIs used (avoiding proprietary interfaces where possible)
- [ ] Interoperability with other government systems considered

## Output

1. Build vs. buy decision record with rationale
2. Vendor lock-in risk assessment (if buying)
3. Open source licence review (if building)
