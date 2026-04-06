---
id: SOP-001
title: Document Control
status: approved
author: quality
reviewers:
  - engineering
  - quality
approvers:
  - quality
training:
  required_departments:
    - Quality
    - Engineering
    - Regulatory
  training_mode: quiz
  due_days: 30
---

# SOP-001: Document Control

> **Document Type**: Standard Operating Procedure
> **Regulatory Basis**: ISO 13485:2016 Section 4.2.4
> **Status**: Effective
> **Last Updated**: 2026-04-05
> **Owner**: PactoSigna Quality
> **Review Cycle**: Annual

## 1. Purpose

This procedure establishes the requirements for creating, reviewing, approving, distributing, and managing controlled documents within the Quality Management System. It defines how PactoSigna's git-native document management platform automates document control to ensure compliance with ISO 13485:2016 Section 4.2.4 and 21 CFR Part 820.40.

## 2. Scope

This SOP applies to all QMS-controlled documents, including:

- Quality policies (POL-XXX)
- Standard operating procedures (SOP-XXX)
- Work instructions (WI-XXX)
- User needs (UN-XXX)
- Product requirements (PRS-XXX)
- Software requirements (SRS-XXX)
- Architecture documents (HLD-XXX, SDD-XXX)
- Risk management documents (RISK-XXX, RMP-XXX)
- Test cases and plans (TC-XXX, STP-XXX, SDP-XXX)
- Audit schedules and reports
- Supplier documentation
- Job descriptions and training materials

This SOP does not apply to uncontrolled reference materials, informal meeting notes, or external standards (which are managed by their issuing bodies).

## 3. Definitions

| Term | Definition |
| --- | --- |
| **Controlled Document** | Any document within the QMS that is subject to formal review, approval, and change control |
| **Frontmatter** | YAML metadata block at the top of each markdown document, validated by PactoSigna's Zod schemas at sync time |
| **Document Sync** | The process by which PactoSigna's sync engine imports markdown files from GitHub into the platform's Firestore database |
| **Electronic Signature** | A Part 11-compliant digital signature applied through PactoSigna, binding a signer's identity to a specific document version |
| **Release** | A point-in-time snapshot of documents frozen for sign-off through PactoSigna's Release workflow |
| **Status Lifecycle** | The controlled progression of a document through defined states: `draft` -> `in_review` -> `approved` -> `effective` -> `archived` |

## 4. Roles and Responsibilities

| Role | Responsibilities |
| --- | --- |
| **Document Author** | Creates and maintains document content as markdown files in the git repository; ensures frontmatter conforms to schema requirements |
| **Reviewer** | Verifies technical accuracy, completeness, and compliance via GitHub Pull Request review and PactoSigna platform review |
| **Approver** | Authorizes the document for use by applying a Part 11-compliant electronic signature through PactoSigna |
| **Quality** | Maintains the document control system; monitors sync events for schema validation errors; manages folder rules and naming conventions |
| **Repository Admin** | Configures repository settings in PactoSigna; manages GitHub integration and sync triggers |

## 5. Procedure

### 5.1 Document Creation

1. The author shall create a new markdown file in the appropriate folder within the git repository.
2. The document shall include a YAML frontmatter block with the following required fields:
   - `id`: Unique document identifier following the naming convention (e.g., `SOP-001`)
   - `title`: Descriptive document title
   - `status`: Initial status set to `draft`
   - `author`: Email address of the document author
3. PactoSigna's folder rules enforce document ID prefixes and placement. Documents placed in incorrect folders will generate validation warnings at sync time.
4. The author shall include all required sections as defined by the document type's `REQUIRED_SECTIONS` configuration.

### 5.2 Document Identification and Naming

| Document Type | ID Format | Repository Folder |
| --- | --- | --- |
| Policy | POL-XXX | `docs/policies/` |
| SOP | SOP-XXX | `docs/sops/` |
| Work Instruction | WI-XXX | `docs/work-instructions/` |
| User Need | UN-{CODE}-XXX | `docs/product/user-needs/` |
| Product Requirement | PRS-{CODE}-XXX | `docs/product/requirements/` |
| Software Requirement | SRS-{CODE}-XXX | `docs/software/requirements/` |
| Architecture | HLD-XXX / SDD-XXX | `docs/software/architecture/` or `docs/software/design/` |

### 5.3 Review Process

1. The author shall submit changes via a GitHub Pull Request targeting the main branch.
2. Reviewers listed in the document's frontmatter `reviewers` field shall be assigned to the PR.
3. Reviewers shall evaluate the document for:
   - Technical accuracy and completeness
   - Compliance with applicable standards and regulations
   - Correct frontmatter schema conformance
   - Proper cross-references and traceability links
4. The author shall address all reviewer feedback before proceeding to approval.
5. When the PR is merged, PactoSigna's Document Sync engine automatically imports the updated document and validates the frontmatter against the appropriate Zod schema.

### 5.4 Approval Process

1. Once all reviewers have approved the PR, the document shall be included in a PactoSigna Release.
2. Approvers listed in the document's frontmatter `approvers` field shall apply Part 11-compliant electronic signatures through PactoSigna.
3. Each electronic signature captures:
   - Signer identity (name and email from authenticated session)
   - Signature meaning (e.g., "I have reviewed and approve this document")
   - Timestamp (server-generated)
   - Document version bound to the git commit SHA
4. The document status shall be updated to `approved` upon receipt of all required signatures.
5. PactoSigna's immutable audit trail records all signature events with over 80 distinct action types.

### 5.5 Document Status Lifecycle

| Status | Description | Transition Trigger |
| --- | --- | --- |
| `draft` | Initial state; document is being authored | Document created in repository |
| `in_review` | Document is undergoing formal review | Author submits for review |
| `approved` | All required signatures obtained | All approvers sign via PactoSigna |
| `effective` | Document is in active use | Release published |
| `archived` | Document superseded or withdrawn | New version approved or document retired |

### 5.6 Document Changes

1. All changes to controlled documents shall follow the same review and approval process as new documents.
2. Changes shall be made on a feature branch in the git repository, not directly on the main branch.
3. The PactoSigna Release workflow uses a Design Change Order (DCO) to control and track changes to approved documents.
4. The sync engine validates that changed frontmatter still conforms to the document type's Zod schema.
5. Training re-assignment is triggered automatically when documents with `training` frontmatter blocks are updated and a new release is published.

### 5.7 Document Distribution

1. PactoSigna serves as the single source of truth for all controlled documents once synced from the git repository.
2. The platform provides read access to all organization members based on their role and department.
3. The Release workflow freezes documents as point-in-time snapshots, ensuring that signed versions are immutable.

### 5.8 Obsolete Document Control

1. When a document is superseded or withdrawn, the author shall update its frontmatter status to `archived`.
2. PactoSigna preserves all historical versions through git commit history and release snapshots.
3. Archived documents remain accessible for audit purposes but are clearly marked as no longer in effect.

## 6. PactoSigna Platform Implementation

| Document Control Requirement | PactoSigna Feature |
| --- | --- |
| Document identification | Frontmatter `id` field validated by Zod schemas; folder rules enforce naming conventions |
| Version control | Git repository provides full version history with commit SHA binding |
| Review workflow | GitHub Pull Request integration with assigned reviewers |
| Approval signatures | Part 11-compliant electronic signatures with meaning, identity, and timestamp |
| Change control | Release workflow with Design Change Order (DCO) tracking |
| Distribution | Platform serves synced documents to authorized organization members |
| Obsolescence | Status lifecycle management; archived documents preserved in release snapshots |
| Audit trail | Immutable audit log captures all document mutations (80+ action types) |
| Schema validation | Document Sync engine validates frontmatter against Zod schemas at sync time |
| Training integration | Automatic training assignment when documents with `training` blocks are updated |

## 7. Related Documents

- [POL-001](../policies/POL-001-quality-policy.md) -- Quality Policy
- [WI-001](../work-instructions/WI-001-github-pr-review.md) -- GitHub PR Review
- [WI-002](../work-instructions/WI-002-document-approval.md) -- Document Approval
- [SOP-007](SOP-007-training-competence.md) -- Training and Competence

## 8. References

| Reference | Description |
| --- | --- |
| ISO 13485:2016 Section 4.2.4 | Control of documents |
| ISO 13485:2016 Section 4.2.5 | Control of records |
| 21 CFR Part 820.40 | Document controls |
| 21 CFR Part 11 | Electronic records; electronic signatures |

## 9. Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 1.0 | 2026-01-15 | PactoSigna Quality | Initial release |
| 2.0 | 2026-04-05 | PactoSigna Quality | Rewritten with PactoSigna platform integration -- sync engine, electronic signatures, release workflow, folder rules, schema validation |
