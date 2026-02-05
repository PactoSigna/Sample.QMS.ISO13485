---
id: WI-002
title: Document Approval
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
  training_mode: acknowledge
  due_days: 14
---

# WI-002: Document Approval

## Purpose

Step-by-step instructions for approving controlled documents in PactoSigna.

## Prerequisites

- Document has completed review per [WI-001](WI-001-github-pr-review.md)
- User has approver role for document type

## Procedure

### 1. Navigate to Document

1. Log into PactoSigna
2. Navigate to Documents section
3. Find document pending approval

### 2. Review Document

1. Read document content carefully
2. Verify all review comments addressed
3. Confirm document meets requirements

### 3. Approve Document

1. Click "Approve" button
2. Select signature meaning:
   - "I have reviewed and approve this document"
   - "I am the author and certify accuracy"
3. Authenticate with password
4. Confirm signature

### 4. Verify Status

1. Document status changes to "Approved"
2. Audit log entry created
3. Approvers listed in signature block

## Related Documents

- [SOP-001](../sops/SOP-001-document-control.md) - Document Control
- [WI-001](WI-001-github-pr-review.md) - GitHub PR Review
- [WI-003](WI-003-release-signing.md) - Release Signing
