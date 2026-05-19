# NIST Cybersecurity Framework 2.0 — Overview

## About CSF 2.0

NIST released Cybersecurity Framework 2.0 (CSF 2.0) in February 2024, superseding CSF 1.1 (2018). The revision reflects six years of practitioner feedback, shifts the framework from critical infrastructure focus to applicability across all sectors and organization sizes, and introduces governance as a first-class concern alongside the original five functions. CSF 2.0 does not invalidate prior CSF 1.1 work—existing control mappings, policies, and assessments can be crosswalked—but organizations should account for the structural changes, particularly the promotion of governance activities and the formalization of supply chain risk management (C-SCRM) requirements.

---

## Core Functions

CSF 2.0 organizes cybersecurity outcomes across six functions, each assigned a two-letter abbreviation used throughout NIST reference materials:

| Function | Abbreviation | Purpose |
|---|---|---|
| **Govern** | GV | Establish and monitor the organization's cybersecurity risk management strategy, expectations, and policy. |
| **Identify** | ID | Understand the organization's assets, suppliers, and associated cybersecurity risks. |
| **Protect** | PR | Implement safeguards to manage cybersecurity risks to assets and data. |
| **Detect** | DE | Find and analyze anomalies, indicators of compromise, and other potentially adverse cybersecurity events. |
| **Respond** | RS | Take action regarding a detected cybersecurity incident. |
| **Recover** | RC | Restore assets and operations that were impacted by a cybersecurity incident. |

The first five functions (ID, PR, DE, RS, RC) map directly to their CSF 1.1 counterparts; Govern is new.

---

## Key Changes from CSF 1.1 to CSF 2.0

### New: Govern Function
Govern (GV) is the most structurally significant change. In CSF 1.1, governance activities were embedded within the Identify function or left implicit. CSF 2.0 elevates them into a standalone function with six categories covering organizational context, risk management strategy, roles and responsibilities, policy, oversight, and supply chain risk management. The intent is to make cybersecurity governance a board- and executive-level concern, not just a security-team concern.

### Expanded Supply Chain Risk Management (C-SCRM)
C-SCRM was a single subcategory in CSF 1.1. In CSF 2.0, it is a full category (GV.SC) within the Govern function with ten subcategories. These address supplier selection, contractual requirements, due diligence, monitoring, and incident response coordination across the supply chain. This aligns with requirements surfacing in FFIEC, OCC, and FRB guidance on third-party risk management.

### Organizational Profiles
CSF 2.0 formalizes the concept of Current and Target Profiles as a structured mechanism for gap analysis. A Current Profile documents the outcomes an organization is achieving today; a Target Profile documents desired outcomes given risk tolerance, legal obligations, and business objectives. The delta between the two drives the remediation roadmap. NIST provides a Community Profile template to support sector-specific adoption.

### CSF Tiers
Tiers (1–4: Partial, Risk-Informed, Repeatable, Adaptive) are retained from CSF 1.1 but clarified in CSF 2.0 as a characterization of the rigor and integration of cybersecurity risk management practices, not a maturity score. Tiers are intentionally not prescriptive; a Tier 3 or 4 may be appropriate for some organizations but unnecessary for others depending on risk profile.

---

## Why US Banks Are Adopting NIST CSF 2.0

The FFIEC Cybersecurity Assessment Tool (CAT), which was the dominant regulatory self-assessment framework for US depository institutions since 2015, was formally sunset on **August 31, 2025**. The FFIEC did not replace the CAT with a new proprietary tool; instead, its guidance directs institutions to map to established industry frameworks, with NIST CSF explicitly listed as an appropriate alternative.

For banks, the practical implications are:

- **Examination alignment.** OCC, FDIC, and Federal Reserve examiners are increasingly referencing CSF 2.0 outcomes and Tiers when evaluating cybersecurity program maturity. Institutions without a documented framework mapping face increased scrutiny.
- **Third-party risk.** The GV.SC categories provide a defensible structure for vendor risk programs, which regulators across all three primary federal banking agencies have prioritized in recent guidance.
- **Interoperability.** NIST has published informative reference crosswalks connecting CSF 2.0 to FFIEC CAT, NIST SP 800-53 Rev 5, ISO/IEC 27001:2022, and CIS Controls v8. Banks with existing control libraries can preserve prior investment while migrating to CSF 2.0 as the organizing structure.
- **Scalability.** Community banks and credit unions operating with lean GRC teams can use the Organizational Profile construct to scope assessments proportionally, rather than applying all 106 subcategories indiscriminately.

NIST CSF 2.0 is not a regulatory mandate for banks, but given the CAT sunset and examiner expectations, operating without a documented mapping to a recognized framework is a meaningful compliance and examination risk.

---

## References

- NIST Cybersecurity Framework landing page: [https://www.nist.gov/cyberframework](https://www.nist.gov/cyberframework)
- CSF 2.0 publication (NIST CSWP 29): [https://doi.org/10.6028/NIST.CSWP.29](https://doi.org/10.6028/NIST.CSWP.29)
- CSF 2.0 Quick Start Guides and Community Profiles: [https://www.nist.gov/cyberframework/csf-20-quick-start-guides](https://www.nist.gov/cyberframework/csf-20-quick-start-guides)
- FFIEC CAT sunset announcement (March 2024): [https://www.ffiec.gov/cyberassessmenttool.htm](https://www.ffiec.gov/cyberassessmenttool.htm)
- NIST SP 800-221A (C-SCRM guidance): [https://doi.org/10.6028/NIST.SP.800-221A](https://doi.org/10.6028/NIST.SP.800-221A)
