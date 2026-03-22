---
id: AUD-RPT-001
title: "Internal Audit: Design Control Q1 2026"
status: approved
author: jane.smith@example.com
reviewers: [quality.lead@example.com]
approvers: [quality.director@example.com]
audit_date: "2026-03-15"
audit_id: IA-2026-001
process_area: Design Control
clause: "§7.3"
auditor: jane.smith@example.com
findings:
  - finding_id: F-001
    classification: minor_nc
    description: "Training records for SOP-012 rev. 3 not updated for two design engineers"
    capa_id: CAPA-2026-005
  - finding_id: F-002
    classification: observation
    description: "Risk file naming convention inconsistent across projects but within tolerance"
  - finding_id: F-003
    classification: major_nc
    description: "Design review meeting minutes for Project Alpha not recorded per SOP-007 §4.2"
    capa_id: CAPA-2026-006
---

# Internal Audit: Design Control Q1 2026

## Scope

This audit covered the Design Control process (ISO 13485:2016 §7.3) including:

- Design and development planning (§7.3.2)
- Design inputs and outputs (§7.3.3, §7.3.4)
- Design reviews (§7.3.5)
- Design verification and validation (§7.3.6, §7.3.7)
- Design transfer (§7.3.8)
- Design changes (§7.3.9)
- Design and development files (§7.3.10)

The audit scope included all active device projects (Project Alpha, Project Beta) and their associated design history files.

## Methodology

The audit was conducted on 2026-03-15 using the following approach:

1. **Document review**: Examination of design history files, SOPs, and work instructions related to design control
2. **Record sampling**: Random selection of 15 design records across both active projects
3. **Personnel interviews**: Interviews with 4 design engineers and 2 project leads
4. **Process observation**: Observation of one design review meeting (Project Beta sprint review)

### Reference Documents

- SOP-007: Design Control Procedure (rev. 4)
- SOP-012: Training and Competence (rev. 3)
- WI-003: Design Review Meeting Protocol (rev. 2)

## Findings

### F-001: Training Records Not Updated (Minor NC)

**Classification**: Minor Nonconformance
**Clause**: ISO 13485 §6.2, SOP-012 §4.3

Two design engineers (DE-003, DE-007) completed training on SOP-012 revision 3 but their training records were not updated in the training management system. The training was completed on 2026-02-20, but records still reference revision 2.

**Root cause**: Manual training record update process has no automated reminder when SOPs are revised.

**CAPA**: Linked to CAPA-2026-005 for implementation of automated training record updates.

### F-002: Risk File Naming Inconsistency (Observation)

**Classification**: Observation
**Clause**: SOP-007 §5.1 (recommended practice)

Risk files across Project Alpha and Project Beta use slightly different naming conventions (e.g., `RISK-Alpha-001` vs `Risk_Beta_001`). While both are within the tolerance defined in the file naming work instruction, standardization would improve consistency.

**Recommendation**: Consider updating WI-003 to include a mandatory naming template for risk files.

### F-003: Design Review Minutes Not Recorded (Major NC)

**Classification**: Major Nonconformance
**Clause**: ISO 13485 §7.3.5, SOP-007 §4.2

Design review meeting minutes for Project Alpha sprint review on 2026-02-28 were not formally recorded. Interviews confirmed the meeting occurred and decisions were made, but no meeting minutes document exists in the design history file.

**Impact**: Missing design review records represent a gap in the design history file required by §7.3.10 and could impact regulatory submission readiness.

**CAPA**: Linked to CAPA-2026-006 for corrective action including process reinforcement and implementation of automated meeting minutes templates.

## Conclusion

The Design Control process is generally well-implemented with strong design input/output documentation and effective verification activities. However, three findings were identified:

- **1 Major NC** (F-003): Missing design review minutes — requires immediate CAPA
- **1 Minor NC** (F-001): Training records not updated — CAPA initiated
- **1 Observation** (F-002): Naming convention inconsistency — recommendation only

The major nonconformance (F-003) requires priority attention as it affects design history file completeness. CAPA-2026-006 has been initiated with a target closure date of 2026-04-30.

Overall audit assessment: The design control process meets ISO 13485 requirements with the noted exceptions. Follow-up verification of CAPAs is scheduled for the Q3 2026 audit cycle.
