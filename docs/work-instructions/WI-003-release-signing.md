---
id: WI-003
title: Release Signing
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
  training_mode: instructor_led
  due_days: 14
---

# WI-003: Release Signing

## Purpose

Step-by-step instructions for electronically signing software releases per 21 CFR Part 11.

## Prerequisites

- All release documents approved
- All verification activities complete
- Risk management file complete
- User has release authority

## Procedure

### 1. Create Release

1. Navigate to Releases section in PactoSigna
2. Click "Create Release"
3. Enter release version and description
4. Select documents to include

### 2. Verify Completeness

System validates:

- All required document types present
- All documents in approved status
- Traceability complete (no gaps)
- Risk controls verified

### 3. Sign Release

1. Review release summary
2. Select signature meaning:
   - "I authorize this release for production"
3. Authenticate with password
4. Confirm electronic signature

### 4. Post-Release

1. Release status changes to "Released"
2. Audit log captures all signatures
3. Release becomes immutable
4. Notification sent to stakeholders

## Signature Requirements

Per 21 CFR Part 11:

- Signature includes printed name, date/time, meaning
- Signatures are linked to their respective documents
- Signed records cannot be modified

## Related Documents

- [SOP-002](../sops/SOP-002-design-development.md) - Design and Development
- [WI-002](WI-002-document-approval.md) - Document Approval
