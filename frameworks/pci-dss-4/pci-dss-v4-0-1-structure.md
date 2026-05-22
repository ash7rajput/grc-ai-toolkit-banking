# PCI DSS v4.0.1 — Structure Reference

## Overview

**Payment Card Industry Data Security Standard (PCI DSS) v4.0.1** is the current version of the global security standard for protecting payment card account data. It was published by the **PCI Security Standards Council (PCI SSC)** on **June 11, 2024** as a minor revision to v4.0 (originally released March 31, 2022), incorporating clarifications and corrections raised by the assessor and stakeholder community.

### Timeline and Effective Dates

| Version | Published | Status |
|---------|-----------|--------|
| v3.2.1 | May 2018 | Retired March 31, 2024 |
| v4.0 | March 31, 2022 | Retired December 31, 2024 |
| **v4.0.1** | **June 11, 2024** | **Current. Required for all assessments on or after March 31, 2025** |

_All dates verified against PCI Security Standards Council official communications, June 2024 and subsequent._

All new assessments on or after March 31, 2025 must use v4.0.1. v4.0 was retired on December 31, 2024 and may no longer be used as the basis for new assessments.

A subset of new requirements introduced in v4.0/v4.0.1 were designated **"best practices"** until March 31, 2025, after which they became **fully mandatory**.

### Key Changes from v3.2.1

- **Expanded authentication controls** — multi-factor authentication (MFA) now required for all access into the cardholder data environment (CDE), not just remote access (Req 8).
- **Customized approach** — organizations may now satisfy the intent of a requirement using alternative controls, documented and validated by a Qualified Security Assessor (QSA), instead of the defined approach.
- **Targeted risk analysis** — entities must perform formal risk analyses to justify the frequencies chosen for certain periodic activities (e.g., log review, vulnerability scanning intervals).
- **Stronger encryption and key management** — explicit requirements for key custodian acknowledgement, cryptographic cipher suites, and TLS 1.2+ minimums (Req 4).
- **Phishing-resistant MFA** — new sub-requirements for phishing-resistant authentication mechanisms for privileged access (Req 8.6).
- **Ecommerce / client-side security** — new controls for managing scripts loaded in payment pages (Req 6.4, Req 11.6).
- **Logging and monitoring enhancements** — automated mechanisms required for log reviews; failure of critical security controls must trigger alerts (Req 10).
- **Roles and responsibilities** — every requirement now explicitly requires documented assignment of roles and responsibilities.

---

## The 12 PCI DSS Requirements

| # | Requirement Title |
|---|-------------------|
| 1 | Install and maintain network security controls |
| 2 | Apply secure configurations to all system components |
| 3 | Protect stored account data |
| 4 | Protect cardholder data with strong cryptography during transmission over open, public networks |
| 5 | Protect all systems and networks from malicious software |
| 6 | Develop and maintain secure systems and software |
| 7 | Restrict access to system components and cardholder data by business need to know |
| 8 | Identify users and authenticate access to system components |
| 9 | Restrict physical access to cardholder data |
| 10 | Log and monitor all access to system components and cardholder data |
| 11 | Test security of systems and networks regularly |
| 12 | Support information security with organizational policies and programs |

The 12 requirements are organized under six **Goals** (formerly "Control Objectives"):

1. **Build and Maintain a Secure Network and Systems** — Req 1–2
2. **Protect Account Data** — Req 3–4
3. **Maintain a Vulnerability Management Program** — Req 5–6
4. **Implement Strong Access Control Measures** — Req 7–9
5. **Regularly Monitor and Test Networks** — Req 10–11
6. **Maintain an Information Security Policy** — Req 12

---

## Copyright Notice

> The full text of PCI DSS v4.0.1, including all requirement statements, testing procedures, and guidance, is **copyright © 2006–2024 PCI Security Standards Council, LLC**. It is not reproduced in this toolkit.
>
> To read or download the official standard, visit the **PCI SSC Document Library**:
> **https://www.pcisecuritystandards.org/document_library/**
>
> Free registration on the PCI SSC portal is required to download the standard. The document is provided at no cost.

---

## How This Is Used in This Toolkit

This file serves as a structural index and orientation guide for the PCI DSS v4.0.1 framework within the GRC AI Toolkit — Banking.

**Module 1** will produce a mapping that links **NIST CSF 2.0 subcategories** (e.g., `PR.AC-01`, `DE.CM-04`) to specific **PCI DSS v4.0.1 requirement IDs and section numbers** (e.g., `Req 8.2.1`, `Req 10.4.1`). Each mapping entry will include:

- The CSF 2.0 subcategory identifier and short title
- The corresponding PCI DSS requirement number(s) and section reference
- A brief, original-language note explaining *why* the two controls align — written by toolkit contributors, not sourced from the standard
- An indication of whether the PCI requirement was newly introduced or strengthened in v4.0.1 versus v3.2.1

This approach allows practitioners to:

1. Use CSF 2.0 as the organizing framework for a bank's overall cybersecurity program
2. Cross-walk directly to PCI DSS obligations without reproducing copyrighted text
3. Understand the *intent* of each PCI requirement at a level sufficient to assess coverage gaps

Full requirement text must always be read in the official PCI SSC document. Toolkit mappings do not constitute legal or compliance advice and should be validated by a qualified assessor.
