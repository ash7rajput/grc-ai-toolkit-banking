# Module 1 — Multi-Framework Control Mapping Engine

This module produces cross-framework control mappings linking **NIST CSF 2.0 subcategories** to three banking-relevant target frameworks: **PCI DSS v4.0.1**, **SOC 2 Trust Services Criteria (2017, revised 2022)**, and the **CRI Financial Services Cybersecurity Profile v2.2**.

The mapping files in this module are the output of an AI-assisted workflow. Every mapping was generated using the prompt library at [`prompts/module-01-mapping-prompts.md`](../../prompts/module-01-mapping-prompts.md) and reviewed against authoritative source documents before being committed. The validation log for each mapping session is in `validation-logs/`.

---

## Frameworks and Version Pins

| Framework | Version | Authority | Notes |
|-----------|---------|-----------|-------|
| NIST CSF 2.0 | CSWP 29, February 2024 | NIST | Primary organizing framework; 6 functions, 22 categories, 106 subcategories |
| PCI DSS | v4.0.1, June 11, 2024 | PCI SSC | Required for all assessments on or after March 31, 2025; v4.0 retired December 31, 2024 |
| SOC 2 TSC | 2017, revised 2022 | AICPA | Security (CC1–CC9) is universal; Availability, Processing Integrity, Confidentiality, Privacy are optional and scope-dependent |
| CRI Profile | v2.2, 2025 | Cyber Risk Institute | 318 diagnostic statements across 7 functions (GV, ID, PR, DE, RS, RC, EX); tier-scoped |

---

## Directory Structure

```
modules/01-mapping-engine/
├── README.md                          ← this file
├── mappings/
│   ├── govern/                        ← GV function subcategories (Day 3)
│   ├── identify/                      ← ID function subcategories (Day 4)
│   ├── protect/                       ← PR function subcategories (Day 4)
│   └── detect-respond-recover/        ← DE, RS, RC function subcategories (Day 5)
└── validation-logs/                   ← manual QA findings, one log per session
```

---

## Mapping File Format

Each file in a `mappings/` subdirectory covers one NIST CSF 2.0 subcategory. Files are named by subcategory ID (e.g., `GV.OC-01.md`).

### File structure

```markdown
# [SUBCATEGORY_ID] — [SUBCATEGORY_TITLE]

**CSF 2.0 Function:** [Function name]
**CSF 2.0 Category:** [Category name]
**Subcategory outcome:** [One-sentence outcome statement]

---

## PCI DSS v4.0.1 Mapping

| PCI Req ID | Mapping Rationale | Confidence | New/Strengthened in v4.x |
|------------|-------------------|------------|--------------------------|
| ...        | ...               | High/Med/Low | Yes/No — [note if yes] |

_[2–4 sentence summary of mapping quality and practitioner caveats]_

---

## SOC 2 TSC Mapping

| TSC Criterion ID | Trust Services Category | Mapping Rationale | Confidence | Scope Note |
|-----------------|------------------------|-------------------|------------|------------|
| ...             | Security / Availability / ... | ... | High/Med/Low | [Universal or: only if [category] is in scope] |

_[2–4 sentence summary, noting whether mapped criteria are Common Criteria or optional-category]_

---

## CRI Profile v2.2 Mapping

| CRI Statement ID | CRI Function | Banking Context Note | Applies at Tier [X]? | Confidence |
|-----------------|-------------|---------------------|----------------------|------------|
| ...             | ...          | ...                  | Yes/No               | High/Med/Low |

_[2–4 sentence summary, flagging Extend function gaps and any IDs requiring verification]_

---

## Validation Status

| Check | Status | Notes |
|-------|--------|-------|
| PCI DSS IDs verified against v4.0.1 document | [Pass / Fail / Pending] | |
| SOC 2 criterion IDs verified (no invented CC#.# IDs) | [Pass / Fail / Pending] | |
| CRI diagnostic statement IDs verified against v2.2 | [Pass / Fail / Pending] | |
| Mapping rationale is specific (not generic) | [Pass / Fail / Pending] | |
| Confidence indicators are grounded | [Pass / Fail / Pending] | |
| SOC 2 optional-category scope note present where needed | [Pass / Fail / Pending] | |
| No copyrighted framework text reproduced | [Pass / Fail / Pending] | |

**Validation log entry:** [Link to entry in validation-logs/]
```

---

## Validation Workflow

The validation workflow runs in two stages: pre-commit checks performed during each mapping session, and a validation log entry recorded after each session.

### Stage 1 — Per-file checks (before committing any mapping file)

These checks are applied to every file before it moves from draft to committed state. The full rules are in [`prompts/module-01-mapping-prompts.md — Validation Rules`](../../prompts/module-01-mapping-prompts.md).

**1. Verify framework IDs against authoritative sources**

- PCI DSS: Confirm requirement numbers exist in the PCI DSS v4.0.1 document (PCI SSC Document Library, registration required). Sub-requirement numbering changed materially from v3.2.1 to v4.0; verify sub-requirements individually.
- SOC 2 TSC: Confirm criterion IDs against AICPA TSP Section 100. AI frequently invents criteria beyond the actual count within a CC series (e.g., CC6.9 does not exist). Verify the upper bound for each series.
- CRI Profile: Treat every CRI diagnostic statement ID as unverified until checked against the official CRI Profile v2.2 document at cyberriskinstitute.org. CRI is the highest-risk area for AI hallucination in this module — smaller training-data footprint than the other frameworks.

**2. Check that mapping rationale is specific**

Reject any rationale that describes the general topic area without explaining the specific control activity that creates the alignment (e.g., "both relate to access control" is not a rationale). Rationale must name what each control specifically requires and why that aligns with the CSF subcategory.

**3. Confirm confidence indicators are grounded**

A High confidence mapping must have a clear, direct correspondence — both controls describe materially the same activity in different framework vocabularies. If the correspondence requires interpretation or inference, it is at best Medium. Low confidence mappings are hypotheses, not usable mappings; treat them as requiring practitioner SME review before use.

**4. Check version and effective date accuracy**

AI output must reference PCI DSS v4.0.1 (not v4.0), SOC 2 TSC 2017 revised 2022, and CRI Profile v2.2. Version errors are a common AI failure mode on frameworks that have had multiple recent releases.

**5. Check for SOC 2 scope bleed**

Any mapping to Availability (A1), Processing Integrity (PI1), Confidentiality (C1), or Privacy (P1–P8) criteria must carry a scope note. These categories are optional; applicability depends on whether the category is in scope for the specific examination engagement.

**6. Check for copyright compliance**

AI output must not reproduce verbatim or near-verbatim text from PCI DSS, AICPA TSC, or CRI Profile documents. The prompts instruct the model to use IDs and rationale only — check compliance at review time.

---

### Stage 2 — Validation log entry (after each mapping session)

After completing a batch of mapping files in a single working session, create a validation log entry in `validation-logs/`. Name the file by date and function (e.g., `2026-05-23-govern.md`).

**Validation log structure:**

```markdown
# Validation Log — [Function(s)] — [Date]

**Session scope:** [e.g., GV.OC-01 through GV.RM-07]
**Frameworks checked:** PCI DSS v4.0.1, SOC 2 TSC 2017/2022, CRI Profile v2.2

---

## AI Errors Caught and Corrected

[List each error found during review: what AI produced, what the correct value is, and which authoritative source confirmed the correction]

## Mappings Downgraded

[List any mappings where the practitioner lowered confidence from AI-assigned High to Medium or Low, with the reason]

## Mappings Removed

[List any AI-generated mappings removed entirely because the alignment did not survive scrutiny]

## IDs Requiring Further Verification

[Any CRI or other IDs not yet verified against primary source that are marked Pending in the mapping file]

## Practitioner Notes

[Anything notable about this session's AI output quality — patterns, recurring failure modes, or observations relevant to the Playbook]
```

---

## Known Limitations

See [`prompts/module-01-mapping-prompts.md — Known Limitations`](../../prompts/module-01-mapping-prompts.md) for the full list. The primary limitations affecting use of these mapping files:

- **Mapping ≠ compliance.** A mapped ID means the control intent overlaps. Whether a specific bank's implementation satisfies the requirement requires testing, evidence review, and examiner discretion. These files document coverage alignment, not control effectiveness.

- **CRI Extend function.** The CRI Extend (EX) function addresses third-party and supply chain risk and has no direct NIST CSF 2.0 equivalent. Banks using CSF as their program spine will have structural blind spots in this area unless CRI Extend is treated as a supplemental layer. Extend gaps are flagged in the CRI mapping sections of affected files.

- **SOC 2 optional categories.** Mappings to non-CC criteria are included where the control intent aligns, but these criteria only appear in a SOC 2 report if the relevant category is in scope for the examination. Do not treat an Availability or Confidentiality mapping as universally applicable without confirming examination scope.

- **AI training data cutoff.** Requirements introduced or materially changed in the most recent framework versions may not be fully represented in AI output. The v4.0.1-specific PCI DSS sub-requirements and CRI Profile v2.2 changes are areas of elevated hallucination risk.
