---
id: SOP-017
title: Computer System Validation
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

# SOP-017: Computer System Validation

## 1. Purpose

Validate computer software used within the Quality Management System to ensure it performs its intended functions correctly and consistently.

## 2. Scope

Applies to all computer systems used for quality-critical activities, including:

- QMS platform (document management, training, signatures)
- Issue tracking system
- Version control system
- CI/CD pipeline
- Electronic signature systems
- Data backup and recovery systems

Systems used exclusively for non-quality purposes (e.g., office productivity, communication) are excluded unless they generate quality records.

## 3. Definitions

| Term | Definition |
| --- | --- |
| Computer System Validation (CSV) | Establishing documented evidence that a computer system consistently performs its intended functions |
| Intended Use | Documented description of how the system is used within the QMS |
| Risk-Based Approach | Validation effort proportionate to the risk associated with the system's use |
| Revalidation | Repeating validation activities after changes to ensure continued fitness for use |

## 4. Responsibilities

- **Quality**: Identify systems requiring validation, define validation requirements, approve validation reports
- **Engineering/IT**: Execute validation activities, maintain validated state, notify Quality of system changes
- **System Owners**: Define intended use, identify critical functions

## 5. Procedure

### 5.1 System Inventory

1. Quality maintains an inventory of all computer systems used in the QMS
2. Inventory records: system name, version, vendor, intended use, risk classification, validation status, next review date

### 5.2 Risk Classification

| Risk Level | Criteria | Validation Rigor |
| --- | --- | --- |
| High | Direct impact on product quality, safety, or regulatory compliance (e.g., electronic signatures, design controls) | Full validation (IQ, OQ, PQ) |
| Medium | Indirect impact on quality (e.g., training management, supplier tracking) | Functional verification (OQ) |
| Low | Minimal impact (e.g., communication tools, project management) | Documented intended use only |

### 5.3 Validation Planning

For high and medium risk systems:

1. Create a validation plan including:
   - System description and intended use
   - Risk classification and rationale
   - Validation approach and scope
   - Test cases and acceptance criteria
   - Roles and responsibilities
   - Schedule

### 5.4 Validation Execution

#### Installation Qualification (IQ) — High Risk Only

- Verify system is installed per specifications
- Verify system configuration matches requirements
- Document installation environment

#### Operational Qualification (OQ) — High and Medium Risk

- Execute test cases for each critical function
- Verify system performs intended functions correctly
- Test boundary conditions and error handling
- Document pass/fail results with evidence

#### Performance Qualification (PQ) — High Risk Only

- Verify system performs consistently under normal operating conditions
- Execute representative workflow scenarios
- Verify data integrity and accuracy

### 5.5 Validation Report

1. Summarize validation activities and results
2. Document any deviations and their resolution
3. State validation conclusion (system is / is not validated for intended use)
4. Quality Manager approves validation report

### 5.6 Maintaining Validated State

1. System changes assessed for validation impact
2. Revalidation triggers:
   - Major version upgrades
   - Configuration changes affecting validated functions
   - Infrastructure changes (OS upgrades, server migrations)
   - Vendor-reported issues affecting validated functions
3. Minor updates (patches, security fixes) assessed; revalidation performed if validated functions affected

### 5.7 Periodic Review

1. Validated systems reviewed annually
2. Review confirms: system still in use, intended use unchanged, no unreported changes, no outstanding issues
3. Review documented; any issues trigger revalidation or remediation

## 6. Records

- Computer system inventory
- Validation plans
- Test protocols and results (IQ, OQ, PQ)
- Validation reports
- Change impact assessments
- Periodic review records

## 7. References

- ISO 13485:2016 Section 4.1.6
- 21 CFR Part 11 — Electronic Records; Electronic Signatures
- GAMP 5 — A Risk-Based Approach to Compliant GxP Computerized Systems
- [SOP-005](SOP-005-control-of-records.md) — Control of Records
