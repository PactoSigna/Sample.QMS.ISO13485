---
id: AUD-RPT-002
title: "Internal Audit Report: ISO 13485 QMS Audit"
status: approved
author: quality.lead@example.com
reviewers: [quality.manager@example.com]
approvers: [quality.director@example.com]
audit_date: "2026-01-20"
audit_id: IA-2026-000
process_area: Document Control and Design Development
clause: "§4.2, §7.3"
auditor: quality.lead@example.com
findings:
  - finding_id: F-001
    classification: observation
    description: "Controlled document distribution list not updated for latest SOP revision"
source: audit-report.pdf
---

# Internal Audit Report: ISO 13485 QMS Audit

## Scope

This audit covered Document Control (ISO 13485:2016 §4.2) and Design and Development (§7.3) processes, examining procedural compliance and record keeping across all active projects.

## Methodology

The audit was conducted on 2026-01-20 using the following approach:

1. **Document review**: Examination of controlled document registers, distribution lists, and revision histories
2. **Record sampling**: Review of 10 design development records and 5 document control records
3. **Personnel interviews**: Interviews with 2 quality team members and 1 engineering lead
4. **Process observation**: Observation of document review workflow in the QMS platform

### Reference Documents

- [SOP-001](../../sops/SOP-001-document-control.md) - Document Control Procedure
- [SOP-002](../../sops/SOP-002-design-development.md) - Design & Development Procedure
- [WI-003](../../work-instructions/WI-003-release-signing.md) - Release Signing Work Instruction

## Findings

### F-001: Document Distribution List Not Updated (Observation)

**Classification**: Observation
**Clause**: ISO 13485 §4.2.4

The controlled document distribution list was not updated to reflect the latest revision of SOP-001. The previous revision's distribution list was still in use. This did not result in any personnel using outdated documents, as the QMS platform automatically serves the current version.

**Recommendation**: Automate distribution list updates when controlled documents are revised in the QMS platform.

## Conclusion

The Document Control and Design Development processes are well-established and generally compliant with ISO 13485:2016 requirements. One observation was identified regarding document distribution list maintenance. No nonconformances were found.

Overall audit assessment: Both processes meet ISO 13485 requirements. The observation is a low-priority improvement opportunity.
