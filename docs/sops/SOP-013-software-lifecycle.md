---
id: SOP-013
title: Software Lifecycle
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

# SOP-013: Software Lifecycle

## 1. Purpose

Define the software development lifecycle processes for medical device software in accordance with IEC 62304. Ensure that software is developed, maintained, and managed with appropriate rigor based on its safety classification.

## 2. Scope

Applies to all medical device software and software components, including:

- Software systems
- Software items and units
- SOUP (Software of Unknown Provenance) components

## 3. Definitions

| Term | Definition |
| --- | --- |
| Software Safety Classification | Classification (A, B, or C) based on the potential of the software to contribute to a hazardous situation |
| Class A | No injury or damage to health possible |
| Class B | Non-serious injury possible |
| Class C | Death or serious injury possible |
| SOUP | Software of Unknown Provenance — pre-existing software not developed under a known software development process |
| Software Item | Any identifiable part of a software system (may be a software unit or an aggregation) |
| Software Unit | Software item that is not subdivided into other items |
| Anomaly | Any condition that deviates from expectations based on requirements, design documents, or standards |

## 4. Responsibilities

- **Engineering Lead**: Maintain the software development plan, ensure IEC 62304 compliance
- **Software Developers**: Implement software per design specifications, perform unit testing, conduct code reviews
- **Quality**: Verify process compliance, review deliverables, maintain traceability
- **Risk Management**: Ensure software risks are identified and mitigated

## 5. Procedure

### 5.1 Software Development Planning

For each software project or major release:

1. Create or update the Software Development Plan specifying:
   - Software safety classification
   - Lifecycle model (iterative, incremental)
   - Deliverables per lifecycle phase
   - Development standards and coding conventions
   - Tools and infrastructure
   - Verification and validation approach
   - Configuration management approach
   - Risk management integration points

### 5.2 Activity Requirements by Safety Class

| Activity | Class A | Class B | Class C |
| --- | --- | --- | --- |
| Software development planning | Required | Required | Required |
| Software requirements analysis | Required | Required | Required |
| Software architectural design | — | Required | Required |
| Software detailed design | — | — | Required |
| Software unit implementation | Required | Required | Required |
| Software unit verification | — | Required | Required |
| Software integration and testing | Required | Required | Required |
| Software system testing | Required | Required | Required |
| Software release | Required | Required | Required |

### 5.3 Software Requirements Analysis

1. Derive software requirements from system requirements and risk control measures
2. Document requirements with unique identifiers
3. Ensure traceability: system requirement → software requirement
4. Requirements reviewed for completeness, correctness, and testability

### 5.4 Software Architectural Design (Class B, C)

1. Define software architecture (components, interfaces, data flows)
2. Identify SOUP components and their requirements
3. Document architecture with sufficient detail for implementation
4. Verify architecture addresses all software requirements

### 5.5 Software Detailed Design (Class C)

1. Define detailed design for each software unit
2. Sufficient detail for implementation without further design decisions
3. Verify detailed design implements architectural design

### 5.6 Software Unit Implementation and Verification

1. Implement per detailed design (Class C) or architectural design (Class B) or requirements (Class A)
2. Follow coding standards and conventions
3. Unit verification (Class B, C):
   - Code review (all changes reviewed by at least one independent reviewer)
   - Unit testing with defined acceptance criteria
   - Static analysis

### 5.7 Software Integration and Integration Testing

1. Integrate software units and items per the integration plan
2. Verify interfaces between integrated items
3. Integration test coverage traces to architectural design
4. Document and resolve anomalies

### 5.8 Software System Testing

1. Execute system test plan against software requirements
2. Test in an environment representative of the intended use environment
3. Document test execution results (pass/fail per test case)
4. All test failures resolved or documented as known anomalies with risk assessment

### 5.9 Software Release

Before release:

1. All planned verification and validation activities completed
2. Known anomalies documented with risk assessment and risk acceptance
3. Release notes prepared (version, changes, known issues)
4. All required signatures obtained (per [SOP-002](SOP-002-design-development.md))
5. Release artifacts archived (source code, build, test results)

### 5.10 SOUP Management

1. Identify all SOUP components (name, version, manufacturer, license)
2. Define functional and performance requirements for each SOUP item
3. Assess risk contribution of SOUP failure
4. Monitor for published anomalies, security vulnerabilities, and updates
5. Evaluate updates for impact and regression risk before adoption

### 5.11 Software Maintenance

1. Collect and analyze feedback and problem reports
2. Classify modifications: corrective, adaptive, perfective
3. Apply appropriate lifecycle activities based on modification scope and safety class
4. Regression testing proportionate to the modification

### 5.12 Software Problem Resolution

1. Problem reports logged with description, severity, and affected version
2. Problems investigated and root cause determined
3. Change requests created for corrections
4. Corrections follow the applicable lifecycle activities
5. Problem resolution verified

## 6. Records

- Software development plan
- Software requirements specification
- Software architecture document
- Software detailed design (Class C)
- Test plans and test reports (unit, integration, system)
- SOUP register
- Release notes
- Problem reports and resolution records
- Configuration management records

## 7. References

- IEC 62304:2006+A1:2015 — Medical device software lifecycle
- ISO 13485:2016 Section 7.3
- ISO 14971:2019 — Risk management
- 21 CFR 820.30 — Design Controls
- [SOP-002](SOP-002-design-development.md) — Design and Development
- [SOP-003](SOP-003-risk-management.md) — Risk Management
- [SOP-015](SOP-015-change-control.md) — Change Control
