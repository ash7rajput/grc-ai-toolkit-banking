# SOC 2 Trust Services Criteria — Structure Reference

## Overview

**SOC 2 (System and Organization Controls 2)** is an auditing framework developed and maintained by the **American Institute of Certified Public Accountants (AICPA)**. It evaluates whether a service organization's controls meet the **Trust Services Criteria (TSC)**, which define the requirements for security, availability, processing integrity, confidentiality, and privacy of a system.

### Publication History

| Version | Published | Status |
|---------|-----------|--------|
| Trust Services Principles and Criteria (TSPC) | 2009 | Superseded |
| TSC 2017 | April 2017 | Baseline |
| **TSC 2017, revised** | **2022** | **Current — applicable to all SOC 2 examinations** |

The 2022 revision incorporated minor updates and alignment with the **COSO 2013 Internal Control — Integrated Framework**, which underpins the Common Criteria series. The TSC is published in the AICPA's *Attestation Standards* and is updated periodically via codification; auditors reference the version in effect at the examination date.

### SOC 2 vs. SOC 1 vs. SOC 3

- **SOC 1** — Internal controls over financial reporting (ICFR); governed by SSAE 18.
- **SOC 2** — Security and operational controls; governed by AT-C Section 205 and the TSC.
- **SOC 3** — Public-facing summary report based on a SOC 2 examination; same criteria, restricted distribution removed.

SOC 2 reports are issued as **Type I** (design of controls at a point in time) or **Type II** (design and operating effectiveness over a period, typically 6–12 months). Banking counterparties and regulators almost universally require Type II reports.

---

## The 5 Trust Services Categories

| # | Category | Criteria Series | Inclusion |
|---|----------|-----------------|-----------|
| 1 | **Security** | Common Criteria (CC1–CC9) | **Universal** — present in every SOC 2 report |
| 2 | **Availability** | A-series (A1) | Optional — scope determined by service commitments |
| 3 | **Processing Integrity** | PI-series (PI1) | Optional — applicable where accuracy and completeness of processing matters |
| 4 | **Confidentiality** | C-series (C1) | Optional — applicable where confidential information is held or processed |
| 5 | **Privacy** | P-series (P1–P8) | Optional — applicable where personal information is collected, used, retained, disclosed, or disposed of |

Security is the only universally included category in a SOC 2 examination. The Common Criteria (CC1 through CC9) form the Security category and appear in every SOC 2 report. The remaining four categories — Availability, Processing Integrity, Confidentiality, and Privacy — are optional. The service organization selects them based on its service commitments and system requirements, and the auditor evaluates only the categories that are in scope for the engagement.

_SOC 2 is a voluntary attestation, not a regulatory mandate. Scope is driven by service commitments and system requirements documented by the service organization._

---

## Common Criteria (CC) Series

The Common Criteria are organized into nine series, aligned to the five components of the **COSO Internal Control — Integrated Framework** plus AICPA-specific operational and risk controls.

| Series | Name | Summary |
|--------|------|---------|
| **CC1** | Control Environment | Establishes the tone and foundation for internal control: organizational structure, commitment to integrity and ethical values, board oversight, and assignment of authority and responsibility. |
| **CC2** | Communication and Information | Governs how the entity obtains, generates, and uses relevant information, and how it communicates internally and externally — including to users, vendors, and regulators. |
| **CC3** | Risk Assessment | Requires the entity to identify and analyze risks to achieving its objectives, including fraud risk, and to establish a basis for determining how those risks should be managed. |
| **CC4** | Monitoring Activities | Addresses ongoing and separate evaluations used to determine whether controls are present and functioning, and whether findings are communicated and acted on in a timely manner. |
| **CC5** | Control Activities | Covers the policies and procedures deployed to bring about management's directives, including technology general controls, segregation of duties, and authorization controls. |
| **CC6** | Logical and Physical Access Controls | The most granular series for information security: access provisioning and deprovisioning, authentication, encryption, transmission protection, and physical security of assets. |
| **CC7** | System Operations | Addresses detection and response to security events and incidents: vulnerability management, anomaly detection, incident response, and business continuity / recovery. |
| **CC8** | Change Management | Controls over the process of authorizing, designing, developing, testing, approving, and implementing changes to infrastructure, data, software, and procedures. |
| **CC9** | Risk Mitigation | Focuses on how the entity identifies and manages risks through vendor/business-partner management (including third-party service providers) and business disruption risk mitigation strategies. |

Within each series, individual criteria are numbered sequentially (e.g., **CC6.1**, **CC6.2**, … **CC6.8**). Points of Focus — illustrative control activities drawn from COSO — are listed under each criterion but are not themselves requirements; they guide how auditors evaluate whether a criterion is met.

---

## Copyright Notice

> The full text of the AICPA Trust Services Criteria, including all criterion statements, points of focus, and supplemental guidance, is **copyright © American Institute of Certified Public Accountants**. It is not reproduced in this toolkit.
>
> The authoritative source is the AICPA's publication:
> **_Trust Services Criteria for Security, Availability, Processing Integrity, Confidentiality, and Privacy_ (2017, with 2022 updates)**
>
> The document is available through the **AICPA & CIMA Online Store** and the **AICPA Library**:
> **https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services**
>
> Practitioners performing SOC 2 examinations must reference the official publication. This toolkit does not constitute audit guidance and should not be used as a substitute for the authoritative criteria.

---

## How This Is Used in This Toolkit

This file serves as a structural index and orientation guide for the SOC 2 Trust Services Criteria within the GRC AI Toolkit — Banking.

**Module 1** will produce a mapping that links **NIST CSF 2.0 subcategories** (e.g., `PR.AC-01`, `DE.CM-04`) to specific **SOC 2 TSC criterion IDs** (e.g., `CC6.1`, `CC7.2`). Each mapping entry will include:

- The CSF 2.0 subcategory identifier and short title
- The corresponding TSC criterion ID(s) — drawn from the Common Criteria or applicable additional category series
- A brief, original-language note explaining the control alignment — written by toolkit contributors, not sourced from the AICPA publication
- An indication of whether the criterion is Common Criteria (universal) or belongs to an additional category (scoped)

This approach allows banking practitioners to:

1. Use CSF 2.0 as the organizing spine for their cybersecurity program
2. Identify which SOC 2 criteria a given CSF control activity satisfies — supporting vendor due diligence, contract requirements, and third-party risk assessments
3. Understand control intent without reproducing copyrighted criterion text

Full criterion text, points of focus, and auditor guidance must always be read in the official AICPA publication. Toolkit mappings do not constitute attestation or audit advice and should be reviewed with a licensed CPA firm conducting the examination.
