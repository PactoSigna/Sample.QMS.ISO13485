---
id: SOP-015
title: Change Control
status: approved
author: quality@example.com
reviewers:
  - engineering
approvers:
  - quality-lead
training:
  required_departments:
    - Engineering
    - Quality
  training_mode: quiz
  due_days: 30
---

# SOP-015: Change Control

## 1. Purpose

Control changes to the design and development of medical device software, ensuring that all changes are reviewed, verified, validated as appropriate, and approved before implementation.

## 2. Scope

Applies to all changes to released medical device software, including:

- Bug fixes and defect corrections
- Feature additions and enhancements
- Performance improvements
- Dependency updates (including SOUP components)
- Infrastructure and configuration changes affecting the product

## 3. Definitions

| Term | Definition |
| --- | --- |
| Change Request | Formal request to modify a released product or its documentation |
| Impact Assessment | Analysis of the effect of a proposed change on the product, users, and regulatory status |
| Major Change | Change that affects safety, performance, or intended use; requires full verification and validation |
| Minor Change | Change that does not affect safety or intended use; requires targeted verification |

## 4. Responsibilities

- **Requestor**: Submit change request with rationale and supporting information
- **Engineering Lead**: Conduct impact assessment, plan implementation
- **Quality**: Review impact assessment, verify appropriate V&V, approve change
- **Regulatory**: Assess regulatory impact for major changes (submission amendments, notification requirements)
- **Cross-functional Review Board**: Approve major changes

## 5. Procedure

### 5.1 Change Request Initiation

Change requests originate from:

- CAPA outcomes (per [SOP-004](SOP-004-capa.md))
- Customer feedback and complaints (per [SOP-010](SOP-010-feedback-complaints.md))
- Regulatory changes or new requirements
- Post-market surveillance findings (per [SOP-019](SOP-019-post-market-surveillance.md))
- Internal improvement initiatives
- Security vulnerability discoveries

### 5.2 Change Classification

| Criteria | Major Change | Minor Change |
| --- | --- | --- |
| Safety impact | Yes | No |
| Intended use change | Yes | No |
| Regulatory submission impact | Yes | No |
| New or modified risk controls | Yes | No |
| Core algorithm changes | Yes | No |
| UI/UX only, no safety impact | No | Yes |
| Documentation corrections | No | Yes |
| Non-safety dependency updates | No | Yes |

### 5.3 Impact Assessment

For all changes:

1. Identify affected requirements, design documents, and risk analysis
2. Determine if risk analysis needs updating
3. Identify affected verification and validation activities
4. Assess impact on existing product in the field
5. Determine regulatory submission impact (major changes only)

For major changes, impact assessment is reviewed by the cross-functional review board.

### 5.4 Planning and Approval

1. Engineering plans implementation including:
   - Affected files and components
   - Required V&V activities
   - Regression test scope
   - Documentation updates
2. Quality reviews and approves the plan
3. For major changes: cross-functional review board approves

### 5.5 Implementation

1. Changes implemented on a feature branch
2. Code changes reviewed per [WI-001](../work-instructions/WI-001-github-pr-review.md)
3. All V&V activities executed per the approved plan:
   - Major changes: full verification against affected requirements + targeted validation
   - Minor changes: targeted verification + regression testing

### 5.6 Verification and Validation

| Activity | Major Change | Minor Change |
| --- | --- | --- |
| Unit testing | Required | Required |
| Integration testing | Required | As needed |
| System testing | Required (affected areas) | Regression only |
| Risk analysis update | Required | If applicable |
| Design review | Required | Not required |
| Regulatory assessment | Required | Not required |

### 5.7 Release

1. Change documentation complete (updated requirements, design, test records)
2. All V&V activities passed
3. Risk management file updated if applicable
4. Release per [SOP-014](SOP-014-production-control.md)

## 6. Records

- Change request forms
- Impact assessments
- Cross-functional review board decisions (major changes)
- Verification and validation records
- Updated design documentation

## 7. References

- ISO 13485:2016 Section 7.3.9
- IEC 62304 Section 8 — Software configuration management
- 21 CFR 820.30(i) — Design changes
- [SOP-002](SOP-002-design-development.md) — Design and Development
- [SOP-003](SOP-003-risk-management.md) — Risk Management
- [SOP-013](SOP-013-software-lifecycle.md) — Software Lifecycle
- [SOP-014](SOP-014-production-control.md) — Production Control
