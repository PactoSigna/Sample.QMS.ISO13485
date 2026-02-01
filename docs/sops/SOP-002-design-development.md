---
id: SOP-002
title: Design and Development
status: approved
author: engineering@example.com
reviewers:
  - quality
approvers:
  - engineering-lead
---

# SOP-002: Design and Development

## Purpose

Define the design and development process for medical device software per IEC 62304 and ISO 13485.

## Scope

Applies to all software development activities for regulated medical devices.

## Responsibilities

- **Product Owner**: Defines user needs and product requirements
- **Engineering**: Implements software requirements and architecture
- **Quality**: Ensures process compliance and traceability

## Procedure

### 1. Design Input

1. Capture user needs (UN-XXX documents)
2. Derive product requirements (PRS-XXX documents)
3. Derive software requirements (SRS-XXX documents)
4. Establish traceability using markdown links

### 2. Design Process

1. Create architecture documents (HLD-XXX)
2. Create detailed design documents (SDD-XXX)
3. Implement per design specifications
4. Maintain traceability to requirements

### 3. Design Verification

1. Create test cases (TC-XXX) that verify requirements
2. Execute tests and document results
3. Link test cases to requirements with `**Verifies:**` links

### 4. Design Validation

1. Validate against user needs
2. Link test cases to user needs with `**Validates:**` links
3. Document validation evidence

### 5. Design Transfer

1. Complete all verification activities
2. Complete risk management activities
3. Approve release per [WI-003](../work-instructions/WI-003-release-signing.md)

## Related Documents

- [SOP-003](SOP-003-risk-management.md) - Risk Management
- [WI-001](../work-instructions/WI-001-github-pr-review.md) - GitHub PR Review

## References

- IEC 62304:2006+A1:2015
- ISO 13485:2016 Section 7.3
