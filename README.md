# AI-Augmented GRC Toolkit for US Banking

**Helping US banks transition from the retired FFIEC CAT to NIST CSF 2.0, augmented by AI.**

---

## Why This Exists

The FFIEC Cybersecurity Assessment Tool (CAT) was retired on August 31, 2025. It had served as the primary self-assessment framework for US depository institutions since 2015, and its retirement left many banks — particularly community banks and regional institutions — without a clear path forward. The FFIEC did not replace the CAT with a new proprietary tool; its guidance points institutions toward established industry frameworks, with NIST CSF 2.0 (released February 2024) as the most widely referenced alternative.

This repository is a working artifact library and methodology demonstration. It shows how a senior GRC practitioner can use AI tooling — specifically Claude Code and Cowork — to accelerate the CSF 2.0 transition: building control mappings, generating risk register templates, structuring third-party risk assessments, and drafting audit-ready policy documentation faster than traditional approaches allow.

This is not a SaaS product and not a competitor to Drata or Vanta. It is an open methodology and a collection of reusable artifacts. If you are a GRC practitioner navigating the same transition, the outputs here are meant to be adapted, not just read.

---

## What's Inside

### Modules

| Module | Description |
|--------|-------------|
| **Module 1** | NIST CSF 2.0 multi-framework mapping engine — maps CSF 2.0 subcategories to PCI DSS v4.0.1, SOC 2 TSC, and CRI Profile 2.0 |
| **Module 2** | Banking-specific risk register generator — produces structured risk registers aligned to CSF 2.0 functions and banking exam priorities |
| **Module 3** | Third-party risk assessment automation — TPRM questionnaire and scoring templates tied to GV.SC subcategories |
| **Module 4** | Audit evidence and policy drafting assistant — generates policy shells and evidence request lists mapped to CSF 2.0 outcomes |

### Also Included

- **Banking GRC AI Playbook** — methodology document covering how to integrate AI tooling into a GRC workflow responsibly, with prompting patterns and quality-control checkpoints

---

## Frameworks Covered

- NIST CSF 2.0 (primary organizing framework)
- PCI DSS v4.0.1
- SOC 2 Trust Services Criteria
- CRI Profile 2.0

---

## Tech Stack

- Claude Code + Claude Desktop (AI-assisted drafting and analysis)
- Cowork (multi-agent orchestration)
- Git + GitHub (version control)
- Markdown-first (all artifacts are plain text, no proprietary formats)
- Minimal Python (data processing where needed)

---

## Status

Active development. Started 2026-05-19. 14-day build.

---

## Roadmap

- [x] Day 1: Repo scaffolding, NIST CSF 2.0 overview
- [ ] Day 2: Framework data ingestion, Playbook outline
- [ ] Days 3–5: Module 1 (mapping engine)
- [ ] Days 6–7: Module 2 (risk register)
- [ ] Days 8–9: Module 3 (TPRM)
- [ ] Days 10–11: Module 4 (audit assistant)
- [ ] Day 12: Playbook consolidation
- [ ] Day 13: Repo polish + demo videos
- [ ] Day 14: LinkedIn launch

---

## Author

Ashwin — 10 years in US banking GRC.
[LinkedIn](https://www.linkedin.com/in/placeholder) *(link to be updated)*

---

## License

MIT — see [LICENSE](LICENSE).
