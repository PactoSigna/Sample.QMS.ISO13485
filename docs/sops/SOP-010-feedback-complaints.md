---
id: SOP-010
title: Customer Feedback and Complaint Handling
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
    - Quality
    - Engineering
  training_mode: quiz
  due_days: 30
---

# SOP-010: Customer Feedback and Complaint Handling

> **Document Type**: Standard Operating Procedure
> **Regulatory Basis**: ISO 13485:2016 Sections 8.2.1, 8.2.2
> **Status**: Effective
> **Last Updated**: 2026-04-05
> **Owner**: PactoSigna Quality
> **Review Cycle**: Annual

## 1. Purpose

This procedure establishes the requirements for collecting, evaluating, investigating, and resolving customer feedback and complaints related to medical device software products. It defines how PactoSigna's Quality Events module manages the complete complaint lifecycle with automated escalation paths, audit trails, and regulatory reporting support.

## 2. Scope

This SOP applies to all feedback and complaints received from:

- Customers and end users
- Healthcare professionals
- Distributors and partners
- Regulatory authorities
- Internal sources (employees identifying field issues)

This SOP covers the full lifecycle from initial receipt through investigation, determination, and closure, including escalation to nonconformance and CAPA processes when warranted.

## 3. Definitions

| Term | Definition |
| --- | --- |
| **Feedback** | Any communication from a customer about the product, positive or negative, that does not allege a specific deficiency in safety, performance, or quality |
| **Complaint** | Any written, electronic, or oral communication that alleges deficiencies related to identity, quality, durability, reliability, usability, safety, or performance of a medical device after release |
| **Adverse Event** | An incident involving a medical device that led to or might have led to death or serious deterioration in health of a patient, user, or other person |
| **Quality Event** | A complaint, nonconformance, or CAPA record managed within PactoSigna's Quality Events module |
| **Vigilance Report** | A report submitted to a regulatory authority regarding a serious incident or field safety corrective action |

## 4. Roles and Responsibilities

| Role | Responsibilities |
| --- | --- |
| **Quality** | Receives and logs complaints in PactoSigna; conducts or coordinates investigations; determines regulatory reporting needs; monitors complaint trends; ensures timely closure |
| **Engineering** | Provides technical assessment for complaint investigations; identifies root causes in software; assesses impact on other product versions |
| **Regulatory** | Assesses regulatory reporting requirements (MDR vigilance, FDA MDR/MAUDE); prepares and submits vigilance reports; monitors regulatory feedback |
| **Customer Support** | Collects and forwards feedback and complaints to Quality; provides initial triage; maintains communication with complainants |
| **Management** | Reviews complaint trends during management review; allocates resources for investigation and resolution |

## 5. Procedure

### 5.1 Feedback Collection

Feedback shall be collected through:

- Customer support channels (email, tickets, phone)
- User surveys and satisfaction questionnaires
- Sales and account management interactions
- App store reviews and ratings
- User analytics and usage data
- Post-market surveillance activities

Feedback that does not allege a specific deficiency shall be logged, categorized, and analyzed for trends. Safety concerns identified in feedback shall be immediately escalated to Quality for complaint evaluation.

### 5.2 Complaint Receipt and Logging

1. All potential complaints shall be logged in PactoSigna's Quality Events module within **1 business day** of receipt.
2. PactoSigna automatically assigns a unique complaint identifier and sets the initial state to `received`.
3. The complaint record shall include:
   - Date and method of receipt
   - Source (complainant identity, if available)
   - Product and version affected
   - Description of the alleged deficiency
   - Initial severity assessment
4. PactoSigna's audit trail records the creation event with the logger's identity and timestamp.

### 5.3 Complaint State Machine

PactoSigna manages the complaint lifecycle through a defined state machine:

| State | Description | Exit Criteria |
| --- | --- | --- |
| `received` | Complaint logged; awaiting assessment | Quality completes initial assessment |
| `investigation` | Root cause analysis and impact assessment in progress | Investigation findings documented; determination made |
| `disposition` | Actions determined and being implemented | All required actions completed; regulatory reporting submitted if needed |
| `closed` | Complaint fully resolved | Quality approves closure; complainant notified |

### 5.4 Initial Assessment

Within **3 business days** of receipt, Quality shall determine:

1. **Is this a complaint?** If the communication does not allege a specific deficiency, classify as feedback and track per Section 5.1.
2. **Severity classification:**

   | Severity | Criteria | Response Timeline |
   | --- | --- | --- |
   | **Critical** | Potential patient safety risk; adverse event reported or plausible | Investigation within 24 hours; regulatory assessment within 48 hours |
   | **Major** | Significant functional impact; regulatory non-compliance; data integrity risk | Investigation within 5 business days |
   | **Minor** | Low impact; cosmetic issue; inconvenience with workaround | Investigation within 30 business days |

3. **Regulatory reporting assessment**: Critical complaints shall trigger immediate assessment for:
   - EU MDR vigilance reporting (Article 87)
   - FDA Medical Device Reporting (21 CFR Part 803)
   - FDA MAUDE database reporting
   - Other jurisdiction-specific requirements

### 5.5 Complaint Investigation

1. Quality shall assign an investigator (typically Engineering for software-related issues).
2. The investigation shall determine:
   - Root cause of the alleged deficiency
   - Whether the deficiency is confirmed or not substantiated
   - Scope of impact (other versions, other customers, other product areas)
   - Risk assessment of the deficiency
3. Investigation findings shall be documented in the complaint record in PactoSigna.
4. Investigation timelines:
   - Critical: Complete within **15 business days**
   - Major: Complete within **30 business days**
   - Minor: Complete within **60 business days**

### 5.6 Determination and Escalation

Based on investigation findings:

| Determination | Action | PactoSigna Workflow |
| --- | --- | --- |
| Corrective action needed | Initiate CAPA per [SOP-004](SOP-004-capa.md) | Complaint -> CAPA escalation in Quality Events |
| Nonconforming product identified | Initiate NC record | Complaint -> NC auto-escalation when severity warrants |
| Systemic issue identified | NC -> CAPA escalation | NC -> CAPA path for systemic issues requiring root cause elimination |
| Regulatory reporting required | Submit vigilance report | Regulatory assessment documented in complaint record |
| No action required | Document rationale | Justification recorded with Quality approval |

PactoSigna supports automatic escalation from Complaint to Nonconformance when severity warrants, and from NC to CAPA for systemic issues, maintaining full traceability across the escalation chain.

### 5.7 Complaint Closure

1. All planned actions shall be completed and verified.
2. The complainant shall be notified of the resolution (where contact information is available).
3. Quality shall close the complaint in PactoSigna with documented rationale.
4. PactoSigna's audit trail records the closure event with all supporting evidence.

### 5.8 Trending and Post-Market Surveillance

1. Complaint trends shall be analyzed quarterly using PactoSigna's Quality Events reporting:
   - Complaint volume by type, severity, and product area
   - Root cause category distribution
   - Time to closure metrics
   - Escalation rates (complaint -> NC -> CAPA)
2. Adverse trends shall be escalated to:
   - CAPA process for systemic corrective action
   - Risk management for risk assessment update
   - Post-market surveillance review
3. Post-market surveillance data, including complaint trends, shall be documented using PactoSigna's post-market surveillance and post-market feedback document types.
4. Trending data shall be reported in management review per [SOP-006](SOP-006-management-review.md).

### 5.9 Regulatory Reporting

1. When regulatory reporting is required, Regulatory shall:
   - Prepare the vigilance report per applicable jurisdiction requirements
   - Submit within regulatory timelines (EU MDR: 15 days for serious incidents; FDA MDR: 30 days or 5-day report for emergencies)
   - Document the submission in the complaint record in PactoSigna
2. PactoSigna's audit trail provides evidence of reporting timeliness for regulatory audits.
3. Regulatory reporting decisions (including decisions not to report, with rationale) shall be documented in the complaint record.

## 6. PactoSigna Platform Implementation

| Complaint Handling Requirement | PactoSigna Feature |
| --- | --- |
| Complaint lifecycle | Quality Events module with 4-state complaint state machine (`received` -> `investigation` -> `disposition` -> `closed`) |
| Unique identification | Automatic complaint ID assignment |
| Escalation paths | Complaint -> NC auto-escalation; NC -> CAPA escalation for systemic issues |
| Investigation tracking | Investigation findings documented within the complaint quality event record |
| Trend analysis | Quality Events reporting with complaint trends by type, severity, period, and root cause |
| Post-market surveillance | PMS and post-market feedback document types for trend documentation |
| Regulatory reporting evidence | Audit trail captures reporting decisions and submission timestamps |
| Audit trail | Immutable log of all complaint state changes, actions, and decisions |
| Management review input | Complaint trends aggregated for management review dashboard |

## 7. Related Documents

- [SOP-004](SOP-004-capa.md) -- Corrective and Preventive Action
- [SOP-006](SOP-006-management-review.md) -- Management Review
- [SOP-008](SOP-008-internal-audit.md) -- Internal Audit
- [POL-001](../policies/POL-001-quality-policy.md) -- Quality Policy

## 8. References

| Reference | Description |
| --- | --- |
| ISO 13485:2016 Section 8.2.1 | Feedback |
| ISO 13485:2016 Section 8.2.2 | Complaint handling |
| 21 CFR Part 820.198 | Complaint files |
| 21 CFR Part 803 | Medical device reporting |
| EU MDR 2017/745 Article 87 | Vigilance reporting |

## 9. Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 1.0 | 2026-01-15 | PactoSigna Quality | Initial release |
| 2.0 | 2026-04-05 | PactoSigna Quality | Rewritten with PactoSigna platform integration -- Quality Events complaint workflow, auto-escalation, post-market surveillance, regulatory reporting support |
