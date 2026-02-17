---
id: SOP-012
title: Regulatory Reporting and Advisory Notices
status: approved
author: quality@example.com
reviewers:
  - quality
approvers:
  - regulatory-lead
training:
  required_departments:
    - Quality
    - Regulatory
  training_mode: quiz
  due_days: 30
---

# SOP-012: Regulatory Reporting and Advisory Notices

## 1. Purpose

Ensure timely identification, assessment, and reporting of incidents to regulatory authorities. Define the process for issuing advisory notices and field safety corrective actions.

## 2. Scope

Applies to all reportable events involving medical device software products marketed in any jurisdiction.

## 3. Definitions

| Term | Definition |
| --- | --- |
| Serious Incident | Any incident that directly or indirectly led to, might have led to, or might lead to death, serious deterioration of health, or serious public health threat |
| Field Safety Corrective Action (FSCA) | Action taken to reduce a risk of death or serious deterioration of health associated with the use of a medical device that is already placed on the market |
| Advisory Notice | Communication sent to users or customers about an FSCA |
| Vigilance Report | Report submitted to a regulatory authority about a serious incident or FSCA |

## 4. Responsibilities

- **Regulatory**: Lead reportability assessments, prepare and submit vigilance reports, manage advisory notices
- **Quality**: Coordinate investigations, maintain reportability assessment records
- **Engineering**: Provide technical analysis for investigations
- **Management**: Approve FSCAs and advisory notices

## 5. Procedure

### 5.1 Reportability Assessment

When a potential reportable event is identified (from complaints, nonconformances, or post-market data):

1. Regulatory assesses whether the event meets reportability criteria
2. Assessment considers: severity of harm, causal relationship to the device, frequency
3. Assessment documented within 24 hours of becoming aware of the event
4. If uncertain, err on the side of reporting

### 5.2 Reporting Criteria by Jurisdiction

#### EU (MDR 2017/745 Article 87)

| Event Type | Reporting Timeline |
| --- | --- |
| Serious public health threat | 2 calendar days |
| Death or unanticipated serious deterioration of health | 10 calendar days |
| Other serious incidents | 15 calendar days |

Reports submitted via EUDAMED (or national competent authority if EUDAMED not available).

#### USA (FDA — 21 CFR Part 803)

| Event Type | Reporting Timeline |
| --- | --- |
| Death | 30 calendar days (5-day report if awareness of similar events) |
| Serious injury | 30 calendar days |
| Malfunction that could cause death or serious injury | 30 calendar days |

Reports submitted via FDA MedWatch (Form 3500A).

### 5.3 Report Preparation

1. Regulatory prepares the initial report with available information
2. Report includes: device identification, event description, patient outcome, root cause (if known), corrective actions taken or planned
3. If investigation is ongoing, submit initial report and provide follow-up reports as information becomes available
4. Quality Manager and Regulatory lead review and approve report before submission

### 5.4 Follow-up Reports

1. Follow-up reports submitted when new information becomes available
2. Final report submitted when investigation is complete
3. All follow-up reports reference the initial report

### 5.5 Field Safety Corrective Actions

When an FSCA is determined necessary:

1. Regulatory defines the scope of the FSCA (affected products, versions, markets)
2. Corrective action plan developed (software update, feature disable, product removal)
3. Plan approved by Management, Quality, and Regulatory
4. FSCA implemented per the corrective action plan
5. Regulatory notifies applicable competent authorities

### 5.6 Advisory Notices

1. Advisory notice content includes: device identification, description of the issue, risk to users/patients, recommended actions, contact information
2. Notice reviewed and approved by Regulatory and Management
3. Distribution method determined (email, in-app notification, postal mail) based on urgency and audience
4. Distribution records maintained

### 5.7 Effectiveness Verification

1. Verify advisory notice reached intended recipients
2. Verify corrective action was effective (monitor for recurrence)
3. Document effectiveness verification results
4. Submit effectiveness report to regulatory authorities as required

## 6. Records

- Reportability assessment records
- Vigilance reports (initial, follow-up, final)
- FSCA plans and implementation records
- Advisory notices and distribution records
- Effectiveness verification records

## 7. References

- ISO 13485:2016 Sections 8.2.3, 8.3.3
- EU MDR 2017/745 Articles 87-92
- 21 CFR Part 803 (MDR — Medical Device Reporting)
- MEDDEV 2.12/1 — Guidelines on a Medical Devices Vigilance System
- [SOP-004](SOP-004-capa.md) — CAPA
- [SOP-010](SOP-010-feedback-complaints.md) — Customer Feedback and Complaint Handling
- [SOP-011](SOP-011-nonconforming-product.md) — Nonconforming Product
