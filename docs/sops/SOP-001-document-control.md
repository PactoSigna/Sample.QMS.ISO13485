---
id: SOP-001
title: Document Control
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
    - Regulatory
  training_mode: quiz
  due_days: 30
---

# SOP-001: Document Control

## Purpose

Define the process for creating, reviewing, approving, and managing controlled documents within the Quality Management System.

## Scope

Applies to all QMS documents including policies, SOPs, work instructions, and device documentation.

## Responsibilities

- **Document Author**: Creates and maintains document content
- **Reviewers**: Verify technical accuracy and completeness
- **Approvers**: Authorize document for use
- **Quality**: Maintains document control system

## Procedure

### 1. Document Creation

1. Author creates document using appropriate template
2. Document ID assigned per naming convention:
   - Policies: POL-XXX
   - SOPs: SOP-XXX
   - Work Instructions: WI-XXX
3. Initial status set to `draft`

### 2. Review Process

1. Author submits document via GitHub Pull Request
2. Reviewers listed in frontmatter are assigned
3. Reviewers provide feedback via PR comments
4. Author addresses all feedback

### 3. Approval Process

1. All reviewers approve PR
2. Approvers listed in frontmatter sign off
3. Status changed to `approved`
4. PR merged to main branch

### 4. Document Changes

1. Create new branch for changes
2. Update document content
3. Increment version if applicable
4. Follow review/approval process

## Related Documents

- [POL-001](../policies/POL-001-quality-policy.md) - Quality Policy
- [WI-001](../work-instructions/WI-001-github-pr-review.md) - GitHub PR Review
- [WI-002](../work-instructions/WI-002-document-approval.md) - Document Approval

## References

- ISO 13485:2016 Section 4.2.4
- 21 CFR Part 820.40
