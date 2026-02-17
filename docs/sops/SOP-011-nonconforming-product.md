---
id: SOP-011
title: Nonconforming Product
status: approved
author: quality@example.com
reviewers:
  - engineering
approvers:
  - quality-lead
training:
  required_departments:
    - Quality
    - Engineering
  training_mode: quiz
  due_days: 30
---

# SOP-011: Nonconforming Product

## 1. Purpose

Identify, document, evaluate, segregate, and disposition nonconforming product to prevent unintended use or delivery.

## 2. Scope

Applies to all medical device software products found to not conform to specified requirements at any stage of the lifecycle, including:

- Software defects found during development, testing, or post-release
- Failed test results
- Out-of-specification releases
- Post-market reported issues
- Audit findings indicating product nonconformity

## 3. Definitions

| Term | Definition |
| --- | --- |
| Nonconforming Product | Product that does not fulfill specified requirements |
| Disposition | Decision on the action to be taken for nonconforming product |
| Concession | Permission to use or release nonconforming product as-is |
| Rework | Action taken to make a nonconforming product conform to requirements |

## 4. Responsibilities

- **Quality**: Maintain nonconformance records, coordinate disposition decisions, track closure
- **Engineering**: Provide technical assessment, implement rework or corrections
- **Regulatory**: Assess regulatory impact of nonconformances, advise on reporting needs
- **Product Owner**: Approve concessions (use-as-is decisions)

## 5. Procedure

### 5.1 Identification

Nonconforming product may be identified through:

- Testing (unit, integration, system, regression)
- Code review findings
- Customer complaints (per [SOP-010](SOP-010-feedback-complaints.md))
- Internal audits (per [SOP-008](SOP-008-internal-audit.md))
- Post-market surveillance (per [SOP-019](SOP-019-post-market-surveillance.md))
- Automated monitoring and alerting

### 5.2 Documentation

A nonconformance report (NCR) is created including:

- Unique NCR identifier
- Date of detection
- Product/version affected
- Description of the nonconformity
- Severity classification
- Detected by (person/process)
- Impact assessment

### 5.3 Severity Classification

| Severity | Definition | Response Time |
| --- | --- | --- |
| Critical | Patient safety risk, data loss risk, or regulatory non-compliance affecting safety | Immediate containment, disposition within 24 hours |
| Major | Significant functional impact, regulatory non-compliance not affecting safety | Disposition within 5 business days |
| Minor | Cosmetic, low functional impact, no safety or regulatory concern | Disposition within 15 business days |

### 5.4 Containment

For critical and major nonconformances in released product:

1. Assess whether released versions are affected
2. If affected: determine interim containment (disable feature, communicate workaround, halt distribution)
3. Notify affected customers if necessary
4. Assess regulatory reporting requirements (per [SOP-012](SOP-012-regulatory-reporting.md))

### 5.5 Disposition

Disposition options:

| Disposition | Description | Approval Required |
| --- | --- | --- |
| Rework (Patch) | Fix the defect and re-verify | Engineering lead + Quality |
| Use-As-Is (Concession) | Accept the nonconformity with documented justification and risk assessment | Product Owner + Quality + Regulatory (for safety-related) |
| Reject (Recall/Rollback) | Remove or replace the nonconforming product | Quality + Regulatory |

### 5.6 Rework

1. Rework follows the same design control process as original development
2. Reworked product undergoes verification appropriate to the change
3. Rework is documented with the same review and approval as the original
4. Re-testing confirms the nonconformity is resolved and no regression introduced

### 5.7 Closure

1. Disposition is executed and verified
2. Quality determines if CAPA is warranted (per [SOP-004](SOP-004-capa.md))
3. NCR is closed by Quality
4. Nonconformance data feeds into data analysis (per [SOP-016](SOP-016-data-analysis.md))

## 6. Records

- Nonconformance reports (NCRs)
- Disposition records and justifications
- Concession authorizations
- Rework verification records
- Containment action records

## 7. References

- ISO 13485:2016 Section 8.3
- 21 CFR 820.90
- [SOP-004](SOP-004-capa.md) — CAPA
- [SOP-010](SOP-010-feedback-complaints.md) — Customer Feedback and Complaint Handling
- [SOP-012](SOP-012-regulatory-reporting.md) — Regulatory Reporting
