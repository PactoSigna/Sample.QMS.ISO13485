---
id: SOP-008
title: Internal Audit
status: approved
author: quality
reviewers:
  - engineering
  - quality
approvers:
  - quality
training:
  required_departments:
    - Quality
  training_mode: quiz
  due_days: 30
---

# SOP-008: Internal Audit

> **Document Type**: Standard Operating Procedure
> **Regulatory Basis**: ISO 13485:2016 Section 8.2.4
> **Status**: Effective
> **Last Updated**: 2026-04-05
> **Owner**: PactoSigna Quality
> **Review Cycle**: Annual

## 1. Purpose

This procedure establishes the requirements for planning, conducting, reporting, and following up on internal audits to verify the effectiveness of the Quality Management System and ensure compliance with ISO 13485:2016, applicable regulatory requirements, and organizational procedures. It defines how PactoSigna's audit document types, compliance reporting, and CAPA integration support a structured internal audit program.

## 2. Scope

This SOP applies to all processes, departments, and activities within the QMS scope. All ISO 13485 clauses shall be audited at least once within the audit cycle. This includes:

- Document control and records management
- Design and development controls
- Risk management processes
- CAPA and quality event management
- Training and competence
- Supplier management
- Customer feedback and complaint handling
- Management review processes
- Electronic signature and Part 11 compliance

This SOP does not cover external audits conducted by regulatory bodies or certification auditors (though preparation for such audits is supported by PactoSigna's compliance reporting features).

## 3. Definitions

| Term | Definition |
| --- | --- |
| **Audit Program** | The annual schedule of audits covering the full QMS over a defined cycle, documented in PactoSigna as an `audit_schedule` document |
| **Lead Auditor** | Person responsible for planning and conducting a specific audit; must be independent of the area being audited |
| **Auditee** | Person or department being audited |
| **Major Finding** | Absence or total breakdown of a required system element |
| **Minor Finding** | Isolated lapse in compliance that does not represent a systemic failure |
| **Observation** | Opportunity for improvement that does not constitute a nonconformance |
| **Audit Report** | Formal documentation of audit results, documented in PactoSigna as an `audit_report` document |

## 4. Roles and Responsibilities

| Role | Responsibilities |
| --- | --- |
| **Quality Management Representative** | Establishes and maintains the audit program; assigns auditors; tracks findings to closure; reports audit results to management review |
| **Lead Auditor** | Plans and conducts audits; reports findings; verifies corrective action effectiveness |
| **Auditees** | Cooperates with auditors; provides access to records and processes; implements corrective actions within agreed timelines |
| **Top Management** | Reviews audit results during management review; provides resources for the audit program and corrective actions |

## 5. Procedure

### 5.1 Audit Program Planning

1. The Quality Management Representative shall establish an annual audit program as a controlled document (`audit_schedule` type) in PactoSigna.
2. The audit program shall cover all QMS processes and ISO 13485 clauses within the audit cycle.
3. Audit frequency shall be based on:

   | Factor | Higher Frequency | Lower Frequency |
   | --- | --- | --- |
   | Process risk | High-risk processes (design, CAPA, signatures) | Low-risk support processes |
   | Previous findings | Areas with major or recurring findings | Areas with clean audit history |
   | Regulatory focus | Areas under regulatory scrutiny | Stable, mature processes |
   | Change volume | Recently changed processes or procedures | Unchanged processes |

4. The audit program shall be approved by the Quality Management Representative and reviewed during management review per [SOP-006](SOP-006-management-review.md).

### 5.2 Auditor Qualification

1. Internal auditors shall complete training on ISO 19011 audit principles.
2. Auditors shall be independent of the area being audited to ensure objectivity.
3. Lead auditors shall have conducted at least 2 audits under supervision before leading independently.
4. Auditor qualifications shall be documented in PactoSigna training records per [SOP-007](SOP-007-training-competence.md).

### 5.3 Audit Planning

For each scheduled audit:

1. The Lead Auditor shall prepare an audit plan including:
   - Audit scope (processes, clauses, departments)
   - Audit criteria (standards, procedures, requirements)
   - Audit schedule (dates, times, locations)
   - Audit methods (document review, interviews, observation)
2. The audit plan shall be distributed to the auditee at least **5 business days** before the audit.
3. The Lead Auditor shall review relevant documentation before the audit, including:
   - Applicable SOPs and work instructions
   - Previous audit findings for the area
   - CAPA records related to the area
   - PactoSigna document status and sync history for the area

### 5.4 Audit Execution

1. **Opening meeting**: Confirm scope, schedule, and logistics with the auditee.
2. **Evidence collection**: The Lead Auditor shall gather evidence through:
   - Review of controlled documents and records in PactoSigna
   - Review of PactoSigna's audit trail for relevant actions
   - Interviews with personnel
   - Observation of processes and activities
   - Review of PactoSigna Records Page compiled views as objective evidence
3. **Finding classification**: Classify each observation using the following criteria:

   | Classification | Criteria | Required Action |
   | --- | --- | --- |
   | **Major Finding** | Absence or total breakdown of a required system element | CAPA required; immediate containment |
   | **Minor Finding** | Isolated lapse that does not represent systemic failure | CAPA required; corrective action within 15 business days |
   | **Observation** | Opportunity for improvement; no nonconformance | Documented; tracked as improvement recommendation |

4. **Closing meeting**: Present findings to the auditee; agree on factual accuracy of findings.

### 5.5 Audit Reporting

1. The Lead Auditor shall prepare an audit report (`audit_report` document type) within **10 business days** of audit completion.
2. The audit report shall include:
   - Audit scope and criteria
   - Audit dates and participants
   - Findings classified by severity (major, minor, observation)
   - Evidence supporting each finding
   - Auditor conclusion on the effectiveness of the audited area
3. The audit report shall be managed as a controlled document in PactoSigna per [SOP-001](SOP-001-document-control.md).

### 5.6 Finding Resolution and Follow-Up

1. Major and minor findings shall be escalated to the CAPA process per [SOP-004](SOP-004-capa.md).
2. PactoSigna's Quality Events module links audit findings to CAPA records, maintaining full traceability from finding through corrective action to effectiveness verification.
3. The auditee shall propose corrective actions within **15 business days** of report issuance.
4. The Lead Auditor shall verify corrective action effectiveness.
5. All findings shall be tracked to closure in the finding log.
6. Audit results shall be reported as input to management review per [SOP-006](SOP-006-management-review.md).

### 5.7 Compliance Reporting

PactoSigna's compliance reporting module supports audit activities by providing:

- Compliance packages for audit export with consolidated evidence
- Records Page compiled views (Risk Management File, V&V, DMR, DHR) as audit evidence
- Document status tracking showing procedure currency and review status
- Training compliance data showing department-level completion rates
- Audit trail exports for specific timeframes and action types

## 6. PactoSigna Platform Implementation

| Internal Audit Requirement | PactoSigna Feature |
| --- | --- |
| Audit program documentation | `audit_schedule` document type with structured frontmatter |
| Audit result documentation | `audit_report` document type with findings and evidence |
| Finding to CAPA escalation | Quality Events module links audit findings to CAPA records |
| Audit evidence | Records Page compiled views; audit trail exports; compliance packages |
| Document currency tracking | Document status lifecycle shows current vs. archived procedures |
| Training compliance evidence | Training module completion rates as audit input |
| Corrective action tracking | CAPA state machine tracks finding resolution through effectiveness verification |
| Management review input | Audit results aggregated for management review dashboard |

## 7. Related Documents

- [SOP-001](SOP-001-document-control.md) -- Document Control
- [SOP-004](SOP-004-capa.md) -- Corrective and Preventive Action
- [SOP-006](SOP-006-management-review.md) -- Management Review
- [SOP-007](SOP-007-training-competence.md) -- Training and Competence

## 8. References

| Reference | Description |
| --- | --- |
| ISO 13485:2016 Section 8.2.4 | Internal audit |
| ISO 19011:2018 | Guidelines for auditing management systems |
| 21 CFR Part 820.22 | Quality audit |

## 9. Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 1.0 | 2026-01-15 | PactoSigna Quality | Initial release |
| 2.0 | 2026-04-05 | PactoSigna Quality | Rewritten with PactoSigna platform integration -- audit document types, compliance reporting, CAPA integration, Records Page evidence |
