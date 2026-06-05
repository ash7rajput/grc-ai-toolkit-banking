# NIST CSF 2.0 GOVERN Function — SOC 2 Trust Services Criteria Mapping

**Module:** 01 — Multi-Framework Control Mapping Engine
**Mapping direction:** NIST CSF 2.0 GOVERN (GV) → SOC 2 Trust Services Criteria (TSC 2017, revised 2022)
**CSF source:** NIST CSWP 29, February 26, 2024 — `frameworks/nist-csf-2/csf-2-core.md`
**SOC 2 source:** AICPA Trust Services Criteria, 2017 revised 2022 — `frameworks/soc2-tsc/soc2-tsc-structure.md`
**Generated:** 2026-05-24
**Status:** AI-generated draft — requires practitioner validation before use

> **AI-assisted output.** All criterion IDs, rationale, and confidence levels require verification against the authoritative AICPA TSC publication before use in any assessment, client deliverable, or examination-support context. Apply the validation rules in [`../../../../prompts/module-01-mapping-prompts.md`](../../../../prompts/module-01-mapping-prompts.md). Record findings in [`../../validation-logs/`](../../validation-logs/).

---

## Scope Notes

### SOC 2 maps GOVERN substantially better than PCI DSS

SOC 2's Common Criteria are built on the **COSO 2013 Internal Control – Integrated Framework**, which is a governance and risk management model. This makes SOC 2 structurally well-suited to map against GOVERN subcategories in ways that PCI DSS—a prescriptive cardholder data standard—is not. Where the [PCI DSS mapping](csf-govern-to-pci-dss-v4-0-1.md) produced 17 "no direct mapping" results, this mapping produces only 1. That difference reflects framework design, not control coverage gaps.

### All mappings in this file are to Common Criteria (CC1–CC9)

The Common Criteria are the Security category of the TSC and are **universal**: they appear in every SOC 2 report regardless of scope. No GOVERN subcategory maps to the optional categories (Availability/A1, Processing Integrity/PI1, Confidentiality/C1, Privacy/P1–P8). Those categories address operational system behavior and data handling; GOVERN addresses strategic governance capabilities. This is expected and not a mapping gap.

Where optional-category criteria are tangentially relevant, this is called out in the Validation Notes rather than in the table.

### SOC 2 system boundary caveat

SOC 2 examinations are scoped to a specific **system**: a defined set of infrastructure, software, people, procedures, and data. The TSC criteria apply in the context of that system, not to the organization as a whole. GOVERN subcategories are enterprise-level governance requirements that apply organization-wide.

This means SOC 2 mappings for GV.OC and GV.RM subcategories are partial by design: where SOC 2 requires the control environment and risk assessment to support security of *the in-scope system*, CSF GOVERN requires those same capabilities to operate at the enterprise level. A bank's SOC 2 report addresses the system in scope; its CSF GOVERN program extends across all cybersecurity activities. **A SOC 2 mapping to a GOVERN subcategory does not mean the bank's CSF GOVERN obligation is satisfied by SOC 2 compliance alone.**

### CC9.2 appears across ten GV.SC subcategories

CC9.2 is the single SOC 2 criterion for vendor and business partner risk management. It is the primary—and often only—SOC 2 analog for the ten GV.SC subcategories. This concentration is structurally correct, not a mapping error. CC9.2 is a broad criterion; the GV.SC subcategories slice the same domain into ten more granular program-level requirements. Verify that CC9.2 exists and confirm it is the correct criterion number before use.

---

## Mapping Table

> **Copyright notice:** AICPA Trust Services Criteria text, criterion statements, and Points of Focus are copyright © American Institute of Certified Public Accountants. Not reproduced here. Criterion IDs cited as references only. Full text must be read in the official AICPA TSC publication. This mapping does not constitute attestation or audit advice; consult a licensed CPA firm for examination guidance.

| CSF Subcategory | CSF Outcome (brief) | SOC 2 Criterion/Criteria | Mapping Rationale | Confidence |
|:----------------|:--------------------|:-------------------------|:------------------|:----------:|
| **GV.OC-01** | Organizational mission shapes how cybersecurity risk decisions are framed and prioritized | CC3.1 | SOC 2 CC3.1 requires the entity to specify objectives clearly enough to identify and assess risks to their achievement (COSO Principle 6). Mission-informed risk management is the upstream activity that defines those objectives; CC3.1's requirement to articulate objectives as the basis for risk decisions partially captures this. SOC 2 does not require that mission explicitly drive risk framing. | MEDIUM |
| **GV.OC-02** | Internal and external stakeholders are identified and their cybersecurity needs factored into risk decisions | CC2.2, CC2.3 | CC2.2 requires management to communicate information internally to support the functioning of internal control; CC2.3 requires external communication with parties affected by the entity's services. Together they address the flow of stakeholder information that GV.OC-02 requires, but neither criterion explicitly requires identifying and incorporating stakeholder needs as a governance input to risk decisions. | MEDIUM |
| **GV.OC-03** | Legal, regulatory, and contractual cybersecurity obligations are identified and actively managed | CC3.1, CC5.3 | CC3.1 requires specifying objectives with consideration of applicable legal and regulatory requirements as inputs to risk assessment. CC5.3 requires the entity to deploy policies and procedures that implement management's directives, including those driven by compliance obligations. Together these partially capture the obligation identification and management that GV.OC-03 requires, but SOC 2 does not require a formal regulatory inventory as a distinct governance output. | MEDIUM |
| **GV.OC-04** | Key capabilities and services that external stakeholders depend on the organization to deliver are documented | CC2.3 | CC2.3 requires management to communicate with external parties about matters affecting their use of the entity's services, which implies an understanding of what external parties depend on the entity to provide. The criterion addresses the communication of that information outward, not the documentation of dependencies as an inventory: making this a low-confidence partial mapping. | LOW |
| **GV.OC-05** | Critical external capabilities and services the organization relies on are inventoried | CC9.2 | SOC 2 CC9.2 requires the entity to assess and manage risks from vendor and business partner relationships, which necessarily involves identifying those relationships and the capabilities they provide. The inventory of critical external dependencies is a precondition for the risk management that CC9.2 requires. CC9.2 focuses on risk management, not the inventory activity itself, so this is a medium-confidence alignment. | MEDIUM |
| **GV.RM-01** | Cybersecurity risk management objectives are defined and endorsed by relevant stakeholders | CC3.1, CC1.2 | CC3.1 requires the entity to specify objectives clearly enough to identify and analyze risks: capturing the "define objectives" activity. CC1.2 requires the board to exercise oversight of strategic plans and significant risk decisions: capturing stakeholder endorsement at the governance level. Neither criterion uses the vocabulary of "risk management objectives" as a named governance output. | MEDIUM |
| **GV.RM-02** | Risk appetite and tolerance thresholds are documented, maintained, and shared | CC3.2, CC1.2 | CC3.2 requires the entity to identify risks to achieving objectives and analyze them, which in practice involves defining risk tolerances that determine when identified risks require response. CC1.2 requires board oversight including over how significant risks are managed, which encompasses oversight of risk appetite. SOC 2 does not require a documented risk appetite statement as a distinct artifact. | MEDIUM |
| **GV.RM-03** | Cybersecurity risk activities are embedded in enterprise risk management | CC3.2 | CC3.2 requires a risk assessment process that identifies risks across the entity's objectives: a framework that, when fully implemented, integrates cybersecurity risks into the same process used for other organizational risks. SOC 2 is system-scoped and does not require that risk management be formally integrated with an enterprise risk management function: this is a partial mapping. | MEDIUM |
| **GV.RM-04** | Guidance on acceptable risk response options is communicated to decision-makers | CC2.2, CC3.2 | CC3.2 requires identifying risks and selecting appropriate risk responses; CC2.2 requires that information needed to support control objectives: including risk response guidance: is communicated internally to those responsible for acting on it. Neither criterion explicitly requires that acceptable risk response options be defined and communicated as a governance discipline separate from the risk assessment process. | MEDIUM |
| **GV.RM-05** | Organization-wide channels for reporting cybersecurity risks: including supplier risk: are defined | CC2.2, CC2.3 | CC2.2 requires that relevant information be communicated internally through defined channels to the people who need it, and CC2.3 requires external communication channels for parties relevant to the system. These criteria require that risk information flows: implying communication channels exist: but do not require channels to be formally defined as named governance infrastructure. | MEDIUM |
| **GV.RM-06** | A consistent methodology for calculating, categorizing, and prioritizing cybersecurity risks is standardized | CC3.2 | CC3.2 requires the entity to identify and analyze risks to achieving its objectives, which requires a methodology to do so consistently. SOC 2 does not require this methodology to be formally documented as an enterprise standard: the COSO principle underlying CC3.2 implies structured analysis, not a defined, communicated methodology as GV.RM-06 specifies. | MEDIUM |
| **GV.RM-07** | Upside risks and strategic opportunities are recognized and included in risk discussions | No direct mapping | SOC 2 TSC focuses on risk identification and management for achieving control objectives in the context of a defined system. It does not address positive or opportunity-based risk management. | — |
| **GV.RR-01** | Organizational leadership is visibly accountable for cybersecurity risk and cultivates a risk-aware culture | CC1.1, CC1.2 | CC1.1 requires demonstrated commitment to integrity and competence from the top of the organization (COSO Principle 1: tone at the top), and CC1.2 requires the board to exercise meaningful oversight over strategic plans and significant risks including cybersecurity (COSO Principle 2). Together these directly capture leadership-level accountability for cybersecurity risk. | HIGH |
| **GV.RR-02** | Cybersecurity roles, responsibilities, and decision-making authority are clearly defined, communicated, and enforced | CC1.3 | SOC 2 CC1.3 requires the entity to consider all organizational structures and assign authority and responsibility for achieving objectives (COSO Principle 3). This is a direct analog to GV.RR-02's requirement to define, communicate, and enforce cybersecurity roles and decision-making authority. | HIGH |
| **GV.RR-03** | Personnel, budget, and tools are allocated proportional to cybersecurity risk priorities | CC1.4 | CC1.4 requires the entity to demonstrate commitment to attracting, developing, and retaining competent individuals in alignment with its objectives (COSO Principle 4). This partially captures the personnel resourcing dimension of GV.RR-03 but does not address budget allocation or tool procurement proportional to risk. | LOW |
| **GV.RR-04** | Cybersecurity considerations are integrated into hiring, onboarding, performance management, and separation | CC1.4, CC1.5, CC6.2, CC6.3 | CC1.4 (commitment to competence through qualified hiring), CC1.5 (accountability enforcement through performance processes), CC6.2 (access provisioning before granting system access: relevant at hire/onboarding), and CC6.3 (modifying or removing access at role change or separation) together address the HR lifecycle integration that GV.RR-04 requires. The mapping is distributed across two criteria series (Control Environment and Logical Access) rather than addressed by a single criterion. | MEDIUM |
| **GV.PO-01** | A cybersecurity risk management policy is formally documented and communicated | CC5.3, CC2.2 | CC5.3 requires the entity to deploy control activities through documented policies and procedures that implement management's directives (COSO Principle 12), directly capturing the policy documentation requirement. CC2.2 requires internal communication including of those policies to the people responsible for acting on them. Together these are a direct analog to GV.PO-01. | HIGH |
| **GV.PO-02** | Cybersecurity policy is periodically reviewed and updated to reflect current requirements and threats | CC5.3, CC4.1 | CC5.3 requires policies to be deployed and maintained: which implies keeping them current: and CC4.1 requires ongoing and separate evaluations of the control environment, including whether policies and procedures remain adequate for current conditions. Neither criterion specifies a review frequency; the update obligation is implied by CC5.3's maintenance requirement and CC4.1's evaluation requirement. | MEDIUM |
| **GV.OV-01** | Cybersecurity risk management results are reviewed and used to refine organizational direction | CC4.1, CC4.2 | CC4.1 requires ongoing and separate evaluations of whether internal controls are present and functioning; CC4.2 requires that deficiencies identified through those evaluations are communicated to responsible parties and that remediation actions are taken. Together these directly address the review-and-refine cycle that GV.OV-01 requires. CC1.2 (board oversight) is also relevant where findings reach the strategic direction level. | HIGH |
| **GV.OV-02** | The cybersecurity risk management strategy is periodically reassessed for sufficiency | CC3.4, CC4.1 | CC3.4 requires the entity to identify and analyze significant changes in the external environment, business model, and technology that could affect the control framework: capturing the trigger events that necessitate strategic reassessment. CC4.1 provides the evaluation mechanism through which sufficiency is assessed. Together these address GV.OV-02's requirement but do not specify a periodic reassessment cadence. | MEDIUM |
| **GV.OV-03** | Cybersecurity risk management performance is measured and evaluated, with findings used to drive adjustments | CC4.1, CC4.2 | CC4.1 requires the entity to conduct ongoing and separate evaluations of whether controls are present and functioning: this is performance measurement. CC4.2 requires that deficiencies are communicated to responsible parties, that management and the board are informed as appropriate, and that corrective action is taken: this is performance evaluation with consequence. | HIGH |
| **GV.SC-01** | A formal C-SCRM program with strategy, objectives, policies, and processes is established | CC9.2 | SOC 2 CC9.2 requires the entity to assess and manage risks from vendor and business partner relationships, establishing the vendor risk management program that GV.SC-01's C-SCRM program establishment requires. CC9.2 is a principle-level criterion; the strategy, objectives, policies, and processes GV.SC-01 specifies represent implementation detail beyond what CC9.2 prescribes. | HIGH |
| **GV.SC-02** | Cybersecurity responsibilities for suppliers, customers, and partners are defined and communicated internally and externally | CC9.2, CC2.3 | CC9.2 requires managing vendor and business partner risks, which includes defining the cybersecurity responsibilities of those parties. CC2.3 requires external communication with relevant parties: including vendors: about matters affecting the system. Neither criterion explicitly requires a documented responsibility matrix for supply chain cybersecurity. | MEDIUM |
| **GV.SC-03** | C-SCRM is embedded in cybersecurity and enterprise risk management programs | CC9.2, CC3.2 | CC9.2 addresses vendor risk management as a component of the overall security control environment; CC3.2 requires a risk assessment framework that encompasses all risks to achieving objectives, including supply chain risks. Together these imply integration of supply chain risk into the broader risk program, but SOC 2 does not require this integration to be formalized or documented as a governance output. | MEDIUM |
| **GV.SC-04** | Suppliers are inventoried and ranked by criticality to business operations | CC9.2 | CC9.2 requires the entity to identify vendors and business partners and assess the risks they represent: an inventory is a prerequisite for this assessment. Criticality-based ranking is not explicitly required by CC9.2 but is implied by the risk-based prioritization that a sound vendor management program requires. | MEDIUM |
| **GV.SC-05** | Cybersecurity requirements for supply chain relationships are established and embedded in contracts | CC9.2 | CC9.2 requires the entity to establish requirements for vendor and business partner performance related to the security of the system, and to evaluate vendors' compliance with those requirements. Embedding security requirements in contracts is the primary mechanism for establishing those performance expectations. | HIGH |
| **GV.SC-06** | Cybersecurity risk assessment and planning occur before formalizing new supplier relationships | CC9.2 | CC9.2 requires the entity to assess risks of vendors and business partners before establishing relationships: a direct analog to GV.SC-06's pre-engagement due diligence requirement. | HIGH |
| **GV.SC-07** | Risks from suppliers and third parties are documented, prioritized, and continuously monitored throughout the relationship | CC9.2 | CC9.2 requires ongoing assessment and management of vendor and business partner risks throughout the relationship lifecycle, including monitoring of vendor performance and activities. This directly corresponds to GV.SC-07's requirement for continuous, documented risk monitoring. | HIGH |
| **GV.SC-08** | Key suppliers and third parties are included in incident planning, response, and recovery activities | CC7.4, CC9.2 | CC7.4 requires the entity to respond to identified security incidents through defined procedures, including notification and coordination with relevant parties: which may include key vendors. CC9.2's vendor management framework provides the governance basis for involving suppliers. Neither criterion explicitly requires vendors to be included in incident planning or exercises. | MEDIUM |
| **GV.SC-09** | Supply chain security practices are woven into cybersecurity and enterprise risk programs across the technology lifecycle | CC9.2, CC3.2 | CC9.2 establishes vendor and business partner risk management as an integrated component of the overall control framework; CC3.2 requires a risk assessment process encompassing all organizational risks including supply chain. Together these capture the integration intent, but neither requires supply chain security to be systematically tracked across the full technology acquisition and decommissioning lifecycle. | MEDIUM |
| **GV.SC-10** | C-SCRM plans address cybersecurity risks that continue or arise after a supplier relationship ends | CC9.2, CC6.3 | CC9.2's vendor management lifecycle encompasses relationship termination activities: the entity must manage the offboarding of vendors as a risk management matter. CC6.3 requires that access is removed or modified when no longer needed, which applies directly at the end of a vendor relationship. Neither criterion explicitly requires a C-SCRM framework addressing ongoing cybersecurity risk after relationship conclusion. | LOW |

---

## Mapping Summary

| Confidence Level | Count | CSF Subcategories |
|:-----------------|:-----:|:------------------|
| HIGH | 9 | GV.RR-01, GV.RR-02, GV.PO-01, GV.OV-01, GV.OV-03, GV.SC-01, GV.SC-05, GV.SC-06, GV.SC-07 |
| MEDIUM | 18 | GV.OC-01/02/03/05, GV.RM-01/02/03/04/05/06, GV.RR-04, GV.PO-02, GV.OV-02, GV.SC-02/03/04/08/09 |
| LOW | 3 | GV.OC-04, GV.RR-03, GV.SC-10 |
| No direct mapping | 1 | GV.RM-07 |
| **Total** | **31** | |

**Criteria referenced:** CC1.1, CC1.2, CC1.3, CC1.4, CC1.5, CC2.2, CC2.3, CC3.1, CC3.2, CC3.4, CC4.1, CC4.2, CC5.3, CC6.3, CC7.4, CC9.2

**Optional categories used:** None — all mappings are to Common Criteria (Security category, universal to every SOC 2 report)

---

## Validation Notes

### 1. All criterion IDs require verification against the official AICPA TSC publication

The criterion IDs cited in this file come from practitioner knowledge of the AICPA TSC 2017/2022 publication, not from a source document within this repository. The `frameworks/soc2-tsc/soc2-tsc-structure.md` source file contains only series-level summaries, not individual criterion IDs.

**Before using any mapping, verify each criterion ID against the authoritative AICPA publication**—*Trust Services Criteria for Security, Availability, Processing Integrity, Confidentiality, and Privacy (2017, with 2022 updates)*, available through the AICPA & CIMA Online Store.

**Specific verification required:**

| Series | Criteria used in this file | Upper bound to verify | Risk |
|--------|---------------------------|----------------------|------|
| CC1 | CC1.1, CC1.2, CC1.3, CC1.4, CC1.5 | CC1 has 5 criteria | Medium: confident in numbering |
| CC2 | CC2.2, CC2.3 | CC2 has 3 criteria | Medium: CC2.1 is not used; confirm CC2.2 and CC2.3 labels |
| CC3 | CC3.1, CC3.2, CC3.4 | CC3 has 4 criteria | Medium: confirm CC3.4 covers significant change analysis |
| CC4 | CC4.1, CC4.2 | CC4 has 2 criteria | Low: confident |
| CC5 | CC5.3 | CC5 has 3 criteria | Low: CC5.3 is policies and procedures deployment |
| CC6 | CC6.3 | CC6 has 8 criteria | Medium: confirm CC6.3 covers access modification/removal |
| CC7 | CC7.4 | CC7 has 5 criteria | High: confirm CC7.4 covers incident response; CC7 numbering most uncertain in this file |
| CC9 | CC9.2 | CC9 has 2 criteria | Low: CC9.2 is widely cited as the vendor/business partner criterion |

---

### 2. CC7.4: highest-risk criterion ID in this file

CC7.4 is the criterion mapped for GV.SC-08 (supplier involvement in incident activities). Within CC7, my understanding is: CC7.1 covers detection infrastructure and vulnerability management, CC7.2 covers monitoring for anomalies, CC7.3 covers evaluation/classification of security events, CC7.4 covers incident response procedures and notification, and CC7.5 covers post-incident remediation and communication.

**Flag CC7.4 as the highest-priority verification item in this file.** Incident response is spread across CC7 criteria, and if the criterion boundary falls differently than mapped, this affects the GV.SC-08 rationale. Verify before use.

---

### 3. CC9.2 maps to ten GV.SC subcategories: this is correct, not a shortcut

CC9.2 is the single SOC 2 criterion for vendor and business partner risk management. The ten GV.SC subcategories slice the C-SCRM domain into granular program requirements (program establishment, role definition, pre-engagement due diligence, ongoing monitoring, incident integration, post-relationship management). SOC 2 addresses this entire domain through one principle-level criterion.

This has an important implication for gap analysis: **a bank can satisfy CC9.2 while still having material gaps in GV.SC program maturity.** CC9.2 establishes a floor; GV.SC-01 through GV.SC-10 collectively define a ceiling. A bank with a basic vendor list and annual reviews may satisfy CC9.2 while failing GV.SC-07 (continuous monitoring) and GV.SC-10 (post-relationship risk management).

---

### 4. GV.RR-04 maps across two criteria series: note for evidence planning

GV.RR-04 (cybersecurity in HR practices) maps to four criteria spanning the Control Environment (CC1.4, CC1.5) and Logical Access (CC6.2, CC6.3) series. In a SOC 2 examination, these criteria are tested separately by different auditor procedures. Evidence for CC1.4/CC1.5 comes from HR policies, hiring processes, and performance management documentation; evidence for CC6.2/CC6.3 comes from access provisioning and deprovisioning workflows and access review records. A bank implementing GV.RR-04 controls should map evidence to each criterion series individually, not treat them as a single evidence set.

---

### 5. GV.PO-01 and GV.PO-02 both map to CC5.3: same note as PCI DSS

Both GV.PO-01 (policy establishment) and GV.PO-02 (policy maintenance) map to CC5.3, mirroring the PCI DSS pattern where both map to 12.1.1. CC5.3 covers both the existence of policies and their maintenance. GV.PO-02 additionally maps to CC4.1 (which requires ongoing evaluation of whether policies remain adequate). For evidence purposes: documents demonstrating an initial policy publication satisfy CC5.3's GV.PO-01 dimension; evidence of an annual policy review cycle satisfies both CC5.3's maintenance requirement and CC4.1.

---

### 6. Optional categories — review for privacy-regulated institutions

No GOVERN subcategories are mapped to optional TSC categories in this file. However, practitioners assessing banks subject to GLBA Safeguards Rule, CCPA, or other privacy regulations should consider whether:

- **GV.OC-03** (legal and regulatory obligations) creates an obligation to implement the Privacy category (P-series), if personal financial information is in scope for the examination.
- **GV.OC-04** (external dependencies outward) has a partial connection to **A1.1** (Availability) if the bank's system availability commitments are defined in service-level agreements — applicable if Availability is in the examination scope.

These are not mapped in the table because they are conditional on examination scope decisions. A practitioner determining examination scope for a bank client should evaluate both of these before finalizing the SOC 2 scope.

---

### 7. Contrast with PCI DSS mapping — for Playbook use

The [PCI DSS GOVERN mapping](csf-govern-to-pci-dss-v4-0-1.md) produced 17 "no direct mapping" results. This mapping produces 1. This is not because SOC 2 is more comprehensive — it reflects the difference between a principle-based governance framework (SOC 2/COSO) and a prescriptive technical standard (PCI DSS). Neither framework fully satisfies a bank's GOVERN obligations under CSF 2.0.

For banking GRC practitioners: a bank that has both a SOC 2 Type II report and PCI DSS compliance still has GOVERN gaps. The coverage gaps that remain after both frameworks are applied are almost entirely in **GV.RM** (risk management strategy — risk appetite, ERM integration, risk communication architecture) and the depth of **GV.SC** program maturity. These gaps are where the CRI Profile's banking-specific diagnostic statements will add the most value; see the [CRI Profile GOVERN mapping](csf-govern-to-cri-profile-v2-2.md) when available.

---

*Validation log entry to be created at: `../../validation-logs/[date]-govern-soc2.md`*
*Reviewed by: [practitioner name/date — to be completed after validation]*
