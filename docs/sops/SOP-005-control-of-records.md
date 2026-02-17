---
id: SOP-005
title: Control of Records
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

# SOP-005: Control of Records

## 1. Purpose

Define the process for identifying, storing, protecting, retrieving, retaining, and disposing of quality records to ensure they remain legible, readily identifiable, and retrievable.

## 2. Scope

Applies to all quality records including but not limited to:

- Design and development records
- Training and competency records
- Audit reports and findings
- CAPA records
- Management review minutes
- Complaint and feedback records
- Supplier evaluation records
- Nonconformance reports
- Release and deployment records

## 3. Definitions

| Term | Definition |
| --- | --- |
| Quality Record | Evidence of activities performed or results achieved that demonstrates conformity to requirements |
| Retention Period | Minimum duration a record must be maintained before disposition |
| Disposition | Controlled destruction or archival of records after the retention period |

## 4. Responsibilities

- **Quality**: Maintains the record retention schedule, conducts periodic reviews, oversees disposition
- **All Departments**: Generate records per applicable SOPs, ensure records are complete and accurate
- **IT/Engineering**: Maintain record storage systems, backup procedures, and access controls

## 5. Procedure

### 5.1 Record Identification

All quality records must include:

- Unique identifier or reference to the source document/process
- Date of creation
- Author or responsible person
- Status (if applicable)

### 5.2 Record Storage

Records are stored in the following systems:

| Record Type | Storage Location | Format |
| --- | --- | --- |
| Controlled documents | Git repository (main branch) | Markdown |
| Electronic signatures | QMS platform database | Electronic |
| Training records | QMS platform database | Electronic |
| Audit reports | Git repository | Markdown / PDF |
| CAPA records | Issue tracking system | Electronic |

### 5.3 Record Protection

- **Access control**: Records accessible only to authorized personnel via role-based access
- **Backup**: Automated daily backups with off-site replication
- **Integrity**: Git version control provides tamper-evident history; electronic records are immutable once created
- **Confidentiality**: Sensitive records encrypted at rest and in transit

### 5.4 Record Retrieval

Records are retrievable by:

- Document ID or record identifier
- Date range
- Author or responsible person
- Full-text search within the QMS platform

### 5.5 Retention Periods

| Record Category | Minimum Retention Period | Regulatory Basis |
| --- | --- | --- |
| Design and development records | Lifetime of device + 15 years | EU MDR Art. 10(8) |
| Risk management records | Lifetime of device + 15 years | ISO 14971 |
| Training records | Duration of employment + 5 years | ISO 13485 §6.2 |
| CAPA records | 15 years from closure | 21 CFR 820.184 |
| Complaint records | Lifetime of device + 15 years | EU MDR, 21 CFR 820.198 |
| Audit records | 10 years | ISO 13485 §4.2.5 |
| Management review records | 10 years | ISO 13485 §5.6 |
| Supplier records | Duration of relationship + 5 years | ISO 13485 §7.4 |

### 5.6 Disposition

1. Quality reviews records approaching end of retention period quarterly
2. Records eligible for disposition are listed in a disposition log
3. Quality Manager approves disposition
4. Electronic records are permanently deleted from all systems including backups
5. Disposition is recorded in the disposition log

## 6. Records

- Record retention schedule
- Disposition log
- Periodic review records

## 7. References

- ISO 13485:2016 Section 4.2.5
- 21 CFR 820.184
- EU MDR 2017/745 Article 10(8)
- [SOP-001](SOP-001-document-control.md) — Document Control
