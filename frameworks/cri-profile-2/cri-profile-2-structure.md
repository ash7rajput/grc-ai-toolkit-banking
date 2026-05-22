# CRI Profile v2.2 — Structure Reference

## Overview

The **Cyber Risk Institute (CRI) Financial Services Cybersecurity Profile** is a sector-specific cybersecurity framework purpose-built for financial institutions. It was developed by a coalition of major financial trade associations and member firms — including the Bank Policy Institute (BPI), Financial Services Information Sharing and Analysis Center (FS-ISAC), and others — under the CRI umbrella.

**Profile v2.2** is the current public version, built on **NIST CSF 2.0** (released February 2024), updating and superseding Profile 1.2 (which was based on NIST CSF 1.1).

### Purpose and Design Goals

The CRI Profile exists because NIST CSF 2.0 is a general-purpose framework, while financial institutions operate under a distinct regulatory environment and systemic risk considerations. The CRI Profile bridges that gap by mapping CSF 2.0 subcategories to financial-sector diagnostic statements, using a four-tier impact model to scale expectations by institution type and significance.

### Version History

| Version | CSF Basis | Published | Status |
|---------|-----------|-----------|--------|
| Profile 1.0 | NIST CSF 1.1 | 2019 | Superseded |
| Profile 1.2 | NIST CSF 1.1 | 2021 | Superseded |
| Profile v2.0 | NIST CSF 2.0 | February 2024 | Superseded |
| Profile v2.1 | NIST CSF 2.0 | April 15, 2025 | Superseded — added DORA mapping; restructured Examples of Effective Evidence |
| **Profile v2.2** | **NIST CSF 2.0** | **2025** | **Current** |

---

## Relationship to NIST CSF 2.0

The CRI Profile is best understood as a **banking-tailored implementation layer** on top of NIST CSF 2.0, not a replacement or competing framework.

### Structural Alignment

CSF 2.0 subcategories map to CRI diagnostic statements, with some subcategories expanding into multiple diagnostic statements. The general hierarchy is:

```
NIST CSF 2.0 Function
  └── Category
        └── Subcategory (e.g., PR.AA-01)
              └── CRI Diagnostic Statement(s)
```

The CRI Profile v2.2 contains **318 total diagnostic statements** across its seven functions.

### Tiering Model (Firm-Size Scoping)

The CRI Profile uses a **four-tier impact classification** to determine which diagnostic statements are in scope for a given firm. Tier assignment is based on systemic impact, with factors including firm size, interconnectedness, and the nature of services provided.

| Tier | Indicative Profile | Diagnostic Statements in Scope |
|------|--------------------|-------------------------------|
| **Tier 1** | Nationally or super-nationally systemic institutions (e.g., G-SIBs, firms designated under EO 13636 Section 9) | All 318 |
| **Tier 2** | Large regional and super-regional institutions with significant sector impact | Not specified in available CRI documentation |
| **Tier 3** | Mid-sized firms — vital to the sector but with limited national impact | 282 |
| **Tier 4** | Community banks and credit unions with fewer than 1 million customers | 208 |

Higher tiers are **cumulative** — a Tier 1 firm satisfies all statements across all tiers. A Tier 4 firm is assessed only against the 208 Tier 4 statements.

### Regulatory Alignment

The CRI Profile v2.2 Mapping Catalogue contains approximately **40 mappings** to regulatory references and industry standards. Confirmed mappings include **NIST CSF 2.0** (the framework's structural basis) and **DORA** (EU Digital Operational Resilience Act, added in v2.1 for internationally active institutions). For the complete mapping catalogue, refer to the official CRI documentation at the link in the Sources section below.

---

## CRI Profile Functions

Profile v2.2 aligns with the six NIST CSF 2.0 functions and adds a seventh, **Extend**, for third-party and supply chain risk management. Extend is unique to the CRI Profile and has no direct CSF 2.0 equivalent.

| Function | Summary | CRI-Specific Context |
|----------|---------|----------------------|
| **Govern** (GV) | Establishes and monitors cybersecurity risk management strategy, expectations, and policy | Board-level cyber risk appetite; regulatory reporting obligations |
| **Identify** (ID) | Understands current cybersecurity risks to the organization's assets, data, and capabilities | Financial data asset classification; business impact analysis for critical financial services |
| **Protect** (PR) | Safeguards to manage cybersecurity risks and ensure delivery of critical services | Authentication for privileged financial system access; encryption of payment and account data |
| **Detect** (DE) | Identifies the occurrence of cybersecurity events | Anomaly detection in transaction monitoring; fraud signal integration with security operations |
| **Respond** (RS) | Actions regarding detected cybersecurity incidents | Regulatory notification timelines; coordination with FS-ISAC and sector ISAOs |
| **Recover** (RC) | Restores capabilities or services impaired by a cybersecurity incident | Recovery objectives for payment and settlement functions; post-incident regulatory reporting |
| **Extend** (EX) | Third-party and supply chain risk management — unique to the CRI Profile | Vendor concentration risk; critical service provider classification (cloud, core banking, payment processors); contractual cyber obligations |

---

## Copyright Notice

> The full text of the CRI Financial Services Cybersecurity Profile v2.2, including all diagnostic statements, tiering assignments, and the Mapping Catalogue, is **proprietary to the Cyber Risk Institute**. It is not reproduced in this toolkit.
>
> Use of the CRI Profile is subject to the terms published on the CRI website. Practitioners performing regulatory examinations or gap assessments must reference the official document.

---

## Sources

- CRI Profile overview and download: **https://cyberriskinstitute.org/cri-profile-overview/**
- CRI Profile v2 Guidebook (April 2024 public release) — available via the CRI website
- CRI Profile v2 Mapping Catalogue — included in the official Profile download package

_Detailed diagnostic statement text is owned by the Cyber Risk Institute and is not reproduced in this toolkit. All claims in this file are sourced from publicly available CRI documentation._

---

## How This Is Used in This Toolkit

This file serves as the structural orientation guide for the CRI Profile v2.2 within the GRC AI Toolkit — Banking.

**Module 1** leverages the CRI Profile as the **banking-tailored layer on top of NIST CSF 2.0**. Rather than mapping CSF subcategories to regulatory frameworks directly, the toolkit uses the CRI Profile as an intermediate translation layer, reflecting how financial institutions and their regulators — including OCC, Federal Reserve, FDIC, NCUA, state regulators, SEC, and CFTC — use these frameworks together.

The mapping structure in Module 1 will be:

```
NIST CSF 2.0 Subcategory
  ├── CRI Profile v2.2 Diagnostic Statement(s)      ← banking-specific scoping
  ├── PCI DSS v4.0.1 Requirement (where applicable) ← payment security obligations
  └── SOC 2 TSC Criterion (where applicable)        ← third-party assurance
```

Each Module 1 entry for a CRI-mapped item will include:

- The CSF 2.0 subcategory identifier and title
- The CRI diagnostic statement ID(s) that correspond to it
- The applicable **CRI tier(s)** — indicating the institutional scope for the control
- A brief, original-language note on the banking-specific control context — written by toolkit contributors
- Any regulatory citation from the CRI Mapping Catalogue that is particularly relevant to U.S. banking examinations

This structure allows practitioners to:

1. Understand a CSF 2.0 subcategory in terms of what it means in a banking context
2. Identify tier-appropriate control expectations without over-engineering for a tier that does not apply
3. Cross-walk to PCI DSS and SOC 2 within a single mapping artifact, reducing the overhead of maintaining separate framework gap analyses
