# NIST CSF 2.0 GOVERN Function — PCI DSS v4.0.1 Mapping

**Module:** 01 — Multi-Framework Control Mapping Engine
**Mapping direction:** NIST CSF 2.0 GOVERN (GV) → PCI DSS v4.0.1
**CSF source:** NIST CSWP 29, February 26, 2024 — `frameworks/nist-csf-2/csf-2-core.md`
**PCI DSS source:** PCI SSC, June 11, 2024 — `frameworks/pci-dss-4/pci-dss-v4-0-1-structure.md`
**Generated:** 2026-05-23
**Status:** AI-generated draft — requires practitioner validation before use

> **AI-assisted output.** All sub-requirement IDs, rationale, and confidence levels require verification against authoritative source documents before use in any assessment or client deliverable. Apply the validation rules in [`../../../../prompts/module-01-mapping-prompts.md`](../../../../prompts/module-01-mapping-prompts.md). Record findings in [`../../validation-logs/`](../../validation-logs/).

---

## Scope Note

The GOVERN function addresses organizational governance for cybersecurity: mission context, risk strategy, roles and responsibilities, policy, oversight, and supply chain risk management. PCI DSS v4.0.1 is a prescriptive, technically oriented standard focused on cardholder data environment (CDE) protection. It is not a governance framework.

Meaningful PCI DSS mappings for GOVERN concentrate in three categories: **Policy (GV.PO)**; **Roles and Responsibilities (GV.RR)**, where PCI DSS Requirement 12 includes explicit governance obligations; and **Supply Chain Risk Management (GV.SC)**, where PCI DSS Requirement 12.8 establishes a structured third-party service provider management program.

The **GV.RM (Risk Management Strategy)** and **GV.OV (Oversight)** categories have minimal (indirect) PCI DSS mapping. PCI DSS is compliance-based and prescriptive: it does not require organizations to define risk appetite, establish risk prioritization methodologies as a governance capability, or measure the performance of their cybersecurity strategy. These gaps are expected and do not reflect control weaknesses—they reflect the difference in scope between a governance framework and a cardholder data security standard.

**17 of 31 GOVERN subcategories have no meaningful PCI DSS counterpart.** This is structurally expected: absence of a PCI DSS mapping does not reduce the organizational significance of those subcategories in a banking cybersecurity program.

---

## Mapping Table

> **Copyright notice:** PCI DSS requirement text is copyright © 2006–2024 PCI Security Standards Council, LLC and is not reproduced here. Requirement IDs and section references only. Full text must be read in the official PCI DSS v4.0.1 document, available from the PCI SSC Document Library at pcisecuritystandards.org (free registration required).

| CSF Subcategory | CSF Outcome (brief) | PCI DSS Requirement(s) | Mapping Rationale | Confidence |
|:----------------|:--------------------|:-----------------------|:------------------|:----------:|
| **GV.OC-01** | Organizational mission shapes how cybersecurity risk decisions are framed and prioritized | No direct mapping | PCI DSS is a prescriptive cardholder data protection standard. It does not include requirements for how organizational mission should frame or prioritize cybersecurity risk decisions. | — |
| **GV.OC-02** | Internal and external stakeholders are identified and their cybersecurity needs factored into risk decisions | No direct mapping | PCI DSS does not include governance requirements for stakeholder identification or for incorporating stakeholder expectations into risk management decisions. | — |
| **GV.OC-03** | Legal, regulatory, and contractual cybersecurity obligations are identified and actively managed | No direct mapping | PCI DSS establishes specific CDE security obligations but does not require organizations to maintain a broader regulatory and contractual obligation inventory. PCI DSS is one obligation in this universe; meeting it does not satisfy the identification and tracking capability GV.OC-03 requires. | — |
| **GV.OC-04** | Key capabilities and services that external stakeholders depend on the organization to deliver are documented | No direct mapping | PCI DSS focuses on protecting inbound cardholder data flowing into the CDE. It does not address what the organization is responsible for delivering to external stakeholders. | — |
| **GV.OC-05** | Critical external capabilities and services the organization relies on are inventoried | 12.8.1 | PCI DSS requires maintaining a list of all TPSPs (third-party service providers) that share or could affect the security of cardholder data or the CDE. This is a scoped form of the external dependency inventory GV.OC-05 requires: limited to CDE-affecting service relationships rather than all critical external capabilities. | MEDIUM |
| **GV.RM-01** | Cybersecurity risk management objectives are defined and endorsed by relevant stakeholders | No direct mapping | PCI DSS specifies what must be protected; it does not require organizations to define their own risk management objectives or obtain governance-level endorsement for them. | — |
| **GV.RM-02** | Risk appetite and tolerance thresholds are documented, maintained, and shared | No direct mapping | PCI DSS is a pass/fail compliance framework. There are no concepts of risk appetite or organizational risk tolerance thresholds within its structure. | — |
| **GV.RM-03** | Cybersecurity risk activities are embedded in enterprise risk management | No direct mapping | PCI DSS is narrowly scoped to CDE protection. It does not require cybersecurity risk management to be integrated with enterprise risk management processes. | — |
| **GV.RM-04** | Guidance on acceptable risk response options is communicated to decision-makers | No direct mapping | PCI DSS specifies required controls and provides a customized approach pathway; it does not require organizations to communicate acceptable risk response options as a governance practice distinct from compliance. | — |
| **GV.RM-05** | Organization-wide channels for reporting cybersecurity risks — including supplier risk — are defined | No direct mapping | PCI DSS does not require formal organization-wide risk communication pathways. Incident escalation contacts in the IR plan (12.10.1) are incident-specific, not a general risk reporting architecture. | — |
| **GV.RM-06** | A consistent methodology for calculating, categorizing, and prioritizing cybersecurity risks is standardized | 12.3.1 | PCI DSS requires targeted risk analyses for requirements where implementation frequency is flexible; those analyses must follow a defined methodology and produce documented results. This partially captures the intent of a standardized risk prioritization methodology but is limited to PCI-scoped risk decisions rather than the full cybersecurity risk program. | MEDIUM |
| **GV.RM-07** | Upside risks and strategic opportunities are recognized and included in risk discussions | No direct mapping | PCI DSS does not address positive or opportunity-based risk management. | — |
| **GV.RR-01** | Organizational leadership is visibly accountable for cybersecurity risk and cultivates a risk-aware culture | 12.1.4 | PCI DSS requires that responsibility for information security be formally assigned to a CISO or equivalent executive management member, establishing the leadership-level accountability and formal ownership that GV.RR-01 requires. | HIGH |
| **GV.RR-02** | Cybersecurity roles, responsibilities, and decision-making authority are clearly defined, communicated, and enforced | 12.1.3 | PCI DSS requires that information security roles and responsibilities be formally defined, assigned to appropriate personnel, and understood: a direct analog to GV.RR-02's requirements for defined, communicated, and enforced role clarity. | HIGH |
| **GV.RR-03** | Cybersecurity resources — budget, personnel, and tools — are allocated proportional to risk priorities | No direct mapping | PCI DSS does not address resource allocation, staffing adequacy, or budgeting processes for cybersecurity. | — |
| **GV.RR-04** | Cybersecurity considerations are integrated into hiring, onboarding, performance management, and separation | 12.6.3, 12.7.1 | PCI DSS 12.7.1 requires pre-employment background screening for candidates who will have access to the CDE; 12.6.3 requires security awareness training at hire and at least annually thereafter. Together these address the pre-hire and onboarding integration that GV.RR-04 requires. PCI DSS does not address separation procedures or performance management integration. | MEDIUM |
| **GV.PO-01** | A cybersecurity risk management policy is formally documented, communicated, and enforced | 12.1.1 | PCI DSS requires an information security policy that is documented, communicated to all relevant personnel, and reviewed at least annually: a direct analog to the formal, communicated policy that GV.PO-01 requires. | HIGH |
| **GV.PO-02** | Cybersecurity policy is periodically reviewed and updated to reflect current requirements and threats | 12.1.1 | PCI DSS 12.1.1 explicitly requires annual review of the information security policy and update when the environment changes: directly corresponding to the policy maintenance activity that GV.PO-02 describes. GV.PO-01 and GV.PO-02 both map to 12.1.1; see Validation Notes. | HIGH |
| **GV.OV-01** | Cybersecurity risk management results are reviewed and used to refine organizational direction | No direct mapping | PCI DSS requires annual policy review (12.1.1) and annual scope confirmation (12.5.2) but does not include a requirement to evaluate whether the cybersecurity risk management strategy is achieving its risk management objectives and use those results to refine direction. | — |
| **GV.OV-02** | The cybersecurity risk management strategy is periodically reassessed for sufficiency | 12.5.2 | PCI DSS requires annual confirmation that PCI DSS scope remains accurate and complete: the closest analog to verifying the program remains sufficient for current needs. Scope validation is narrower than a strategic sufficiency assessment: it confirms boundaries, not program effectiveness. | LOW |
| **GV.OV-03** | Cybersecurity risk management performance is measured and evaluated, with findings used to drive adjustments | No direct mapping | PCI DSS requires security testing (Req 11) and — for service providers only — periodic compliance activity reviews (12.4.2). Neither applies as a general performance measurement requirement for all entities. See Validation Notes for the service-provider carve-out. | — |
| **GV.SC-01** | A formal C-SCRM program with strategy, objectives, policies, and processes is established | 12.8.1, 12.8.2 | PCI DSS requires a maintained list of all CDE-affecting TPSPs and written agreements with each, together establishing a structured third-party risk management program. This is a scoped analog to C-SCRM program establishment: limited to CDE-affecting supplier relationships. | MEDIUM |
| **GV.SC-02** | Cybersecurity responsibilities for suppliers, customers, and partners are defined and communicated internally and externally | 12.8.5, 12.9.1 | PCI DSS 12.8.5 requires explicit documentation of which PCI DSS requirements each TPSP is responsible for versus what the entity retains, and 12.9.1 requires TPSPs to acknowledge those responsibilities in writing: directly capturing the responsibility definition and external communication that GV.SC-02 requires, within CDE scope. | MEDIUM |
| **GV.SC-03** | C-SCRM is embedded in cybersecurity and enterprise risk management programs | No direct mapping | PCI DSS establishes specific TPSP management requirements (Req 12.8) but does not require supply chain risk management to be systematically integrated with broader cybersecurity or enterprise risk management programs. | — |
| **GV.SC-04** | Suppliers are inventoried and ranked by criticality to business operations | 12.8.1 | PCI DSS requires a maintained list of all TPSPs that could affect the security of the CDE, capturing the inventory component of GV.SC-04. PCI DSS does not require criticality ranking or tiering of suppliers: all CDE-affecting TPSPs are in scope regardless of relative business criticality. | MEDIUM |
| **GV.SC-05** | Cybersecurity requirements for supply chain relationships are established and embedded in contracts | 12.8.2 | PCI DSS requires written agreements with all CDE-affecting TPSPs that include acknowledgment of the TPSP's responsibility for protecting cardholder data: a direct analog to embedding cybersecurity requirements in supplier contracts. | HIGH |
| **GV.SC-06** | Cybersecurity risk assessment and planning occur before formalizing new supplier relationships | 12.8.3 | PCI DSS requires due diligence before engaging TPSPs, including assessment of potential impact on CDE security: a direct analog to pre-engagement cybersecurity risk assessment for new supply chain relationships. | HIGH |
| **GV.SC-07** | Risks from suppliers and third parties are documented, prioritized, and continuously monitored throughout the relationship | 12.8.4 | PCI DSS requires monitoring TPSP compliance status at least once every 12 months: capturing the ongoing monitoring activity that GV.SC-07 requires. Annual compliance status monitoring falls short of the continuous, prioritized risk monitoring that GV.SC-07 describes, making this a partial mapping. | MEDIUM |
| **GV.SC-08** | Key suppliers and third parties are included in incident planning, response, and recovery activities | No direct mapping | PCI DSS does not include an explicit requirement to involve key suppliers in incident planning, exercises, or recovery operations. Written TPSP agreements (12.8.2) establish contractual relationships but do not operationalize joint incident response. See Validation Notes. | — |
| **GV.SC-09** | Supply chain security practices are woven into cybersecurity and enterprise risk programs across the technology lifecycle | No direct mapping | PCI DSS specifies what TPSP management activities must occur (Req 12.8) but does not require supply chain security to be systematically embedded throughout the cybersecurity program or tracked across the technology lifecycle. | — |
| **GV.SC-10** | C-SCRM plans address cybersecurity risks that continue or arise after a supplier relationship ends | No direct mapping | PCI DSS addresses active in-scope TPSP relationships. It does not include requirements for managing cybersecurity risk that persists or arises after a supplier relationship concludes, such as residual data disposition or access revocation. See Validation Notes. | — |

---

## Mapping Summary

| Confidence Level | Count | CSF Subcategories |
|:-----------------|:-----:|:------------------|
| HIGH | 6 | GV.RR-01, GV.RR-02, GV.PO-01, GV.PO-02, GV.SC-05, GV.SC-06 |
| MEDIUM | 7 | GV.OC-05, GV.RM-06, GV.RR-04, GV.SC-01, GV.SC-02, GV.SC-04, GV.SC-07 |
| LOW | 1 | GV.OV-02 |
| No direct mapping | 17 | GV.OC-01/02/03/04, GV.RM-01/02/03/04/05/07, GV.RR-03, GV.OV-01/03, GV.SC-03/08/09/10 |
| **Total** | **31** | |

---

## Validation Notes

### 1. All sub-requirement IDs require verification against the official PCI DSS v4.0.1 document

The sub-requirement IDs cited in this file—12.1.1, 12.1.3, 12.1.4, 12.3.1, 12.5.2, 12.6.3, 12.7.1, 12.8.1 through 12.8.5, 12.9.1—are sourced from practitioner knowledge, not from a document file within this repository. The `frameworks/pci-dss-4/pci-dss-v4-0-1-structure.md` source file contains only the 12 top-level requirements.

**Before using any mapping in an assessment, verify each sub-requirement ID against the official PCI DSS v4.0.1 document** from the PCI SSC Document Library (`pcisecuritystandards.org`). The sub-requirement numbering structure changed materially from v3.2.1 to v4.0: do not assume prior-version numbering is still correct.

**Highest-risk IDs to verify first:**
- **12.1.3 and 12.1.4** (roles/responsibilities and CISO requirement): confirm these sub-requirements exist and correspond to the activities described. In v4.0.1, every requirement explicitly includes a roles-and-responsibilities sub-requirement that was not present in v3.2.1: the exact numbering within Requirement 12.1 needs confirmation.
- **12.8.1 through 12.8.5** (TPSP management): the v3.2.1 to v4.0 transition restructured these sub-requirements significantly. Confirm each sub-requirement number, title, and applicability (e.g., which apply to all entities vs. service providers only).

---

### 2. GV.PO-01 and GV.PO-02 both map to 12.1.1

This is intentional. PCI DSS 12.1.1 addresses both the existence of the policy (GV.PO-01) and its periodic review and update (GV.PO-02) within a single sub-requirement. The two CSF subcategories focus on distinct activities—establishment versus maintenance—that PCI DSS treats as a unit. For assessment evidence purposes, documentation satisfying 12.1.1 will simultaneously address both GV.PO subcategories. No double-counting concern: these are genuinely different practices joined in one PCI requirement.

---

### 3. GV.OV-03: service provider scope carve-out

PCI DSS 12.4.2 requires periodic reviews of PCI DSS compliance activities with documented results, but this requirement applies only to **service providers**—entities that provide services to other PCI DSS-covered entities and share in their CDE security responsibility. It was not mapped to GV.OV-03 because the majority of banking entities are not service providers in the PCI DSS sense.

**Practitioner action:** Determine whether the entity in scope also qualifies as a PCI DSS service provider. If yes, 12.4.2 is a relevant partial mapping for GV.OV-03 at MEDIUM confidence (it captures periodic compliance program review, not full performance measurement). Flag this determination in the validation log.

---

### 4. GV.SC-07: monitoring frequency gap

GV.SC-07 describes continuous, prioritized monitoring throughout the supplier relationship lifecycle. PCI DSS 12.8.4 requires monitoring TPSP compliance status **at least once every 12 months**. The confidence is capped at MEDIUM because annual point-in-time monitoring is materially different from continuous risk monitoring. When this mapping is used in a gap analysis, flag that PCI DSS 12.8.4 satisfies the minimum activity but that the frequency is likely insufficient for Tier 1 and Tier 2 banks under the CRI Profile, where more frequent monitoring is expected.

---

### 5. GV.SC-08: contractual basis exists but operational requirement does not

PCI DSS 12.8.2 (written agreements) and 12.9.2 (TPSP support for customer forensic investigation on request) create a contractual basis for TPSP involvement in incident activities, but neither is an operational requirement to include suppliers in incident planning, tabletop exercises, or recovery programs.

**Practitioner action:** Review whether the entity's incident response plan (12.10.1) and existing TPSP agreements specifically address joint incident response activities. If they do, that represents a control that satisfies GV.SC-08 beyond PCI DSS requirements. Document this in the validation log.

---

### 6. GV.SC-10: potential partial mappings to review

GV.SC-10 was assessed as having no direct PCI DSS mapping. However, a practitioner conducting a full gap analysis should evaluate whether the following requirements address components of post-relationship risk management for the specific entity:

- **Requirement 3 and 3.2.1** (stored account data and non-retention of sensitive authentication data): establish data disposition obligations that may remain relevant after a TPSP relationship ends if the TPSP held or processed account data.
- **Requirement 7 and 8** (access restriction and authentication): the requirements to restrict access by business need-to-know and to manage user credentials imply revocation of TPSP access at relationship termination, though this is not explicitly framed as a post-relationship risk activity.

These are components of specific operational controls, not a C-SCRM framework for managing post-relationship risk. Confirm whether the entity has implemented these as part of a formal offboarding process before including them in a GV.SC-10 assessment.

---

### 7. GV.RM-06 confidence is intentionally MEDIUM, not HIGH

The 12.3.1 mapping for GV.RM-06 is capped at MEDIUM because: (a) PCI DSS 12.3.1 applies to targeted risk analyses for specific periodic activities within PCI scope, not to the organization's enterprise cybersecurity risk prioritization methodology; and (b) the level of formality and documentation required by 12.3.1 may differ significantly from what GV.RM-06 envisions as a standardized, organization-wide risk methodology. A practitioner should determine whether the entity's 12.3.1 methodology documentation is integrated with its broader cybersecurity risk management practice or exists solely as a PCI compliance artifact: the latter does not satisfy GV.RM-06.

---

*Validation log entry to be created at: `../../validation-logs/[date]-govern-pci-dss.md`*
*Reviewed by: [practitioner name/date — to be completed after validation]*
