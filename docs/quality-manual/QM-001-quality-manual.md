---
id: QM-001
title: Quality Manual
status: approved
author: quality@example.com
reviewers:
  - management
approvers:
  - ceo
training:
  required_departments:
    - Quality
    - Engineering
    - Regulatory
    - Clinical
    - Security
  training_mode: acknowledge
  due_days: 14
---

# QM-001: Quality Manual

## 1. QMS Scope & Application

This Quality Management System (QMS) applies to the design, development, release, and maintenance of Software as a Medical Device (SaMD) products. The QMS covers all activities from user needs identification through post-market surveillance.

The organization operates as a SaMD company and does not manufacture physical medical devices. All production activities relate to software build, deployment, and distribution.

## 2. Normative References

| Standard | Title |
| --- | --- |
| ISO 13485:2016 | Medical devices — Quality management systems — Requirements for regulatory purposes |
| IEC 62304:2006+A1:2015 | Medical device software — Software life cycle processes |
| ISO 14971:2019 | Medical devices — Application of risk management to medical devices |
| IEC 62366-1:2015+A1:2020 | Medical devices — Application of usability engineering to medical devices |
| IEC 81001-5-1:2021 | Health software — Security for health IT products |
| EU MDR 2017/745 | Regulation on medical devices |
| 21 CFR Part 820 | Quality System Regulation (FDA) |
| 21 CFR Part 11 | Electronic records; Electronic signatures (FDA) |

## 3. Exclusions

The following ISO 13485:2016 clauses are excluded with justification:

| Clause | Title | Justification |
| --- | --- | --- |
| 6.4.2 | Contamination control | Not applicable — no physical product to contaminate |
| 7.5.2 | Cleanliness of product | Not applicable — no physical product |
| 7.5.5 | Sterile medical device requirements | Not applicable — software is not sterilized |
| 7.5.7 | Sterilization validation | Not applicable — no sterilization processes |
| 7.5.9.2 | Implantable device traceability | Not applicable — software is not implantable |

These exclusions do not affect the organization's ability or responsibility to provide medical device software that meets customer and regulatory requirements.

## 4. Quality Policy

The organization's Quality Policy is defined in [POL-001](../policies/POL-001-quality-policy.md) and is communicated to all personnel.

## 5. Quality Objectives

| Objective | Metric | Target |
| --- | --- | --- |
| Product Safety | Critical defects escaping to production | Zero |
| Regulatory Compliance | Conformance to applicable standards | 100% |
| Customer Satisfaction | Customer issue resolution time | Within 48 hours |
| Process Improvement | Process improvements per quarter | At least 2 |
| Training Compliance | Personnel training completion rate | 100% within due dates |
| CAPA Effectiveness | CAPAs closed effectively on first attempt | ≥ 90% |

Objectives are reviewed during Management Review (see [SOP-006](../sops/SOP-006-management-review.md)).

## 6. Organization & Responsibilities

| Role | Responsibilities |
| --- | --- |
| Top Management | Provide resources, set quality policy, conduct management reviews |
| Quality Management Representative | Maintain QMS, report to management, ensure regulatory compliance |
| Quality Department | Document control, audits, CAPA management, training administration |
| Engineering Department | Design, development, testing, deployment of SaMD products |
| Regulatory Department | Regulatory strategy, submissions, post-market surveillance |
| Clinical Department | Clinical evaluation, clinical evidence management |
| Security Department | Cybersecurity risk management, vulnerability management |

## 7. Document Hierarchy

```
Quality Manual (QM-001)
├── Policies (POL-xxx)
│   └── POL-001 Quality Policy
├── Standard Operating Procedures (SOP-xxx)
│   ├── SOP-001 Document Control
│   ├── SOP-002 Design & Development
│   ├── ...
│   └── SOP-020 Product Preservation & Labeling
├── Work Instructions (WI-xxx)
│   ├── WI-001 GitHub PR Review
│   ├── WI-002 Document Approval
│   └── WI-003 Release Signing
└── Records & Reports
    ├── Audit Reports (AUD-xxx)
    └── Quality Records
```

## 8. Process Interaction Map

| Process | Inputs | Outputs | Owner | Key SOPs |
| --- | --- | --- | --- | --- |
| Document Control | Document drafts, change requests | Approved documents, revision history | Quality | SOP-001, SOP-005 |
| Design & Development | User needs, regulatory requirements | Design outputs, verified software | Engineering | SOP-002, SOP-013, SOP-015 |
| Risk Management | Hazard identification, use scenarios | Risk management file, residual risk evaluation | Engineering | SOP-003 |
| Purchasing | Supplier requirements | Qualified suppliers, verified components | Quality | SOP-009 |
| Production (Build & Deploy) | Verified software, release criteria | Released product, deployment records | Engineering | SOP-014 |
| Customer Feedback | Customer communications | Feedback analysis, complaint records | Quality | SOP-010 |
| CAPA | Nonconformances, audit findings | Corrective actions, effectiveness evidence | Quality | SOP-004 |
| Internal Audit | Audit program, QMS processes | Audit findings, improvement opportunities | Quality | SOP-008 |
| Management Review | Process data, audit results | Improvement decisions, resource allocation | Management | SOP-006 |
| Training | Competency requirements, SOP updates | Training records, competency evidence | Quality | SOP-007 |
| Regulatory Reporting | Incidents, complaints | Vigilance reports, advisory notices | Regulatory | SOP-012 |
| Post-Market Surveillance | Market data, clinical evidence | PMS reports, safety updates | Regulatory | SOP-019 |
| Data Analysis | Process metrics, quality data | Trend reports, improvement inputs | Quality | SOP-016 |

## 9. Clause-to-Document Cross-Reference

| ISO 13485 Clause | Title | Covering Document(s) |
| --- | --- | --- |
| 4.1 | General QMS requirements | QM-001 |
| 4.1.6 | Computer software validation | SOP-017 |
| 4.2.2 | Quality Manual | QM-001 |
| 4.2.3 | Medical device file | SOP-002 |
| 4.2.4 | Document control | SOP-001 |
| 4.2.5 | Control of records | SOP-005 |
| 5.1 | Management commitment | QM-001, POL-001 |
| 5.3 | Quality policy | POL-001 |
| 5.4.1 | Quality objectives | QM-001 |
| 5.5.1 | Responsibility and authority | QM-001 |
| 5.6 | Management review | SOP-006 |
| 6.2 | Human resources | SOP-007 |
| 6.3 | Infrastructure | SOP-018 |
| 6.4 | Work environment | SOP-018 |
| 7.1 | Planning of product realization | SOP-002, SOP-003 |
| 7.2 | Customer-related processes | SOP-010 |
| 7.3 | Design and development | SOP-002, SOP-013 |
| 7.3.9 | Design changes | SOP-015 |
| 7.4 | Purchasing | SOP-009 |
| 7.5.1 | Production and service provision | SOP-014 |
| 7.5.4 | Servicing | SOP-013 |
| 7.5.6 | Process validation | SOP-014, SOP-017 |
| 7.5.8 | Identification | SOP-014 |
| 7.5.9 | Traceability | SOP-002, SOP-013 |
| 7.5.11 | Preservation of product | SOP-020 |
| 8.2.1 | Feedback | SOP-010 |
| 8.2.2 | Complaint handling | SOP-010 |
| 8.2.3 | Regulatory reporting | SOP-012 |
| 8.2.4 | Internal audit | SOP-008 |
| 8.3 | Nonconforming product | SOP-011 |
| 8.3.3 | Advisory notices | SOP-012 |
| 8.4 | Data analysis | SOP-016 |
| 8.5.2 | Corrective action | SOP-004 |
| 8.5.3 | Preventive action | SOP-004 |

## References

- [POL-001](../policies/POL-001-quality-policy.md) — Quality Policy
- [SOP-001](../sops/SOP-001-document-control.md) through [SOP-020](../sops/SOP-020-preservation-labeling.md) — Standard Operating Procedures
- ISO 13485:2016
