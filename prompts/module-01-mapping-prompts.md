# Module 1 — Multi-Framework Mapping Prompt Library

## Purpose and Usage

This file contains the reusable prompt templates for the **Module 1 mapping engine** of the GRC AI Toolkit — Banking. Each prompt is designed to be copy-pasted into a capable AI model (Claude Sonnet or equivalent), with the bracketed placeholder values replaced by the practitioner before submission.

### What this file is for

Module 1 produces a cross-framework control mapping that links **NIST CSF 2.0 subcategories** to three banking-relevant frameworks: **PCI DSS v4.0.1**, **SOC 2 Trust Services Criteria (TSC 2017, revised 2022)**, and the **CRI Financial Services Cybersecurity Profile v2.2**. The prompts in this file generate the raw mapping output. A human practitioner reviews, corrects, and finalizes all output before it is committed to any mapping artifact.

### Inputs expected

Each prompt requires the practitioner to supply:

- A **NIST CSF 2.0 subcategory ID** in the format `FUNCTION.CATEGORY-##` (e.g., `PR.AA-01`, `GV.OC-03`, `DE.CM-06`)
- For Prompt 4 (gap analysis): a **list of CSF 2.0 subcategory IDs** the bank claims to implement, plus the bank's **CRI tier** (Tier 1–4)

### Outputs produced

Each prompt returns:

- Matching control IDs in the target framework (requirement numbers, criterion IDs, or diagnostic statement IDs)
- A mapping rationale for each match — a brief explanation of why the CSF subcategory and the target control align
- A confidence indicator for each mapping: **High** (direct, well-documented correspondence), **Medium** (partial or inferential alignment), or **Low** (weak or contested alignment that requires practitioner judgment)

### Before you use these prompts

Read the framework structure files before prompting. Each prompt references specific IDs, tier counts, and version numbers that will produce better output if the model has been oriented to the correct framework structure:

- `frameworks/nist-csf-2/csf-2-overview.md`
- `frameworks/pci-dss-4/pci-dss-v4-0-1-structure.md`
- `frameworks/soc2-tsc/soc2-tsc-structure.md`
- `frameworks/cri-profile-2/cri-profile-2-structure.md`

Apply the validation rules and known limitations sections at the bottom of this file to every output before committing results.

---

## Prompt 1 — Map a Single NIST CSF 2.0 Subcategory to PCI DSS v4.0.1

**Use when:** You have a specific CSF 2.0 subcategory and need to identify the PCI DSS v4.0.1 requirements that address the same control intent.

**Replace before use:** `[CSF_SUBCATEGORY_ID]` and `[CSF_SUBCATEGORY_TITLE]`

```
You are a GRC analyst producing a cross-framework control mapping for a financial institution.

Task: Map the NIST CSF 2.0 subcategory below to the corresponding PCI DSS v4.0.1 requirements.

INPUT:
- CSF 2.0 Subcategory ID: [CSF_SUBCATEGORY_ID]
- CSF 2.0 Subcategory Title: [CSF_SUBCATEGORY_TITLE]

INSTRUCTIONS:
1. Identify all PCI DSS v4.0.1 requirements that address the same control intent as the input subcategory. Use the format Req X.Y.Z (e.g., Req 8.2.1, Req 10.4.1).
2. For each match, provide:
   a. The PCI DSS requirement number and section reference
   b. A one-to-two sentence mapping rationale explaining specifically why this requirement aligns with the CSF subcategory — not a generic statement
   c. A confidence indicator: High, Medium, or Low
   d. Whether the requirement was newly introduced or materially strengthened in v4.0/v4.0.1 versus v3.2.1 (yes/no, with brief note if yes)
3. If no PCI DSS requirement directly addresses this subcategory, state that explicitly rather than forcing a weak mapping.
4. Do not reproduce full PCI DSS requirement text. Use requirement IDs and section references only. Full text is copyrighted by PCI SSC.

OUTPUT FORMAT:
Return a markdown table with columns: PCI Req ID | Mapping Rationale | Confidence | New/Strengthened in v4.x

After the table, add a brief paragraph (2–4 sentences) summarizing the overall mapping quality and any caveats a practitioner should know before relying on this output.
```

---

## Prompt 2 — Map a Single NIST CSF 2.0 Subcategory to SOC 2 TSC

**Use when:** You need to identify which SOC 2 Trust Services Criteria a given CSF 2.0 subcategory satisfies — for vendor due diligence, contract language, or third-party risk assessment purposes.

**Replace before use:** `[CSF_SUBCATEGORY_ID]` and `[CSF_SUBCATEGORY_TITLE]`

```
You are a GRC analyst producing a cross-framework control mapping for a financial institution.

Task: Map the NIST CSF 2.0 subcategory below to the corresponding SOC 2 Trust Services Criteria (TSC 2017, revised 2022, published by AICPA).

INPUT:
- CSF 2.0 Subcategory ID: [CSF_SUBCATEGORY_ID]
- CSF 2.0 Subcategory Title: [CSF_SUBCATEGORY_TITLE]

INSTRUCTIONS:
1. Identify all SOC 2 TSC criteria that address the same control intent as the input subcategory. Use the format CC#.# for Common Criteria (e.g., CC6.1, CC7.2), A1.# for Availability, PI1.# for Processing Integrity, C1.# for Confidentiality, and P#.# for Privacy.
2. For each match, provide:
   a. The TSC criterion ID
   b. A one-to-two sentence mapping rationale explaining specifically why this criterion aligns with the CSF subcategory
   c. A confidence indicator: High, Medium, or Low
   d. The Trust Services Category the criterion belongs to (Security/Common Criteria, Availability, Processing Integrity, Confidentiality, or Privacy) — note that only Security/CC criteria are universal; all others are scoped by the examination engagement
3. If no TSC criterion directly addresses this subcategory, state that explicitly.
4. Do not reproduce full AICPA criterion text or Points of Focus. Use criterion IDs only. Full text is copyrighted by AICPA.

OUTPUT FORMAT:
Return a markdown table with columns: TSC Criterion ID | Trust Services Category | Mapping Rationale | Confidence | Scope Note

After the table, add a brief paragraph (2–4 sentences) summarizing the overall mapping quality and noting whether the mapped criteria are Common Criteria (universal to every SOC 2 report) or belong to optional categories that must be explicitly scoped into an examination.
```

---

## Prompt 3 — Map a Single NIST CSF 2.0 Subcategory to CRI Profile v2.2

**Use when:** You need to understand what a CSF 2.0 subcategory requires in a banking examination context, and which CRI Profile v2.2 diagnostic statements and tiers apply.

**Replace before use:** `[CSF_SUBCATEGORY_ID]`, `[CSF_SUBCATEGORY_TITLE]`, and `[CLIENT_TIER]` (Tier 1, 2, 3, or 4)

```
You are a GRC analyst producing a cross-framework control mapping for a financial institution.

Task: Map the NIST CSF 2.0 subcategory below to the corresponding CRI Financial Services Cybersecurity Profile v2.2 diagnostic statements.

INPUT:
- CSF 2.0 Subcategory ID: [CSF_SUBCATEGORY_ID]
- CSF 2.0 Subcategory Title: [CSF_SUBCATEGORY_TITLE]
- Client CRI Tier: [CLIENT_TIER]

CONTEXT:
- CRI Profile v2.2 contains 318 total diagnostic statements across seven functions: Govern (GV), Identify (ID), Protect (PR), Detect (DE), Respond (RS), Recover (RC), and Extend (EX — third-party and supply chain risk, unique to CRI).
- Tier 1 firms apply all 318 statements. Tier 3 firms apply 282. Tier 4 firms apply 208. Tier 2 count is not specified in available public documentation.
- CSF 2.0 subcategories map to CRI diagnostic statements; some subcategories expand into multiple diagnostic statements.
- CRI Profile v2.2 Mapping Catalogue contains approximately 40 regulatory and standards mappings.

INSTRUCTIONS:
1. Identify the CRI Profile v2.2 diagnostic statement(s) that correspond to the input CSF subcategory.
2. For each match, provide:
   a. The CRI diagnostic statement ID (e.g., PR.AA-01.1)
   b. The CRI function it belongs to
   c. A one-to-two sentence description of what the diagnostic statement addresses in a banking context — written in original language, not reproduced from CRI documentation
   d. Whether the statement applies at the client's stated tier
   e. A confidence indicator: High, Medium, or Low
3. Flag any diagnostic statements that fall within the Extend (EX) function, as these address third-party and supply chain risk and have no direct CSF 2.0 equivalent.
4. If you are uncertain of a specific diagnostic statement ID, say so explicitly rather than guessing. Diagnostic statement IDs should be verified against the official CRI Profile v2.2 document before use in a formal assessment.
5. Do not reproduce full CRI diagnostic statement text. That content is proprietary to the Cyber Risk Institute.

OUTPUT FORMAT:
Return a markdown table with columns: CRI Diagnostic Statement ID | CRI Function | Banking Context Note | Applies at [CLIENT_TIER]? | Confidence

After the table, add a brief paragraph noting any mapping gaps, statements requiring Extend function coverage, and any IDs that require verification against the official CRI document before use in an examination context.
```

---

## Prompt 4 — Multi-Framework Gap Analysis for a Banking Client

**Use when:** A bank has provided a list of CSF 2.0 subcategories it claims to implement, and you need to identify gaps and overlaps across all four frameworks simultaneously.

**Replace before use:** `[CLIENT_NAME_OR_PLACEHOLDER]`, `[CLIENT_TIER]`, and `[CSF_SUBCATEGORY_LIST]`

```
You are a GRC analyst performing a multi-framework gap analysis for a financial institution.

Task: Given the list of NIST CSF 2.0 subcategories the client claims to implement, identify gaps and overlaps across PCI DSS v4.0.1, SOC 2 TSC (2017/2022), and CRI Profile v2.2.

INPUT:
- Client: [CLIENT_NAME_OR_PLACEHOLDER]
- CRI Tier: [CLIENT_TIER]
- CSF 2.0 Subcategories Claimed as Implemented:
[CSF_SUBCATEGORY_LIST]
(Format: one subcategory ID per line, e.g., PR.AA-01, DE.CM-04, GV.OC-02)

CONTEXT:
- PCI DSS v4.0.1 (current, required for all assessments on or after March 31, 2025)
- SOC 2 TSC 2017 revised 2022 (AICPA); Security/Common Criteria CC1–CC9 are universal; other categories are scoped
- CRI Profile v2.2 (seven functions: GV, ID, PR, DE, RS, RC, EX); 318 total diagnostic statements; tier-scoped

INSTRUCTIONS:
1. For each claimed CSF subcategory, identify the corresponding controls in all three target frameworks (PCI DSS, SOC 2, CRI). Flag where a single CSF subcategory maps to multiple requirements in a target framework.

2. Identify GAPS — CSF subcategories not claimed by the client that nonetheless carry significant obligations under one or more target frameworks. Prioritize gaps by severity: Critical (likely to generate an examination finding or audit deficiency), Significant (material control weakness), or Advisory (good practice, not exam-critical).

3. Identify OVERLAPS — instances where a single implemented CSF subcategory satisfies requirements across multiple target frameworks simultaneously. These represent efficiency opportunities.

4. Identify CRI EXTEND GAPS — any third-party/supply chain risk areas (CRI Extend function) that are not covered by the client's submitted CSF subcategory list. These have no direct CSF 2.0 equivalent and are easy to miss in a CSF-based program.

5. Do not reproduce full requirement or criterion text from any framework. Use IDs and section references only.

6. Do not make judgments about the client's actual control effectiveness. This analysis covers claimed scope only. Effectiveness requires testing.

OUTPUT FORMAT:

Section 1 — Subcategory-to-Framework Mapping Summary
A markdown table: CSF Subcategory | PCI DSS Req(s) | SOC 2 Criterion/Criteria | CRI Diagnostic Statement(s) | Notes

Section 2 — Identified Gaps
A list grouped by severity (Critical / Significant / Advisory). For each gap: the missing CSF subcategory or framework control, which framework(s) it affects, and a one-sentence explanation of why it matters.

Section 3 — Overlap Opportunities
A list of CSF subcategories where implementation satisfies two or more target frameworks simultaneously.

Section 4 — CRI Extend Coverage Check
A brief assessment of whether the client's submitted subcategory list addresses third-party and supply chain risk at the level expected for their stated CRI tier.

Section 5 — Analyst Notes
Flag any mappings with Low confidence, any IDs that require verification against official framework documents, and any areas where bank-specific risk tolerance would change the gap prioritization.
```

---

## Validation Rules

Apply these checks to every AI output before committing any mapping to a project artifact or sharing with a client.

### 1. Verify framework IDs against authoritative sources

AI will sometimes generate plausible-looking but incorrect IDs. Before relying on any mapping output:

- **PCI DSS:** Confirm requirement numbers (e.g., Req 8.2.1) exist in the official PCI DSS v4.0.1 document. Download from the PCI SSC Document Library (registration required). Pay particular attention to sub-requirements — section numbering changed materially from v3.2.1 to v4.0.
- **SOC 2 TSC:** Confirm criterion IDs (e.g., CC6.1) against the AICPA Trust Services Criteria publication (TSP Section 100). The number of criteria within each CC series varies; AI sometimes invents criteria beyond the actual count (e.g., CC6.9 does not exist).
- **CRI Profile:** Confirm diagnostic statement IDs against the official CRI Profile v2.2 document from cyberriskinstitute.org. This is the highest-risk area for AI hallucination — the CRI Profile has a smaller training-data footprint than the other frameworks. Treat any CRI diagnostic statement ID as unverified until checked against the source document.

### 2. Check that mapping rationale is specific, not generic

A valid mapping rationale names the specific control activity that creates the alignment. Reject rationale that:

- Describes the general topic area without explaining the control link (e.g., "both relate to access control" is not a rationale)
- Could apply to any subcategory in the same CSF function
- Uses hedging language that signals uncertainty ("may relate to," "could be interpreted as") without a confidence indicator of Low

### 3. Confirm confidence indicators are grounded

A **High** confidence mapping should have a clear, direct correspondence — the two controls describe materially the same activity in different framework vocabularies. If you cannot articulate why a mapping is High without reading both source documents, downgrade it to Medium.

A **Low** confidence mapping should be treated as a hypothesis to be validated by a practitioner with subject-matter expertise in both frameworks, not as a usable mapping.

### 4. Check version and effective date accuracy

Confirm outputs reference:
- PCI DSS **v4.0.1** (not v4.0, which was retired December 31, 2024)
- SOC 2 TSC **2017 revised 2022** (not prior versions)
- CRI Profile **v2.2** (not v2.0 or v2.1)

Version errors are a common AI failure mode on frameworks that have had multiple recent releases.

### 5. Check for scope bleed on SOC 2

AI frequently maps CSF subcategories to SOC 2 criteria in the Availability, Processing Integrity, Confidentiality, or Privacy categories without flagging that these categories are optional. Every mapping output that includes non-CC criteria must carry a note that applicability depends on whether that category is in scope for the client's examination engagement.

### 6. Review the analyst notes section before using gap analysis output

Prompt 4 output includes an Analyst Notes section that flags low-confidence mappings and areas requiring verification. Read this section first. Do not use any mapping flagged as requiring verification in a client deliverable until it has been verified.

---

## Known Limitations

These are areas where the AI mapping prompts in this file are structurally unable to provide reliable output. Human practitioner judgment is required — the prompts cannot substitute for it.

### Examiner and auditor judgment

The prompts produce control mappings. They do not and cannot replicate the judgment of an experienced examiner or auditor assessing whether a specific control implementation satisfies a requirement. A mapped ID does not mean the control would pass examination; it means the control intent overlaps. Testing, evidence review, and examiner discretion determine whether the requirement is actually met.

### Bank-specific risk tolerance and materiality

Gap severity in Prompt 4 output is based on general banking-sector norms. A specific bank's risk tolerance, business model, regulatory history, and examiner relationship change which gaps are genuinely critical versus advisory. A gap rated Critical in the output may be low-priority for a specific institution, and vice versa. Apply institution-specific context before presenting gap prioritizations to management.

### Ambiguous and overlapping requirements across frameworks

Some control areas are addressed differently across frameworks in ways that cannot be resolved by a mapping alone. For example:

- PCI DSS v4.0.1 Req 8 (authentication) and SOC 2 CC6 (logical access) overlap substantially but differ on scope, testing procedures, and required evidence. A CSF subcategory mapping to both does not mean a single control satisfies both simultaneously without review.
- CRI Profile Extend function diagnostic statements have no CSF 2.0 equivalent. Firms using CSF as their program spine will have structural blind spots in third-party and supply chain risk unless CRI Extend is treated as a supplemental layer.
- DORA (EU) requirements mapped in CRI Profile v2.1+ apply only to internationally active institutions operating in or providing services to EU financial entities. The prompts do not know whether DORA applies to your client.

### Recently updated framework content

AI models have training data cutoffs. Requirements introduced or materially changed in the most recent framework versions — including v4.0.1-specific PCI DSS sub-requirements and any CRI Profile v2.2 changes from v2.1 — may not be fully represented in AI output. Prompt 1 asks AI to flag newly strengthened requirements, but this check is not exhaustive. When mapping recently changed requirements, verify directly against the current framework document.

### Interpretation of the CRI Profile tier boundaries

The CRI tier model (Tier 1–4) uses a systemic impact assessment methodology that involves qualitative judgment about a firm's significance to the financial sector. The prompts accept tier as a practitioner-supplied input. AI cannot determine the correct tier for a client — that assessment must be done by the institution in consultation with its regulators or advisors. An incorrect tier input produces incorrect scope output.

### Copyright constraints on output usability

This toolkit does not reproduce framework requirement text. AI output generated by these prompts also should not reproduce copyrighted text. If an output contains verbatim or near-verbatim text from PCI DSS, AICPA TSC, or CRI Profile documents, that content must be removed before the output is used in any deliverable. The prompts instruct the model not to reproduce protected text, but compliance is not guaranteed and must be checked at review time.
