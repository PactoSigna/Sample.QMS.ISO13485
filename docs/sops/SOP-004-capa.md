---
id: SOP-004
title: Corrective and Preventive Action
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
  training_mode: quiz
  due_days: 30
---

# SOP-004: Corrective and Preventive Action (CAPA)

> **Document Type**: Standard Operating Procedure
> **Regulatory Basis**: ISO 13485:2016 Sections 8.5.2, 8.5.3
> **Status**: Effective
> **Last Updated**: 2026-04-05
> **Owner**: PactoSigna Quality
> **Review Cycle**: Annual

## 1. Purpose

This procedure establishes the requirements for identifying, investigating, implementing, and verifying corrective and preventive actions to eliminate the causes of actual and potential nonconformities. It defines how PactoSigna's Quality Events module provides an integrated, auditable CAPA lifecycle with electronic signature gates and automated tracking.

## 2. Scope

This SOP applies to corrective and preventive actions initiated from any of the following sources:

- Customer complaints (escalated from PactoSigna's Complaint workflow)
- Nonconformances (escalated from PactoSigna's NC workflow)
- Internal and external audit findings
- Management review action items
- Risk management findings
- Process performance trends
- Post-market surveillance data
- Regulatory authority notifications

This SOP does not apply to immediate corrections that do not require root cause investigation (e.g., simple data entry errors corrected at the point of discovery).

## 3. Definitions

| Term | Definition |
| --- | --- |
| **Corrective Action** | Action taken to eliminate the cause of a detected nonconformity or other undesirable situation to prevent recurrence |
| **Preventive Action** | Action taken to eliminate the cause of a potential nonconformity or other undesirable situation to prevent occurrence |
| **CAPA** | Corrective and Preventive Action -- the combined process of investigation, root cause analysis, action implementation, and effectiveness verification |
| **Quality Event** | A complaint, nonconformance, or CAPA record managed within PactoSigna's Quality Events module |
| **Root Cause** | The fundamental reason why a nonconformity occurred, identified through systematic analysis |
| **Effectiveness Verification** | Objective evidence that the implemented corrective or preventive action achieved its intended result |

## 4. Roles and Responsibilities

| Role | Responsibilities |
| --- | --- |
| **CAPA Initiator** | Creates the CAPA record in PactoSigna's Quality Events module; provides initial problem description and supporting evidence |
| **CAPA Owner** | Leads the investigation; performs root cause analysis; develops and implements the action plan; provides completion evidence |
| **Quality** | Reviews CAPA records at each state transition; performs effectiveness verification; monitors CAPA metrics and trends; ensures timely closure |
| **Action Owners** | Complete assigned actions within due dates; provide completion evidence documented in PactoSigna |
| **Management** | Reviews CAPA trends during management review; provides resources for CAPA implementation; approves high-impact corrective actions |

## 5. Procedure

### 5.1 CAPA Initiation

1. Any member may initiate a CAPA by creating a quality event record in PactoSigna's Quality Events module.
2. The CAPA record shall include:
   - Problem description with sufficient detail for investigation
   - Source of the CAPA (complaint, NC, audit finding, etc.)
   - Link to the originating quality event (if applicable -- Complaint or NC record)
   - Initial severity assessment
   - Affected products or processes
3. PactoSigna automatically assigns the CAPA a unique identifier and sets the initial state to `open`.
4. PactoSigna's audit trail records the creation event with the initiator's identity and timestamp.

### 5.2 CAPA State Machine

PactoSigna manages the CAPA lifecycle through a defined state machine with electronic signature gates at key transitions:

| State | Description | Exit Criteria |
| --- | --- | --- |
| `open` | CAPA created; awaiting assignment and investigation start | CAPA owner assigned; investigation scope defined |
| `investigation` | Root cause analysis in progress | Root cause identified and documented; extent of problem determined |
| `action_plan` | Corrective/preventive actions defined | Actions assigned to owners with due dates; verification criteria established |
| `implementation` | Actions being executed | All actions completed with evidence; affected documents updated |
| `verification` | Effectiveness being verified | Objective evidence confirms actions were effective |
| `closed` | CAPA complete | Quality approves closure with electronic signature |

Electronic signatures are required at the following transitions:

- `investigation` -> `action_plan`: CAPA owner certifies root cause analysis is complete
- `implementation` -> `verification`: CAPA owner certifies all actions are implemented
- `verification` -> `closed`: Quality certifies effectiveness is verified

### 5.3 Investigation

1. The CAPA owner shall perform a root cause analysis using one or more of the following methods:

   | Method | When to Use |
   | --- | --- |
   | 5 Whys | Simple cause-and-effect chains; single root cause suspected |
   | Fishbone (Ishikawa) | Multiple potential cause categories; complex problems |
   | Fault Tree Analysis | Safety-critical issues; probabilistic analysis needed |
   | Is/Is Not Analysis | Narrowing problem scope; distinguishing symptoms from causes |

2. The investigation shall determine:
   - The root cause(s) of the nonconformity
   - The extent of the problem (other products, processes, or documents affected)
   - Whether similar issues exist elsewhere (horizontal deployment)
   - Risk assessment of the nonconformity's impact
3. Investigation findings shall be documented in the CAPA record in PactoSigna, including supporting evidence.
4. PactoSigna's root cause classification taxonomy allows categorization for trend analysis.

### 5.4 Action Planning

1. The CAPA owner shall define corrective actions that address the identified root cause(s).
2. The CAPA owner shall define preventive actions to prevent recurrence or occurrence of similar issues.
3. Each action shall specify:
   - Description of the action
   - Assigned owner
   - Target completion date
   - Verification criteria (how effectiveness will be measured)
4. Actions are tracked within PactoSigna's Quality Events module with due date monitoring.
5. If actions require document changes, the changes shall follow [SOP-001](SOP-001-document-control.md) (Document Control).
6. If actions require design changes, the changes shall follow [SOP-002](SOP-002-design-development.md) (Design and Development) with a Design Change Order.

### 5.5 Implementation

1. Action owners shall execute their assigned actions within the target dates.
2. Each completed action shall include documented evidence of completion in PactoSigna.
3. If implementation requires updating controlled documents, training re-assignment is automatically triggered by PactoSigna when the updated documents are released.
4. The CAPA owner shall verify that all planned actions have been completed before requesting transition to `verification`.

### 5.6 Effectiveness Verification

1. Quality shall verify that the implemented actions achieved their intended results.
2. Verification methods include:
   - Review of process performance data after implementation
   - Absence of recurrence within a defined monitoring period (minimum 30 days for minor issues, 90 days for major issues)
   - Audit of the corrected process or document
   - Review of complaint/NC trends related to the original issue
3. If verification determines the actions were not effective:
   - The CAPA shall be returned to `investigation` for re-analysis
   - The reason for ineffectiveness shall be documented
   - Escalation to management shall occur if the issue has patient safety implications
4. PactoSigna captures the verification decision with an electronic signature from Quality.

### 5.7 CAPA Closure

1. Upon successful effectiveness verification, Quality shall close the CAPA with an electronic signature in PactoSigna.
2. The closure record shall include:
   - Summary of the root cause and actions taken
   - Evidence of effectiveness
   - Any remaining monitoring requirements
3. PactoSigna's audit trail records the closure event with full traceability to all state transitions, actions, and signatures.

### 5.8 CAPA Metrics and Trending

1. PactoSigna auto-generates CAPA metrics including:
   - Number of open/closed CAPAs by period
   - Average time to closure by severity
   - Root cause category distribution
   - Effectiveness rate (first-time vs. re-opened)
   - Overdue action rate
2. CAPA trends shall be reviewed during management review per [SOP-006](SOP-006-management-review.md).
3. Adverse trends (increasing frequency, decreasing effectiveness) shall trigger a systemic review.

## 6. PactoSigna Platform Implementation

| CAPA Requirement | PactoSigna Feature |
| --- | --- |
| CAPA lifecycle | Quality Events module with 6-state CAPA state machine (`open` -> `investigation` -> `action_plan` -> `implementation` -> `verification` -> `closed`) |
| Electronic signature gates | Part 11-compliant signatures required at key state transitions |
| Action tracking | Action items with owners, due dates, and completion evidence within the CAPA record |
| Root cause classification | Taxonomy for categorizing root causes, enabling trend analysis |
| Escalation from NC/Complaint | Linked quality events -- Complaint -> NC -> CAPA workflow with full traceability |
| Metrics and reporting | Auto-generated CAPA metrics and trend reports for management review |
| Audit trail | Immutable log of all CAPA state changes, actions, and signatures with timestamps and actor identity |
| Document change integration | CAPA actions that require document updates flow through the document control and release workflow |

## 7. Related Documents

- [SOP-001](SOP-001-document-control.md) -- Document Control
- [SOP-002](SOP-002-design-development.md) -- Design and Development
- [SOP-006](SOP-006-management-review.md) -- Management Review
- [SOP-008](SOP-008-internal-audit.md) -- Internal Audit
- [SOP-010](SOP-010-feedback-complaints.md) -- Customer Feedback and Complaint Handling
- [POL-001](../policies/POL-001-quality-policy.md) -- Quality Policy

## 8. References

| Reference | Description |
| --- | --- |
| ISO 13485:2016 Section 8.5.2 | Corrective action |
| ISO 13485:2016 Section 8.5.3 | Preventive action |
| 21 CFR Part 820.90 | Nonconforming product |
| 21 CFR Part 820.100 | Corrective and preventive action |

## 9. Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 1.0 | 2026-01-15 | PactoSigna Quality | Initial release |
| 2.0 | 2026-04-05 | PactoSigna Quality | Rewritten with PactoSigna platform integration -- Quality Events module, CAPA state machine, electronic signature gates, action tracking, metrics |
