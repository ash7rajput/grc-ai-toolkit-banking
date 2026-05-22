# NIST CSF 2.0 Core — Complete Function, Category, and Subcategory Reference

> **Source:** National Institute of Standards and Technology (2024). *The NIST Cybersecurity Framework (CSF) 2.0.* NIST Cybersecurity White Paper (CSWP) NIST CSWP 29. https://doi.org/10.6028/NIST.CSWP.29 (Published February 26, 2024)
>
> **Structure:** 6 Functions · 22 Categories · 106 Subcategories
>
> **Note on numbering:** Subcategory IDs are not sequential by design. Gaps (e.g., ID.AM-06, PR.DS-03 through PR.DS-09) indicate subcategories from CSF 1.1 that were relocated or consolidated in CSF 2.0. All IDs in this document match Appendix A of NIST CSWP 29 exactly.
>
> **Outcome statements** in this document are paraphrased from NIST language to add interpretive clarity. For verbatim text, refer to the authoritative NIST source above.

---

# GOVERN (GV)

*The organization's cybersecurity risk management strategy, expectations, and policy are established, communicated, and monitored. GOVERN sits at the center of the CSF wheel — it informs how the other five Functions are prioritized and executed across the enterprise.*

---

## GV.OC — Organizational Context

The circumstances — mission, stakeholder expectations, dependencies, and legal, regulatory, and contractual requirements — surrounding the organization's cybersecurity risk decisions are understood.

| ID | Title | Outcome |
|----|-------|---------|
| GV.OC-01 | Mission-Informed Risk Management | The organization's mission shapes how cybersecurity risk decisions are framed and prioritized. |
| GV.OC-02 | Stakeholder Expectations | Internal and external stakeholders are identified, and their cybersecurity needs and expectations are actively factored into risk decisions. |
| GV.OC-03 | Legal and Regulatory Obligations | Legal, regulatory, and contractual cybersecurity requirements — including privacy and civil liberties obligations — are identified and actively managed. |
| GV.OC-04 | External Dependencies (Outward) | Key capabilities and services that external stakeholders depend on the organization to deliver are documented and communicated. |
| GV.OC-05 | External Dependencies (Inward) | Critical external capabilities and services the organization relies on are inventoried and their cybersecurity implications understood. |

---

## GV.RM — Risk Management Strategy

The organization's priorities, constraints, risk tolerance and appetite statements, and assumptions are established, communicated, and used to support operational risk decisions.

| ID | Title | Outcome |
|----|-------|---------|
| GV.RM-01 | Risk Objectives | Cybersecurity risk management objectives are defined and endorsed by relevant organizational stakeholders. |
| GV.RM-02 | Risk Appetite and Tolerance | The organization's risk appetite and tolerance thresholds are documented, maintained, and shared to guide risk decisions. |
| GV.RM-03 | Integration with Enterprise Risk | Cybersecurity risk activities and outcomes are embedded within the enterprise risk management (ERM) process rather than managed separately. |
| GV.RM-04 | Strategic Risk Direction | Guidance on acceptable risk response options is established and communicated to those responsible for risk decisions. |
| GV.RM-05 | Risk Communication Channels | Organization-wide communication pathways for reporting cybersecurity risks — including those from suppliers and third parties — are defined. |
| GV.RM-06 | Risk Prioritization Methodology | A consistent methodology for calculating, documenting, categorizing, and prioritizing cybersecurity risks is standardized and communicated. |
| GV.RM-07 | Positive Risk Opportunities | Upside risks (strategic opportunities) are recognized, characterized, and included in organizational cybersecurity risk discussions. |

---

## GV.RR — Roles, Responsibilities, and Authorities

Cybersecurity roles, responsibilities, and authorities to foster accountability, performance assessment, and continuous improvement are established and communicated.

| ID | Title | Outcome |
|----|-------|---------|
| GV.RR-01 | Leadership Accountability | Organizational leadership is visibly accountable for cybersecurity risk and cultivates a culture that is risk-aware, ethical, and improvement-focused. |
| GV.RR-02 | Role Clarity | Cybersecurity roles, responsibilities, and decision-making authority are clearly defined, communicated, understood, and enforced. |
| GV.RR-03 | Resource Allocation | Budget, personnel, and tools are allocated in proportion to cybersecurity risk priorities, roles, and policy commitments. |
| GV.RR-04 | Cybersecurity in HR Practices | Cybersecurity considerations are integrated into hiring, onboarding, performance management, and separation processes. |

---

## GV.PO — Policy

Organizational cybersecurity policy is established, communicated, and enforced.

| ID | Title | Outcome |
|----|-------|---------|
| GV.PO-01 | Policy Establishment | A cybersecurity risk management policy is developed from organizational context and strategy, formally documented, communicated, and enforced. |
| GV.PO-02 | Policy Maintenance | Cybersecurity policy is periodically reviewed and updated to remain current with evolving requirements, threats, technology, and organizational mission. |

---

## GV.OV — Oversight

Results of organization-wide cybersecurity risk management activities and performance are used to inform, improve, and adjust the risk management strategy.

| ID | Title | Outcome |
|----|-------|---------|
| GV.OV-01 | Strategy Outcome Review | Results of cybersecurity risk management strategy are reviewed and used to refine organizational direction and priorities. |
| GV.OV-02 | Strategy Coverage Review | The cybersecurity risk management strategy is reassessed periodically to confirm it remains sufficient for current organizational needs and risk landscape. |
| GV.OV-03 | Performance Evaluation | Cybersecurity risk management performance is measured and evaluated, with findings used to determine where adjustments are needed. |

---

## GV.SC — Cybersecurity Supply Chain Risk Management

Cyber supply chain risk management processes are identified, established, managed, monitored, and improved by organizational stakeholders.

| ID | Title | Outcome |
|----|-------|---------|
| GV.SC-01 | C-SCRM Program Establishment | A formal cybersecurity supply chain risk management (C-SCRM) program — including strategy, objectives, policies, and processes — is established and agreed upon by stakeholders. |
| GV.SC-02 | Supply Chain Roles and Responsibilities | Cybersecurity responsibilities for suppliers, customers, and partners are defined, communicated, and coordinated both internally and externally. |
| GV.SC-03 | C-SCRM Integration | C-SCRM is embedded in broader cybersecurity and enterprise risk management, risk assessment, and improvement activities. |
| GV.SC-04 | Supplier Inventory and Prioritization | The organization maintains an inventory of suppliers and ranks them by their criticality to business operations. |
| GV.SC-05 | Supply Chain Requirements | Cybersecurity requirements for supply chain relationships are established, prioritized, and embedded in contracts and other agreements. |
| GV.SC-06 | Pre-Engagement Due Diligence | Cybersecurity risk assessment and planning are conducted before formalizing new supplier or third-party relationships. |
| GV.SC-07 | Ongoing Supplier Risk Monitoring | Risks from suppliers, their products and services, and other third parties are documented, assessed, prioritized, and continuously monitored throughout the relationship. |
| GV.SC-08 | Supplier Inclusion in Incident Activities | Key suppliers and third parties are included in incident planning, response, and recovery activities. |
| GV.SC-09 | Supply Chain Security Integration | Supply chain security practices are woven into cybersecurity and enterprise risk management programs, with performance tracked across the technology lifecycle. |
| GV.SC-10 | Post-Relationship Risk Management | C-SCRM plans address cybersecurity risk activities that continue or arise after a supplier relationship or service agreement concludes. |

---

# IDENTIFY (ID)

*The organization's current cybersecurity risks are understood. This Function enables an organization to prioritize its efforts consistent with its risk management strategy by understanding its assets, suppliers, and threat environment.*

---

## ID.AM — Asset Management

Assets that enable the organization to achieve business purposes are identified and managed consistent with their relative importance to organizational objectives and risk strategy.

| ID | Title | Outcome |
|----|-------|---------|
| ID.AM-01 | Hardware Inventory | A current, maintained inventory of hardware assets managed by the organization is kept up to date. |
| ID.AM-02 | Software and Services Inventory | A current inventory of software, services, and systems managed by the organization is maintained. |
| ID.AM-03 | Network Communication Mapping | Authorized network communication paths and internal and external data flows are mapped and kept current. |
| ID.AM-04 | Supplier Services Inventory | An inventory of services received from external suppliers is documented and maintained. |
| ID.AM-05 | Asset Prioritization | Assets are tiered and prioritized based on their classification, criticality, required resources, and impact on the organizational mission. |
| ID.AM-07 | Data Inventory and Metadata | Inventories of data and corresponding metadata for designated data types are documented and maintained. |
| ID.AM-08 | Asset Lifecycle Management | Systems, hardware, software, services, and data are governed and tracked throughout their full lifecycles — from acquisition through decommissioning. |

---

## ID.RA — Risk Assessment

The cybersecurity risk to the organization, its assets, and individuals is understood.

| ID | Title | Outcome |
|----|-------|---------|
| ID.RA-01 | Vulnerability Identification | Vulnerabilities in organizational assets are discovered, validated, and recorded in a structured manner. |
| ID.RA-02 | Threat Intelligence Ingestion | Cyber threat intelligence is actively received from trusted information-sharing communities and external sources. |
| ID.RA-03 | Threat Identification | Internal and external threats relevant to the organization are identified and documented. |
| ID.RA-04 | Impact and Likelihood Analysis | The likelihood and potential impact of threats exploiting known vulnerabilities are analyzed and recorded. |
| ID.RA-05 | Inherent Risk Understanding | The combined analysis of threats, vulnerabilities, likelihoods, and impacts is used to characterize inherent risk and drive prioritization of response actions. |
| ID.RA-06 | Risk Response Management | Risk responses are selected, prioritized, planned, tracked, and communicated to relevant stakeholders. |
| ID.RA-07 | Change and Exception Management | Changes and policy exceptions are assessed for risk impact, documented, and tracked through resolution. |
| ID.RA-08 | Vulnerability Disclosure Processes | Processes for receiving, analyzing, and responding to vulnerability disclosures are established and operationalized. |
| ID.RA-09 | Hardware and Software Integrity Verification | The authenticity and integrity of hardware and software are evaluated before acquisition and deployment. |
| ID.RA-10 | Critical Supplier Assessment | Critical suppliers are evaluated for cybersecurity risk before their products or services are acquired. |

---

## ID.IM — Improvement

Improvements to organizational cybersecurity risk management processes, procedures, and activities are identified across all CSF Functions.

| ID | Title | Outcome |
|----|-------|---------|
| ID.IM-01 | Evaluation-Driven Improvements | Cybersecurity process improvements are identified through assessments, audits, and formal evaluations. |
| ID.IM-02 | Test and Exercise Improvements | Security tests and exercises — including joint activities with suppliers and third parties — yield actionable improvement findings. |
| ID.IM-03 | Operations-Driven Improvements | Operational execution of processes, procedures, and activities is reviewed and improvements are identified from real-world performance. |
| ID.IM-04 | Cybersecurity Plan Maintenance | Incident response plans and other cybersecurity plans affecting operations are established, communicated, maintained, and continuously improved. |

---

# PROTECT (PR)

*Safeguards to manage the organization's cybersecurity risks are used. PROTECT supports the ability to prevent or lower the likelihood and impact of adverse cybersecurity events.*

---

## PR.AA — Identity Management, Authentication, and Access Control

Access to physical and logical assets is limited to authorized users, services, and hardware and managed commensurate with the assessed risk of unauthorized access.

| ID | Title | Outcome |
|----|-------|---------|
| PR.AA-01 | Identity and Credential Management | Identities and credentials for authorized users, services, and hardware are provisioned, managed, and revoked by the organization. |
| PR.AA-02 | Identity Proofing | Identities are verified and bound to credentials at an assurance level appropriate to the context and risk of the interaction. |
| PR.AA-03 | Authentication Enforcement | Authentication is required for users, services, and hardware before access to organizational systems is granted. |
| PR.AA-04 | Identity Assertion Protection | Identity assertions are secured in transmission, and receiving parties verify their integrity before acting on them. |
| PR.AA-05 | Access Rights Management | Access permissions and authorizations follow least privilege and separation of duties principles, are policy-defined, enforced, and regularly reviewed. |
| PR.AA-06 | Physical Access Controls | Physical access to organizational assets is controlled, monitored, and enforced commensurate with assessed risk. |

---

## PR.AT — Awareness and Training

The organization's personnel are provided with cybersecurity awareness and training so they can perform their cybersecurity-related tasks.

| ID | Title | Outcome |
|----|-------|---------|
| PR.AT-01 | General Security Awareness Training | All personnel receive cybersecurity awareness training that equips them to handle everyday tasks with an understanding of associated risks. |
| PR.AT-02 | Role-Specific Security Training | Personnel in specialized or elevated-risk roles receive targeted cybersecurity training matched to the specific knowledge and skills their responsibilities require. |

---

## PR.DS — Data Security

Data are managed consistent with the organization's risk strategy to protect confidentiality, integrity, and availability of information.

| ID | Title | Outcome |
|----|-------|---------|
| PR.DS-01 | Data-at-Rest Protection | Data stored at rest is protected for confidentiality, integrity, and availability through appropriate technical and administrative controls. |
| PR.DS-02 | Data-in-Transit Protection | Data moving across networks or between systems is protected for confidentiality, integrity, and availability through appropriate transmission safeguards. |
| PR.DS-10 | Data-in-Use Protection | Data actively being processed or accessed is protected for confidentiality, integrity, and availability through controls applied at the point of use. |
| PR.DS-11 | Backup and Recovery | Data backups are regularly created, securely stored, protected against tampering, and periodically tested to confirm recoverability. |

---

## PR.PS — Platform Security

The hardware, software, and services of physical and virtual platforms are managed consistent with the organization's risk strategy to protect their confidentiality, integrity, and availability.

| ID | Title | Outcome |
|----|-------|---------|
| PR.PS-01 | Configuration Management | Secure configuration baselines and configuration management practices are established and consistently applied across hardware, software, and services. |
| PR.PS-02 | Software Currency | Software is maintained, updated, and — when no longer needed or supportable — removed or replaced at a pace commensurate with associated risk. |
| PR.PS-03 | Hardware Currency | Hardware is maintained and replaced or decommissioned at a pace and manner that reflects associated cybersecurity risk. |
| PR.PS-04 | Log Generation | Systems generate log records in sufficient detail to support continuous monitoring, incident investigation, and compliance requirements. |
| PR.PS-05 | Unauthorized Software Prevention | Technical controls are in place to block unauthorized software from being installed or executed on organizational platforms. |
| PR.PS-06 | Secure Software Development | Secure software development practices are embedded throughout the software development lifecycle, and compliance with those practices is monitored. |

---

## PR.IR — Technology Infrastructure Resilience

Security architectures are managed with the organization's risk strategy to protect asset confidentiality, integrity, and availability, and to sustain organizational resilience.

| ID | Title | Outcome |
|----|-------|---------|
| PR.IR-01 | Network Segmentation and Access | Networks and computing environments are segmented and protected against unauthorized logical access and misuse. |
| PR.IR-02 | Environmental Threat Protection | Technology assets are protected against environmental hazards such as power failures, extreme temperatures, and physical damage. |
| PR.IR-03 | Resilience Mechanisms | Mechanisms are implemented so that systems can continue operating — or recover quickly — under both normal and adverse conditions. |
| PR.IR-04 | Capacity Management | Sufficient resource capacity is provisioned and managed to sustain required availability levels for critical systems and services. |

---

# DETECT (DE)

*Possible cybersecurity attacks and compromises are found and analyzed. DETECT enables the timely discovery and analysis of anomalies, indicators of compromise, and other adverse events.*

---

## DE.CM — Continuous Monitoring

Assets are monitored to find anomalies, indicators of compromise, and other potentially adverse events.

| ID | Title | Outcome |
|----|-------|---------|
| DE.CM-01 | Network Monitoring | Network traffic and services are continuously monitored for indicators of anomalous or potentially malicious activity. |
| DE.CM-02 | Physical Environment Monitoring | The physical operating environment is monitored for conditions that could signal a security event or compromise. |
| DE.CM-03 | Personnel and Device Activity Monitoring | User behavior and technology usage are observed to surface deviations from established norms or acceptable use policies. |
| DE.CM-06 | External Service Provider Monitoring | Activities and outputs of external service providers are monitored for signs of compromise or adverse events. |
| DE.CM-09 | Endpoint and Runtime Monitoring | Computing hardware, software, runtime environments, and their data are monitored for indicators of tampering or unauthorized activity. |

---

## DE.AE — Adverse Event Analysis

Anomalies, indicators of compromise, and other potentially adverse events are analyzed to characterize them and detect cybersecurity incidents.

| ID | Title | Outcome |
|----|-------|---------|
| DE.AE-02 | Event Analysis | Detected anomalies and suspicious events are analyzed in depth to understand their nature, origin, and associated threat activity. |
| DE.AE-03 | Event Correlation | Event data from multiple detection sources is correlated to produce a unified, coherent picture of potential threats. |
| DE.AE-04 | Impact and Scope Estimation | The estimated business and operational impact and scope of an adverse event are evaluated and documented. |
| DE.AE-06 | Event Notification | Timely, relevant information about adverse events is disseminated to authorized personnel and security tooling. |
| DE.AE-07 | Threat Intelligence Integration | Cyber threat intelligence and relevant contextual information are incorporated into the analysis and triage of adverse events. |
| DE.AE-08 | Incident Declaration | When adverse events satisfy predefined incident criteria, they are formally declared as cybersecurity incidents and escalated accordingly. |

---

# RESPOND (RS)

*Actions regarding a detected cybersecurity incident are taken. RESPOND supports the ability to contain the effects of cybersecurity incidents through structured management, analysis, communication, and mitigation.*

---

## RS.MA — Incident Management

Responses to detected cybersecurity incidents are managed.

| ID | Title | Outcome |
|----|-------|---------|
| RS.MA-01 | Incident Response Plan Execution | Upon incident declaration, the incident response plan is activated and executed in coordination with relevant internal and external parties. |
| RS.MA-02 | Incident Triage and Validation | Incoming incident reports are reviewed, triaged for validity, and assessed for appropriate response action. |
| RS.MA-03 | Incident Categorization and Prioritization | Confirmed incidents are categorized by type and prioritized by severity to guide resource allocation and response activities. |
| RS.MA-04 | Incident Escalation | Incidents are escalated to higher management, specialist teams, or external authorities as warranted by severity or complexity. |
| RS.MA-05 | Recovery Initiation Criteria | Predefined criteria for transitioning from response to recovery activities are evaluated and applied at the appropriate time. |

---

## RS.AN — Incident Analysis

Investigations are conducted to ensure effective response and to support forensics and recovery activities.

| ID | Title | Outcome |
|----|-------|---------|
| RS.AN-03 | Root Cause Analysis | Root cause analysis is conducted to establish what occurred during the incident, how it unfolded, and what conditions enabled it. |
| RS.AN-06 | Investigative Action Records | All investigative actions are logged, and the integrity and chain of custody of those records are maintained and preserved. |
| RS.AN-07 | Evidence Collection and Preservation | Incident artifacts and associated metadata are collected and preserved in a manner that maintains their integrity and supports potential legal proceedings. |
| RS.AN-08 | Incident Magnitude Assessment | The overall magnitude and business impact of the incident are estimated through structured analysis and validated with available evidence. |

---

## RS.CO — Incident Response Reporting and Communication

Response activities are coordinated with internal and external stakeholders as required by laws, regulations, or policies.

| ID | Title | Outcome |
|----|-------|---------|
| RS.CO-02 | Stakeholder Notification | Relevant internal and external stakeholders — including regulators, partners, and affected parties — are notified of incidents in accordance with applicable requirements. |
| RS.CO-03 | Information Sharing | Incident-related information is shared with designated internal and external parties to support coordinated response and shared situational awareness. |

---

## RS.MI — Incident Mitigation

Activities are performed to prevent expansion of an event and mitigate its effects.

| ID | Title | Outcome |
|----|-------|---------|
| RS.MI-01 | Incident Containment | Affected systems and network segments are isolated or otherwise contained to prevent the incident from spreading further. |
| RS.MI-02 | Incident Eradication | The root cause and persistence mechanisms of the incident are eliminated from all affected systems and environments. |

---

# RECOVER (RC)

*Assets and operations affected by a cybersecurity incident are restored. RECOVER supports timely restoration of normal operations and appropriate communication during recovery efforts.*

---

## RC.RP — Incident Recovery Plan Execution

Restoration activities are performed to ensure operational availability of systems and services affected by cybersecurity incidents.

| ID | Title | Outcome |
|----|-------|---------|
| RC.RP-01 | Recovery Plan Activation | The recovery phase of the incident response plan is initiated at the appropriate trigger point and executed according to documented procedures. |
| RC.RP-02 | Recovery Action Execution | Specific recovery actions are identified, scoped, sequenced, and carried out to restore affected systems and services to operational status. |
| RC.RP-03 | Backup and Restoration Asset Integrity | Backup and restoration assets are verified for integrity before being used to restore production systems. |
| RC.RP-04 | Post-Incident Operational Norms | Recovery decisions account for mission-critical functions and cybersecurity risk management objectives to establish appropriate post-incident operating norms. |
| RC.RP-05 | Restored Asset Verification | The integrity of restored systems and services is verified and confirmed to be operating correctly before they are returned to full production status. |
| RC.RP-06 | Recovery Closure and Documentation | Incident recovery is formally declared closed using predefined criteria, and all incident-related documentation is completed. |

---

## RC.CO — Incident Recovery Communication

Restoration activities are coordinated with internal and external parties.

| ID | Title | Outcome |
|----|-------|---------|
| RC.CO-03 | Recovery Status Communication | Progress and status of recovery activities are communicated to designated internal and external stakeholders throughout the restoration process. |
| RC.CO-04 | Public Recovery Updates | Public-facing updates about incident recovery are issued through approved communication channels using pre-reviewed messaging. |

---

## Summary Reference

| Function | ID | Categories | Subcategories |
|----------|----|------------|---------------|
| Govern | GV | 6 (GV.OC, GV.RM, GV.RR, GV.PO, GV.OV, GV.SC) | 31 |
| Identify | ID | 3 (ID.AM, ID.RA, ID.IM) | 21 |
| Protect | PR | 5 (PR.AA, PR.AT, PR.DS, PR.PS, PR.IR) | 22 |
| Detect | DE | 2 (DE.CM, DE.AE) | 11 |
| Respond | RS | 4 (RS.MA, RS.AN, RS.CO, RS.MI) | 13 |
| Recover | RC | 2 (RC.RP, RC.CO) | 8 |
| **Total** | | **22** | **106** |

---

> **Source:** National Institute of Standards and Technology (2024). *The NIST Cybersecurity Framework (CSF) 2.0.* NIST CSWP 29. https://doi.org/10.6028/NIST.CSWP.29
>
> This document paraphrases NIST CSF 2.0 outcome statements to provide interpretive value. All subcategory IDs match NIST CSWP 29 Appendix A exactly. Gaps in subcategory numbering are intentional — they reflect CSF 1.1 subcategories relocated or consolidated in CSF 2.0.
