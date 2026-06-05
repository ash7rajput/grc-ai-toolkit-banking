# NIST CSF 2.0 GOVERN Function — CRI Financial Services Cybersecurity Profile v2.2 Mapping

**Module:** 01 — Multi-Framework Control Mapping Engine
**Mapping direction:** NIST CSF 2.0 GOVERN (GV) → CRI Financial Services Cybersecurity Profile v2.2
**CSF source:** NIST CSWP 29, February 26, 2024 — `frameworks/nist-csf-2/csf-2-core.md`
**CRI source:** CRI Profile v2.2, 2025 — `frameworks/cri-profile-2/cri-profile-2-structure.md`; overview at https://cyberriskinstitute.org/cri-profile-overview/
**Generated:** 2026-05-24
**Status:** AI-generated draft — diagnostic statement IDs are ALL tentative; verify against CRI Profile v2.2 Mapping Catalogue before use

> **AI-assisted output — different confidence structure applies here.** The CRI Profile has a smaller public training-data footprint than NIST CSF, PCI DSS, or SOC 2. Diagnostic statement IDs and counts per subcategory cannot be verified without the official CRI Profile v2.2 Mapping Catalogue (included in the download package from cyberriskinstitute.org). **Do not use any diagnostic statement ID from this file in an assessment or client deliverable without first verifying it against the Mapping Catalogue.** The value of this file is in the Relationship and Banking Context Added columns. Treat the ID column as a navigation aid, not as verified output.

---

## Scope Notes

### This mapping is an elaboration, not a cross-framework alignment

The CRI Profile v2.2 is built directly on NIST CSF 2.0. Every CSF subcategory has at least one corresponding CRI diagnostic statement — the Profile is a banking-tailored implementation layer, not a separate control vocabulary. The Relationship column in the table below describes how CRI elaborates on each subcategory, not whether a mapping exists.

**Relationship types used:**
- **Direct equivalent** — the CRI diagnostic statement restates the CSF subcategory with minimal banking-specific addition; the frameworks are functionally equivalent on this point
- **CRI expands with additional diagnostic statements** — the CSF subcategory generates two or more CRI diagnostic statements, decomposing the CSF requirement into more granular banking-specific expectations
- **CRI scopes to banking context only** — the CRI diagnostic statement narrows the CSF subcategory to banking-specific application, with sector-specific language that reflects examiner expectations
- **CRI expands; EX function also applies** — applies exclusively to GV.SC subcategories; the CSF subcategory maps to both Govern (GV.SC) and Extend (EX) function diagnostic statements; see the Extend function note below

### Diagnostic statement ID format and uncertainty

CRI Profile v2.2 diagnostic statement IDs follow the convention `[CSF subcategory ID].[sequential number]` — for example, `GV.OC-01.1`, `GV.RM-02.3`. Where multiple statements exist for a subcategory, they are numbered from `.1` upward. The exact count per subcategory is in the Mapping Catalogue.

IDs in the table below are marked **[†]** — tentative, derived from the naming convention, not from the Catalogue. Where I cannot estimate with reasonable confidence, or where I have specific uncertainty about count or coverage, the row reads **VERIFY AGAINST CRI v2.2 MAPPING CATALOGUE** instead of a tentative ID.

The Day 2 field notes established the rule for this project: _for any framework less prominent than the top-tier standards, assume AI output requires line-by-line source verification before commit._ CRI is that framework. Every [†] ID in this file is subject to that rule.

### GV.SC subcategories: dual coverage in Govern and Extend

For all GV.SC (Supply Chain Risk Management) subcategories, two sets of CRI diagnostic statements apply:

1. **GV.SC Govern statements** — directly corresponding to the CSF GV.SC subcategory
2. **Extend (EX) function statements** — CRI's seventh function, unique to the CRI Profile and with no CSF 2.0 equivalent, providing deeper banking-specific third-party and supply chain risk requirements

The Extend function is architecturally significant: it is where CRI adds the most banking-specific content with no CSF parallel. Vendor concentration risk, critical service provider classification (core banking, payment processors, cloud), and FFIEC outsourcing guidance expectations are primarily captured in Extend. The full Extend function mapping is a separate file not yet created; this file notes EX coverage in every GV.SC row as a forward pointer.

### Tier applicability is not stated in this file

The CRI tier model affects which diagnostic statements apply to a given institution:

Tier    Diagnostic statements
Tier 1    All 318 statements
Tier 3    282 statements
Tier 4    208 statements Tier applicability for specific statements requires the Mapping Catalogue. As a general guidance: the most demanding Govern expectations — board-approved risk appetite documentation, formal C-SCRM programs, quantified performance metrics — are more likely to appear at Tier 1/2 scope than Tier 4. Community banks (Tier 4) should verify which GV.RM and GV.SC statements are in their applicable scope before using this file for assessment.

---

## Mapping Table

> **Copyright notice:** CRI Financial Services Cybersecurity Profile v2.2 content — including diagnostic statement text, tiering assignments, and the Mapping Catalogue — is proprietary to the Cyber Risk Institute. Diagnostic statement text is not reproduced here. Paraphrased banking context descriptions are original language. Full diagnostic statement text must be read in the official CRI Profile v2.2 document from cyberriskinstitute.org.

**[†] = Tentative ID based on CRI naming convention — VERIFY AGAINST CRI v2.2 MAPPING CATALOGUE before use. Count of statements per subcategory is uncertain.**

| CSF Subcategory | CRI Diagnostic Statement ID(s) | Relationship | Banking Context Added by CRI | Confidence |
|:----------------|:-------------------------------|:-------------|:-----------------------------|:----------:|
| **GV.OC-01** Mission shapes cybersecurity risk decisions | GV.OC-01.1 [†] | CRI expands with additional diagnostic statements | CRI grounds mission-based risk framing in the bank's charter obligations — safety and soundness, consumer protection, financial stability. For Tier 1/2 institutions, systemic importance is part of the mission context: examiners expect the cybersecurity risk program to account for sector-level impact, not only institutional impact. | MEDIUM |
| **GV.OC-02** Stakeholder cybersecurity needs factored into risk decisions | GV.OC-02.1 [†] | CRI expands with additional diagnostic statements | CRI distinguishes banking's regulatory stakeholders — OCC, Federal Reserve, FDIC, NCUA — from generic external stakeholders. Examiner expectations are supervisory obligations, not aspirational goals. CRI adds the framing that regulatory relationships are structured governance inputs requiring documented responsiveness, not optional stakeholder management activities. | MEDIUM |
| **GV.OC-03** Legal, regulatory, and contractual cybersecurity obligations identified and managed | GV.OC-03.1, GV.OC-03.2 [†] | CRI expands with additional diagnostic statements | CRI provides the densest banking-specific regulatory mapping in the GOVERN function. The obligation inventory for a U.S. bank includes: GLBA Safeguards Rule, FFIEC IT Examination Handbook series, OCC 2021 cybersecurity guidance, NYDFS Part 500 (for covered entities), PCI DSS, applicable state breach notification laws, and DORA for internationally active institutions. This is the subcategory with the highest-value CRI banking additions. | HIGH |
| **GV.OC-04** What external stakeholders depend on the organization to deliver is documented | GV.OC-04.1 [†] | CRI expands with additional diagnostic statements | CRI specifies the relevant external stakeholders for banking: depositors, payment system participants, and correspondent banking counterparties. For Tier 1/2 banks, continuity obligations extend to payment infrastructure upon which other institutions depend. CRI connects external dependency documentation to operational resilience expectations that banking examiners evaluate. | MEDIUM |
| **GV.OC-05** Critical external capabilities the organization relies on are inventoried | GV.OC-05.1, GV.OC-05.2 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI identifies the banking-specific critical dependency categories: core banking systems (e.g., core processors), payment rails (FedWire, SWIFT, ACH networks), cloud providers hosting critical systems, and correspondent banking relationships. Vendor concentration risk — where multiple institutions share the same critical provider — is a CRI/sector concept with no CSF equivalent, addressed further in the Extend function. | MEDIUM |
| **GV.RM-01** Risk management objectives defined and endorsed by stakeholders | GV.RM-01.1 [†] | CRI expands with additional diagnostic statements | CRI adds that risk management objectives must be formally board-approved and aligned with the bank's capital plan and liquidity risk management framework. Examiner guidance treats undocumented or management-only risk objectives as a governance gap; board approval is the baseline expectation. | MEDIUM |
| **GV.RM-02** Risk appetite and tolerance documented and shared | GV.RM-02.1, GV.RM-02.2, GV.RM-02.3 [†] | CRI expands with additional diagnostic statements | Board-approved cyber risk appetite documentation is one of the most frequently cited examination findings for banks. CRI adds specific requirements absent from CSF: the appetite statement must be quantified where practicable, integrated with enterprise risk appetite, address banking-specific risk categories (payment fraud, ransomware against critical systems, third-party failure), and the board must demonstrate understanding — not just approval — of the thresholds. Multiple diagnostic statements are expected here given the banking regulatory depth. | HIGH |
| **GV.RM-03** Cybersecurity risk activities embedded in enterprise risk management | GV.RM-03.1, GV.RM-03.2 [†] | CRI expands with additional diagnostic statements | CRI adds the three-lines-of-defense structure that banking regulators expect: first-line business unit risk ownership, second-line independent risk function oversight of cybersecurity, and third-line internal audit validation. OCC Handbook guidance on enterprise risk management defines the examiner baseline. A cybersecurity program that sits entirely in IT without second-line oversight is a governance finding in banking. | MEDIUM |
| **GV.RM-04** Acceptable risk response options communicated to decision-makers | GV.RM-04.1 [†] | CRI expands with additional diagnostic statements | CRI adds that risk acceptance decisions for significant cybersecurity risks require board or senior management approval with documented rationale reviewable by examiners. Risk transfer strategies (cyber insurance) are addressed with banking-specific nuance: coverage gap analysis is expected given the complexity of cyber insurance policy exclusions. | MEDIUM |
| **GV.RM-05** Organization-wide risk reporting channels defined | GV.RM-05.1, GV.RM-05.2 [†] | CRI expands with additional diagnostic statements | CRI adds mandatory regulatory notification channels: OCC incident notification rule (effective May 2022 — banks must notify OCC within 36 hours of a significant computer security incident), FDIC equivalent notification requirements, FinCEN SAR filing obligations, and applicable state notification rules. These are not optional governance channels — they are mandatory regulatory obligations with specific timelines and formats that must be built into the risk communication architecture. | HIGH |
| **GV.RM-06** Risk prioritization methodology standardized | GV.RM-06.1, GV.RM-06.2 [†] | CRI expands with additional diagnostic statements | CRI adds that the methodology must be documented, defensible to examiners, and connected to the bank's Risk and Control Self-Assessment (RCSA) process with second-line risk function review. The methodology must specifically address banking sector threat priorities: payment fraud, ransomware targeting core banking systems, and third-party compromise of critical service providers. | MEDIUM |
| **GV.RM-07** Upside risks and strategic opportunities recognized and included | VERIFY AGAINST CRI v2.2 MAPPING CATALOGUE | Direct equivalent (uncertain — verify) | The banking regulatory framework does not emphasize opportunity-based risk management for cybersecurity. CRI may treat this as a direct equivalent to CSF without significant banking addition, or the diagnostic statement may address this in limited scope. This is the GV subcategory where the relationship type is most uncertain. Confirm statement existence, tier applicability, and whether banking-specific content is present before using in an assessment. | LOW |
| **GV.RR-01** Leadership visibly accountable for cybersecurity risk | GV.RR-01.1, GV.RR-01.2, GV.RR-01.3 [†] | CRI expands with additional diagnostic statements | Board cybersecurity governance is a primary focus of banking technology examinations. CRI adds: requirements for independent board member cybersecurity competency (or access to qualified advisors), cyber risk as a standing board risk committee agenda item, CISO reporting lines providing unfiltered board access, and documented board receipt and review of cybersecurity briefings. OCC Large Bank Supervision guidance and Federal Reserve SR letters on board risk governance shape these expectations. Multiple diagnostic statements are expected. | HIGH |
| **GV.RR-02** Cybersecurity roles and responsibilities clearly defined and enforced | GV.RR-02.1, GV.RR-02.2 [†] | CRI expands with additional diagnostic statements | CRI adds banking-specific role definitions and integration requirements: CISO independence from IT operations, BSA/AML Officer coordination with cybersecurity (a banking-specific control intersection), CRO integration with cybersecurity risk functions, and assignment of cybersecurity responsibilities across the three lines of defense. The distinction between IT risk management and cybersecurity risk management as separate functions is an examiner expectation captured here. | HIGH |
| **GV.RR-03** Resources allocated proportional to cybersecurity risk | GV.RR-03.1 [†] | CRI expands with additional diagnostic statements | CRI adds that resource allocation must be documented and proportional to the bank's risk profile, with adequacy reviewed by the second-line risk function. OCC IT Booklet guidance addresses staffing, budget, and tooling adequacy as components of an effective information security program. Significant or repeat examination findings in cybersecurity are frequently correlated with documented resource allocation deficiencies. | MEDIUM |
| **GV.RR-04** Cybersecurity integrated into hiring, onboarding, performance management, and separation | GV.RR-04.1, GV.RR-04.2 [†] | CRI expands with additional diagnostic statements | CRI adds banking-specific personnel security requirements: OCC Fitness and Integrity standards for institution-affiliated parties, FDIC background check expectations, separation-of-duties controls for individuals with payment system access, and immediate access revocation at separation — a specific examination scrutiny point following insider fraud incidents, which are disproportionately common in banking. | MEDIUM |
| **GV.PO-01** Formal cybersecurity policy documented and communicated | GV.PO-01.1, GV.PO-01.2 [†] | CRI expands with additional diagnostic statements | CRI adds that the cybersecurity policy must be board-approved (not management-only), must reference applicable banking regulatory requirements by name (FFIEC, GLBA, applicable OCC/FDIC/Fed guidance), and must explicitly address customer data protection, payment system security, and privileged access controls. Policy absence or inadequacy is a standard examination finding category across OCC, Fed, and FDIC supervision. | HIGH |
| **GV.PO-02** Cybersecurity policy reviewed and updated periodically | GV.PO-02.1 [†] | CRI expands with additional diagnostic statements | CRI adds that policy review must be triggered by regulatory changes — new FFIEC booklets, OCC bulletins, state cybersecurity rules — in addition to annual calendar review. Banking's regulatory change velocity makes purely calendar-driven review insufficient. Post-examination policy remediation directives are a common trigger for unscheduled policy updates that must be tracked and documented. | MEDIUM |
| **GV.OV-01** Risk management results reviewed and used to refine strategy | GV.OV-01.1, GV.OV-01.2 [†] | CRI expands with additional diagnostic statements | CRI adds board-level reporting requirements specific to banking: cybersecurity performance reporting to the board risk committee on a defined cadence, integration of audit and examination findings into risk management strategy updates, and documented board action on risk committee recommendations. OCC guidance on board oversight of technology risk and Federal Reserve guidance on board governance shape the examiner standards here. | HIGH |
| **GV.OV-02** Risk management strategy periodically reassessed for sufficiency | GV.OV-02.1 [†] | CRI expands with additional diagnostic statements | CRI adds that strategy sufficiency assessment must specifically incorporate most recent supervisory examination findings, emerging threats relevant to the bank's risk profile, and material changes to the bank's business model or technology stack. The assessment must be documented and reviewed by the board, incorporating input from internal audit and the second-line risk function. | MEDIUM |
| **GV.OV-03** Cybersecurity performance measured and evaluated | GV.OV-03.1, GV.OV-03.2 [†] | CRI expands with additional diagnostic statements | CRI adds specific KPI/KRI expectations that banking examiners request as evidence of effective governance: vulnerability management metrics (open findings by age and severity), patch compliance rates, security awareness completion rates, third-party risk assessment completion, and incident response performance metrics. Formal cybersecurity scorecards reported to the board are an increasingly standard examiner evidence request. | HIGH |
| **GV.SC-01** Formal C-SCRM program established | GV.SC-01.1, GV.SC-01.2 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds that the C-SCRM program must be board-approved and must specifically address vendor concentration risk as a distinct risk category. The CRI tier model creates materially different C-SCRM expectations: Tier 1/2 banks have significantly more demanding program requirements than Tier 4 community banks. Critical service provider categories are enumerated in the Extend function. FFIEC Outsourcing Technology Services Booklet shapes baseline examiner expectations. | HIGH |
| **GV.SC-02** Supply chain cybersecurity responsibilities defined and communicated | GV.SC-02.1 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds that responsibility allocation with critical vendors must comply with FFIEC third-party risk guidance: right-to-audit provisions, incident notification requirements (vendor contracts must reflect the bank's 36-hour OCC notification obligation), and sub-outsourcing controls. Banking regulators hold the bank — not its vendors — accountable for vendor compliance with regulatory requirements. | HIGH |
| **GV.SC-03** C-SCRM integrated with cybersecurity and enterprise risk programs | GV.SC-03.1 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds that C-SCRM findings must be reported to the board risk committee and integrated with enterprise risk reporting. A TPRM program that operates separately from board governance — with findings that do not reach the board — is a documented examination gap. Integration with the RCSA process and risk committee reporting cadence is the expected architecture. | MEDIUM |
| **GV.SC-04** Suppliers inventoried and ranked by criticality | GV.SC-04.1, GV.SC-04.2 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds vendor concentration risk assessment as a required component of the inventory process — specifically assessing whether the bank's reliance on a vendor is shared by many other institutions (sector-level concentration), not just whether the vendor is critical to the bank individually. Tier 1/2 banks are expected to assess their contribution to sector-level concentration risk, which goes beyond the CSF inventory and prioritization requirement. | HIGH |
| **GV.SC-05** Cybersecurity requirements embedded in supplier contracts | GV.SC-05.1, GV.SC-05.2 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds that banking vendor contracts must include: right to audit, access to security documentation (SOC reports, penetration test results), incident notification requirements aligned with the bank's regulatory obligations, data return and destruction provisions, subcontracting approval requirements, and geographic data processing restrictions. These reflect the FFIEC Outsourcing Technology Services Booklet baseline expectations. | HIGH |
| **GV.SC-06** Due diligence before formalizing new supplier relationships | GV.SC-06.1, GV.SC-06.2 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds that due diligence must be tiered to vendor criticality, with board or senior management approval required before onboarding critical vendors. Examination findings frequently cite insufficient pre-engagement due diligence for core banking system replacements and cloud migrations — two of the highest-risk vendor onboarding events in banking. | HIGH |
| **GV.SC-07** Supplier risks continuously monitored throughout the relationship | GV.SC-07.1, GV.SC-07.2 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds monitoring frequency expectations tied to vendor criticality: critical vendors (core banking, payment processors, cloud) require more frequent review cycles than commodity vendors. Review must include vendor-provided SOC reports, penetration testing results, and changes to subcontracting arrangements. Continuous monitoring via vendor risk signals — news, regulatory actions against the vendor, financial distress indicators — is expected for Tier 1/2 banks. | HIGH |
| **GV.SC-08** Key suppliers included in incident planning, response, and recovery | GV.SC-08.1 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds that critical vendors must be included in tabletop exercises and that contracts must define joint incident response communication procedures. The OCC 36-hour notification rule creates specific coordination obligations when a vendor is party to a computer security incident — pre-agreed communication protocols with critical vendors are now a regulatory expectation, not a best practice. | MEDIUM |
| **GV.SC-09** Supply chain security practices woven into cybersecurity program | GV.SC-09.1 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds that supply chain security must be tracked through the full technology lifecycle — acquisition, deployment, operation, and decommissioning — with particular attention to cloud-hosted core banking systems and payment infrastructure spanning multiple third parties. Banking's long technology refresh cycles (core banking systems often run for 10–20 years) make lifecycle management a specific examination concern that CSF does not address with this specificity. | MEDIUM |
| **GV.SC-10** Post-relationship cybersecurity risk managed | GV.SC-10.1 [†]; EX function diagnostic statements also apply [†] | CRI expands; EX function also applies | CRI adds banking-specific post-relationship requirements: data portability and return/destruction obligations for core banking data (a regulatory concern during core banking migrations), immediate revocation of all vendor system access, updating the bank's risk profile to reflect the removed vendor, and assessing whether the transition creates new concentration risk (migrating to a vendor already serving many institutions). Core banking system migrations are among the highest-risk transitions in banking operations. | MEDIUM |

---

## Mapping Summary

| Relationship Type | Count | Notes |
|:------------------|:-----:|:------|
| CRI expands with additional diagnostic statements | 20 | All non-GV.SC subcategories except GV.RM-07 |
| CRI expands; EX function also applies | 10 | All GV.SC subcategories — dual coverage in Govern + Extend |
| Direct equivalent (uncertain — verify) | 1 | GV.RM-07 — relationship type unverified |
| No CRI counterpart | 0 | Expected: CRI is built on CSF, all subcategories should have coverage |
| **Total** | **31** | |

| Confidence Level | Count | Subcategories |
|:-----------------|:-----:|:--------------|
| HIGH | 14 | GV.OC-03, GV.RM-02, GV.RM-05, GV.RR-01, GV.RR-02, GV.PO-01, GV.OV-01, GV.OV-03, GV.SC-01, GV.SC-02, GV.SC-04, GV.SC-05, GV.SC-06, GV.SC-07 |
| MEDIUM | 16 | GV.OC-01/02/04/05, GV.RM-01/03/04/06, GV.RR-03/04, GV.PO-02, GV.OV-02, GV.SC-03/08/09/10 |
| LOW | 1 | GV.RM-07 |
| **Total** | **31** | |

> Confidence here reflects confidence in the **Relationship type and Banking Context** assessment, not in the diagnostic statement IDs. All IDs carry the same verification requirement regardless of row confidence.

---

## Validation Notes

### 1. No diagnostic statement ID in this file is verified

The CRI Profile has the smallest training-data footprint of the four frameworks in this toolkit. The structure file frameworks/cri-profile-2/cri-profile-2-structure.md contains no individual statement IDs. Every [†]-marked ID in this file is a prediction based on the naming convention, not a confirmed mapping.

**Before using any row in an assessment:** download the CRI Profile v2.2 and its Mapping Catalogue from cyberriskinstitute.org (free registration required); locate the NIST CSF 2.0 → CRI mapping tab; and confirm: (a) the statement ID, (b) the number of diagnostic statements for the subcategory, and (c) the tier applicability for each statement.

**Flag for the validation log:** record every ID that was confirmed, corrected, or not found, with the version of the Mapping Catalogue used. This is the highest-priority verification task in Module 1.

---

### 2. GV.RM-07 relationship type is uncertain

GV.RM-07 (upside/opportunity risk) is the only GOVERN subcategory where I am uncertain whether a CRI diagnostic statement exists and, if so, what banking context it adds. The banking regulatory framework does not emphasize opportunity-based risk management for cybersecurity, and this subcategory may receive only a direct equivalent treatment in CRI, or may be a low-tier-only statement, or may be absent.

**Practitioner action:** Locate GV.RM-07 in the CRI Mapping Catalogue and confirm: (1) does a diagnostic statement exist? (2) Which tiers does it apply to? (3) Does the banking context add anything material? Record findings in the validation log.

---

### 3. The Extend (EX) function is not covered in this file

Every GV.SC row notes that Extend function diagnostic statements also apply, but this file does not map those statements. The Extend function is architecturally distinct: its statements address third-party and supply chain risk with banking-specific depth that has no CSF 2.0 equivalent. For GV.SC subcategories:

- The GV.SC diagnostic statements in this file correspond to the GOVERN-function layer of CRI supply chain governance
- The EX diagnostic statements represent the operational third-party risk management layer — vendor due diligence procedures, contractual security requirements, ongoing monitoring mechanics

**Practitioner action:** When the Extend function mapping file is created, cross-reference GV.SC rows in this file against the EX function entries. For gap analysis of a bank's C-SCRM program, both layers are required: treating GV.SC statements alone as sufficient will understate the CRI Profile's supply chain risk requirements.

---

### 4. Tier applicability shapes assessment scope materially

The CRI tier model affects which diagnostic statements are in scope for a given institution. For the GOVERN function, the following subcategories are most likely to have tier-differentiated applicability — verify in the Mapping Catalogue:

- **GV.RM-02** (risk appetite): Formal board-approved quantified risk appetite is likely a Tier 1/2 requirement; Tier 4 expectations may be less prescriptive
- **GV.RR-01** (leadership accountability): Board competency requirements are likely more demanding at Tier 1/2
- **GV.OV-03** (performance measurement): Formal metrics dashboards and KRI reporting to the board are more likely Tier 1/2 expectations
- **GV.SC-01, GV.SC-04** (C-SCRM program, vendor concentration): Vendor concentration risk assessment as a distinct category is likely a higher-tier requirement

Community bank practitioners (Tier 4): do not assume this file's Banking Context Added descriptions apply uniformly to your program: verify tier applicability before using any GV row as an assessment criterion.

---

### 5. Contrast with PCI DSS and SOC 2 mappings — for Playbook use

This file documents what CRI adds ON TOP OF the CSF subcategory. The [PCI DSS mapping](csf-govern-to-pci-dss-v4-0-1.md) and [SOC 2 mapping](csf-govern-to-soc2-tsc.md) document which external framework controls align with the CSF subcategory. The three files serve different purposes:

- **Use the PCI DSS file** when assessing payment security control coverage and examiner obligations for cardholder data environments
- **Use the SOC 2 file** when scoping vendor due diligence, contract requirements, or third-party assurance against CSF GOVERN controls
- **Use this CRI file** when assessing a bank's cybersecurity program against sector-specific examiner expectations — this is the authoritative banking-context layer

The combined picture across all three files shows: where PCI DSS and SOC 2 have gaps (e.g., risk appetite, ERM integration, oversight performance measurement), CRI diagnostic statements are the primary banking-sector accountability mechanism. Banks should not assume PCI DSS or SOC 2 compliance satisfies the GOVERN requirements that only appear in this file.

---

*Validation log entry to be created at: `../../validation-logs/[date]-govern-cri-profile.md`*
*Reviewed by: [practitioner name/date — to be completed after validation against CRI Profile v2.2 Mapping Catalogue]*
