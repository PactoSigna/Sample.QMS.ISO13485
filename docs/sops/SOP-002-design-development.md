---
id: SOP-002
title: Design and Development
status: approved
author: quality
reviewers:
  - engineering
  - quality
  - regulatory
approvers:
  - quality
training:
  required_departments:
    - Engineering
    - Quality
  training_mode: quiz
  due_days: 30
---

# SOP-002: Design and Development

> **Document Type**: Standard Operating Procedure
> **Regulatory Basis**: ISO 13485:2016 Section 7.3, IEC 62304:2006+A1:2015
> **Status**: Effective
> **Last Updated**: 2026-04-05
> **Owner**: PactoSigna Quality
> **Review Cycle**: Annual

## 1. Purpose

This procedure establishes the requirements for planning and executing the design and development of medical device software in compliance with ISO 13485:2016 Section 7.3 and IEC 62304. It defines how PactoSigna's traceability engine, release workflow, and gap detection capabilities support a controlled design process from user needs through verification and validation.

## 2. Scope

This SOP applies to all software design and development activities for regulated medical devices, including:

- Identification and capture of user needs
- Derivation of product and software requirements
- Creation of architecture and detailed design documents
- Design verification and validation activities
- Design transfer (release) activities
- Design changes managed through the release workflow

This SOP does not cover manufacturing process design or hardware design activities.

## 3. Definitions

| Term | Definition |
| --- | --- |
| **User Need (UN)** | A statement of what a stakeholder requires from the product, documented as UN-{CODE}-XXX |
| **Product Requirement (PRS)** | A testable specification derived from user needs, documented as PRS-{CODE}-XXX with `docType: requirement` and `metadata.category: product` |
| **Software Requirement (SRS)** | An implementation specification derived from product requirements, documented as SRS-{CODE}-XXX with `docType: requirement` and `metadata.category: software` |
| **Design Input** | The complete set of requirements (UN, PRS, SRS) that define what the design must achieve |
| **Design Output** | Architecture (HLD), detailed design (SDD), source code, and test cases that implement the design inputs |
| **Traceability Chain** | The bidirectional linking from UN -> PRS -> SRS -> HLD/SDD -> Tests, implemented via `traces_to` and `traces_from` frontmatter fields |
| **Gap Detection** | PactoSigna's automated engine that identifies broken or missing trace links across the traceability chain |
| **Design Change Order (DCO)** | A controlled change record within PactoSigna's Release workflow that documents the rationale and scope of design changes |
| **Safety Classification** | IEC 62304 classification (Class A, B, or C) assigned to the software system, determining the rigor of development activities |

## 4. Roles and Responsibilities

| Role | Responsibilities |
| --- | --- |
| **Product Owner** | Captures user needs; defines product requirements; prioritizes design inputs |
| **Engineering** | Derives software requirements; creates architecture and design documents; implements and tests software; maintains traceability links |
| **Quality** | Verifies traceability completeness via PactoSigna gap detection; ensures design review records are complete; monitors design control compliance |
| **Regulatory** | Reviews regulatory mapping in requirements frontmatter; ensures applicable standards are addressed; reviews risk management integration |
| **Release Manager** | Manages the PactoSigna Release workflow; creates Design Change Orders; coordinates sign-off activities |

## 5. Procedure

### 5.1 Design Planning

1. For each development project, a Software Development Plan (SDP) shall be created as a controlled document (SDP-XXX).
2. The plan shall define:
   - Software safety classification per IEC 62304 (Class A, B, or C)
   - Development phases and milestones
   - Required design reviews
   - Verification and validation strategy
   - Risk management activities
   - Configuration management approach
3. The safety classification shall be recorded in PactoSigna's Release configuration, as it determines the rigor of required activities.

### 5.2 Design Input -- Requirements Capture

1. **User Needs** shall be documented as markdown files (UN-{CODE}-XXX) in `docs/product/user-needs/` with frontmatter including:
   - `traces_to`: Links to derived product requirements (PRS documents)
   - `priority`: Classification of need importance
   - `stakeholder`: The stakeholder group the need serves

2. **Product Requirements** shall be documented as PRS-{CODE}-XXX in `docs/product/requirements/` with frontmatter including:
   - `traces_from`: Links back to the originating user need(s)
   - `traces_to`: Links to derived software requirements (SRS documents)
   - `verification_method`: How the requirement will be verified

3. **Software Requirements** shall be documented as SRS-{CODE}-XXX in `docs/software/requirements/` with frontmatter including:
   - `traces_from`: Links back to the originating product requirement(s)
   - `traces_to`: Links to architecture/design documents and test cases

4. PactoSigna's Document Sync engine validates all frontmatter fields against Zod schemas at sync time. Invalid trace links or missing required fields generate validation errors.

### 5.3 Design Output -- Architecture and Design

1. **High-Level Design (HLD)** documents shall describe the system architecture, component interfaces, and data flows.
2. **Software Design Documents (SDD)** shall describe detailed component design, algorithms, and data structures.
3. Design outputs shall include `traces_from` references to the software requirements they implement.
4. PactoSigna's gap detection engine verifies that every SRS traces forward to at least one design output and test case.

### 5.4 Design Verification

1. Design verification shall confirm that design outputs meet design input requirements.
2. Verification methods include:
   - Unit tests linked to software requirements
   - Integration tests covering component interfaces
   - System tests validating end-to-end functionality
3. Test cases shall include `traces_from` or `verifies` links to the requirements they verify.
4. A Software Test Plan (STP-XXX) shall define the verification strategy, test levels, and acceptance criteria.
5. PactoSigna's traceability engine reports coverage gaps where requirements lack corresponding test cases.

### 5.5 Design Validation

1. Design validation shall confirm the product meets user needs and intended use.
2. Validation activities include:
   - Usability testing against task analyses
   - Clinical evaluation (where applicable)
   - User acceptance testing
3. Validation test cases shall include `validates` links to user needs (UN documents).

### 5.6 Design Review

1. Design reviews shall be conducted at planned milestones defined in the SDP.
2. PactoSigna's Release workflow provides a Design Review Record virtual view that consolidates:
   - Traceability status (gap detection results)
   - Requirement coverage metrics
   - Risk management status
   - Open issues and action items
3. Review participants shall apply electronic signatures in PactoSigna to record their review and approval.

### 5.7 Design Transfer (Release)

1. Before design transfer, the following shall be complete:
   - All verification activities passed
   - All validation activities completed
   - Risk management file reviewed and accepted
   - All required electronic signatures obtained
   - Gap detection shows no critical missing trace links
2. The Release Manager shall create a PactoSigna Release that freezes all documents as point-in-time snapshots.
3. The Release shall include IEC 62304 safety classification, and the platform enforces sign-off requirements scaled to the classification level.
4. Upon publication, the Release creates an immutable record in the audit trail.

### 5.8 Design Changes

1. All changes to approved design documents shall be managed through PactoSigna's Release workflow with a Design Change Order (DCO).
2. The DCO shall document:
   - Description of the change
   - Rationale for the change
   - Impact assessment (affected requirements, design documents, test cases, risks)
   - Verification and validation plan for the change
3. PactoSigna's gap detection engine identifies when a change breaks existing trace links, ensuring traceability integrity is maintained.

### 5.9 Risk Management Integration

1. Risk management activities shall be conducted in parallel with design activities per [SOP-003](SOP-003-risk-management.md).
2. PactoSigna supports ISO 14971 risk management with:
   - Risk matrix configuration per device
   - Hazard analysis documents linked to requirements
   - STRIDE security risk analysis for cybersecurity
   - Safety chain linking risks to mitigations and verification
3. Risk management findings may generate new requirements, which must follow the traceability chain established in this procedure.

## 6. PactoSigna Platform Implementation

| Design Control Requirement | PactoSigna Feature |
| --- | --- |
| Traceability | `traces_to` and `traces_from` frontmatter fields with gap detection engine |
| Design input capture | Structured markdown documents with Zod-validated frontmatter for UN, PRS, SRS |
| Design output documentation | HLD/SDD documents with bidirectional requirement links |
| Design review records | Release workflow with electronic signature gates and Design Review Record view |
| Design verification | Test case documents linked to requirements; coverage gap reporting |
| Design transfer | Release workflow with point-in-time snapshots and safety classification enforcement |
| Design changes | Design Change Order (DCO) with impact analysis and re-verification tracking |
| Risk integration | Risk matrix, hazard analysis, STRIDE analysis linked to requirements and mitigations |
| Safety classification | IEC 62304 Class A/B/C on releases, scaling sign-off requirements accordingly |

## 7. Related Documents

- [SOP-003](SOP-003-risk-management.md) -- Risk Management
- [SOP-001](SOP-001-document-control.md) -- Document Control
- [WI-001](../work-instructions/WI-001-github-pr-review.md) -- GitHub PR Review
- [WI-003](../work-instructions/WI-003-release-signing.md) -- Release Signing

## 8. References

| Reference | Description |
| --- | --- |
| ISO 13485:2016 Section 7.3 | Design and development |
| IEC 62304:2006+A1:2015 | Medical device software -- Software lifecycle processes |
| ISO 14971:2019 | Application of risk management to medical devices |
| 21 CFR Part 820.30 | Design controls |

## 9. Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 1.0 | 2026-01-15 | PactoSigna Quality | Initial release |
| 2.0 | 2026-04-05 | PactoSigna Quality | Rewritten with PactoSigna platform integration -- traceability engine, gap detection, release workflow, DCO, safety classification |
