# Module 1 — Multi-Framework Control Mapping Engine

This module maps NIST CSF 2.0 subcategories to three banking-relevant 
frameworks: PCI DSS v4.0.1, SOC 2 Trust Services Criteria (2017, revised 
2022), and the CRI Financial Services Cybersecurity Profile v2.2.

Each mapping is generated with the prompt library at 
prompts/module-01-mapping-prompts.md, then reviewed by a GRC practitioner 
against authoritative sources before commit. Validation findings are 
recorded in validation-logs/.

## Frameworks and Version Pins

| Framework | Version | Authority | Notes |
|-----------|---------|-----------|-------|
| NIST CSF 2.0 | CSWP 29, Feb 2024 | NIST | Primary framework; 6 functions, 22 categories, 106 subcategories |
| PCI DSS | v4.0.1, June 11, 2024 | PCI SSC | Required for assessments on/after March 31, 2025; v4.0 retired Dec 31, 2024 |
| SOC 2 TSC | 2017, revised 2022 | AICPA | Security (CC1–CC9) universal; A1, PI1, C1, P1–P8 optional and scope-dependent |
| CRI Profile | v2.2, 2025 | Cyber Risk Institute | 318 diagnostic statements, 7 functions (GV, ID, PR, DE, RS, RC, EX), tier-scoped |

## Directory Structure

modules/01-mapping-engine/
- README.md (this file)
- mappings/
  - govern/
    - csf-govern-to-pci-dss-v4-0-1.md
    - csf-govern-to-soc2-tsc.md
    - csf-govern-to-cri-profile-v2-2.md
  - identify/ (Day 4)
  - protect/ (Day 4)
  - detect-respond-recover/ (Day 5)
- validation-logs/

## Mapping File Format

One file per CSF function per target framework. Each file is a crosswalk 
table. Rows are the CSF subcategories for that function. Columns are the 
target framework requirement IDs, the mapping rationale, and a confidence 
rating.

Confidence ratings:
- HIGH: clear, direct correspondence; both controls describe the same 
  activity in different vocabularies.
- MEDIUM: partial overlap; neither framework fully covers the other.
- LOW: defensible but partial; treat as a hypothesis requiring SME review.
- No direct mapping: stated explicitly where no meaningful counterpart 
  exists. Mappings are never invented to fill rows.

## Validation Workflow

Stage 1 — Per-file checks before commit:
1. Verify framework IDs against authoritative sources. PCI DSS numbering 
   changed materially from v3.2.1 to v4.0.1; verify sub-requirements 
   individually. SOC 2: confirm criterion IDs against AICPA TSP Section 
   100 (AI invents IDs like CC6.9 that do not exist; verify the upper 
   bound of each CC series). CRI: treat every diagnostic statement ID as 
   unverified until checked against the official CRI Profile v2.2 
   document. CRI is the highest hallucination risk in this module.
2. Mapping rationale must be specific. Reject generic rationale like 
   "both relate to access control." Name the specific control activity 
   that creates the alignment.
3. Confidence must be grounded. HIGH requires direct correspondence. If 
   it requires interpretation, it is MEDIUM at best.
4. Version accuracy: PCI DSS v4.0.1 (not v4.0), SOC 2 TSC 2017/2022, CRI 
   Profile v2.2.
5. SOC 2 scope check: any mapping to A1, PI1, C1, or P1–P8 must carry a 
   scope note, since these categories are optional and depend on 
   examination scope.
6. Copyright check: no verbatim framework text. IDs and rationale only.

Stage 2 — Validation log after each session:
After completing a function's mappings, create a log in validation-logs/ 
named by date and function (e.g., 2026-05-21-govern.md), recording: AI 
errors caught and corrected, mappings downgraded, mappings removed, IDs 
still pending verification, and practitioner notes on AI output quality.

## Known Limitations

- Mapping is not compliance. A mapped ID means control intent overlaps. 
  Whether a bank's implementation satisfies the requirement needs testing, 
  evidence, and examiner discretion. These files document coverage 
  alignment, not control effectiveness.
- CRI Extend (EX) function addresses third-party and supply chain risk 
  and has no direct NIST CSF 2.0 equivalent. Banks using CSF as their 
  spine have a structural blind spot here unless Extend is added as a 
  supplemental layer.
- SOC 2 optional categories only appear in a report if in scope for the 
  examination. Do not treat an Availability or Confidentiality mapping as 
  universally applicable.
- AI training cutoff: the newest framework requirements (PCI DSS v4.0.1 
  sub-requirements, CRI v2.2 changes) carry elevated hallucination risk.

## Status

- GOVERN (GV): complete. PCI DSS, SOC 2, and CRI Profile mappings, 
  manually QA'd.
- IDENTIFY (ID): pending (Day 4)
- PROTECT (PR): pending (Day 4)
- DETECT, RESPOND, RECOVER (DE/RS/RC): pending (Day 5)
