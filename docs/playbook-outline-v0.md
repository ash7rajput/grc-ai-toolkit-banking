# Banking GRC AI Playbook — Structural Outline v0

_Working outline as of Day 2. Content to be consolidated on Day 12. Section descriptions are placeholders only — each italicized line summarizes what will go there, not what is there now._

---

## 1. Executive Summary

_One paragraph. Who this Playbook is for, what it argues, and what a practitioner can do differently after reading it. Written last, after Day 12 consolidation._

---

## 2. Context: Why a Senior GRC Practitioner Needs an AI Playbook in 2026

_Sets the scene: the state of AI tooling in regulated financial services in 2026, the gap between general-purpose AI hype and the actual constraints of banking GRC work, and why a practitioner-written playbook is different from a vendor white paper._

---

## 3. Where AI Helps in Banking GRC

_Categorized inventory of tasks where AI provides measurable time savings or quality lift with acceptable risk. Categories will include:_

- _Drafting: policy language, procedure narratives, board reporting summaries_
- _Mapping: cross-framework control alignment (CSF to PCI DSS, SOC 2, CRI Profile)_
- _Summarization: regulatory guidance, examination findings, vendor audit reports_
- _Gap analysis: identifying control coverage gaps across multiple frameworks simultaneously_
- _Evidence requests: drafting RFI language for auditors and examiners_
- _Vendor questionnaires: generating and triaging third-party risk questionnaires_

---

## 4. Where AI Fails or Hallucinates

_Categorized inventory of tasks where AI output cannot be trusted without substantial human verification, or should not be attempted at all. Categories will include:_

- _Regulatory specifics: dates, version numbers, requirement IDs, retirement timelines_
- _Examiner judgment: what an OCC or Fed examiner will accept as satisfactory evidence_
- _Board communication: tone, materiality framing, legal exposure — requires practitioner authorship_
- _Risk acceptance decisions: AI cannot assess institutional risk tolerance or regulatory relationship context_
- _Niche frameworks: quality degrades sharply on frameworks underrepresented in training data_

---

## 5. Prompt Patterns That Work in Regulated Environments

_Practical prompt engineering guidance distilled from the Day 1–11 field notes. Each pattern will include a brief description, the underlying principle, and a concrete example drawn from the toolkit build._

---

## 6. Anti-Patterns and Traps

_The failure modes observed during the build — specific prompt structures, assumptions, and workflows that produced unreliable output or near-misses. Each anti-pattern will include what went wrong and how to avoid it. Drawn directly from the "Where AI failed" sections of the daily playbook notes._

---

## 7. Validation Discipline: How to Verify AI Outputs Against Authoritative Sources

_A repeatable verification protocol for GRC practitioners. Covers: which source documents to keep open while prompting, how to spot hallucinated IDs, how to QA mapping rationale for specificity, and the decision rule for when AI output requires line-by-line verification versus spot-checking. The full validation rules from Module 1 (prompts/module-01-mapping-prompts.md) will be generalized here._

---

## 8. Banking-Specific Vocabulary That Must Be Fed to AI Explicitly

_A curated glossary of terms, distinctions, and regulatory framings that AI does not apply correctly by default in a banking context — and must be supplied in the prompt or system context. Examples include: examiner vs. auditor, mandatory vs. scoped (SOC 2), CRI tier model, prudential vs. functional regulator, FFIEC CAT transition, NPI vs. MNPI._

---

## 9. Practitioner Workflow: A Recommended Day-to-Day Routine for AI-Augmented GRC Work

_A concrete, opinionated workflow for how a senior GRC practitioner integrates AI into their daily work without losing the practitioner judgment layer. Will cover: when to prompt first vs. read first, how to structure review cycles, how to document AI use for examination readiness, and how to calibrate trust in AI output by task type._

---

## 10. What This Changes About the GRC Role

_An honest assessment — not a hype piece — of what AI tooling actually changes for senior GRC practitioners in banking. Covers: what it accelerates, what it does not change, what new skills it demands (prompt engineering, AI output QA, source verification discipline), and what it does not replace (regulatory judgment, examiner relationships, risk ownership)._

---

## 11. References and Further Reading

_Authoritative sources cited throughout the Playbook, organized by framework and topic. Will include official publication links for NIST CSF 2.0, PCI DSS v4.0.1, AICPA TSC, CRI Profile v2.2, FFIEC guidance, and key regulatory rules referenced in the toolkit._

---

_Next update: Day 12 consolidation. Daily field notes source: docs/playbook-notes.md._
