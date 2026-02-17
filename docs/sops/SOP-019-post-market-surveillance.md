---
id: SOP-019
title: Post-Market Surveillance
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

# SOP-019: Post-Market Surveillance

## 1. Purpose

Systematically collect, analyze, and act on post-market data to confirm the safety and performance of medical device software throughout its lifecycle.

## 2. Scope

Applies to all medical device software products placed on the market. Covers proactive and reactive data collection, analysis, and reporting.

## 3. Definitions

| Term | Definition |
| --- | --- |
| Post-Market Surveillance (PMS) | Systematic process to collect and analyze experience gained from devices placed on the market |
| PMS Plan | Device-specific plan describing data sources, methods, and frequencies for post-market data collection |
| PMS Report | Summary document of PMS activities and findings (Class I devices) |
| Periodic Safety Update Report (PSUR) | Comprehensive safety report for Class IIa and higher devices |
| Post-Market Clinical Follow-up (PMCF) | Clinical evaluation activity to collect and evaluate clinical data after device marketing |

## 4. Responsibilities

- **Regulatory**: Develop PMS plans, prepare PMS reports and PSURs, manage PMCF activities
- **Quality**: Provide complaint and nonconformance trend data, support analysis
- **Engineering**: Provide technical analysis, product performance data
- **Clinical**: Support clinical evaluation updates, literature monitoring

## 5. Procedure

### 5.1 PMS Plan

For each device (or device family):

1. Regulatory creates a PMS plan proportionate to the device risk class
2. Plan specifies:
   - Data sources (see Section 5.2)
   - Collection methods and frequencies
   - Analysis methods
   - Indicators and thresholds for action
   - Reporting requirements and timelines
   - Roles and responsibilities
3. PMS plan reviewed annually and updated as needed

### 5.2 Data Sources

| Source | Type | Collection Method |
| --- | --- | --- |
| Complaint and feedback data | Reactive | QMS platform (per [SOP-010](SOP-010-feedback-complaints.md)) |
| Vigilance and incident reports | Reactive | Regulatory databases (EUDAMED, MAUDE) |
| Scientific literature | Proactive | Periodic literature search (at least annually) |
| Similar device experience | Proactive | Regulatory database monitoring, competitor recalls |
| Product performance data | Proactive | Application monitoring, error logs, usage analytics |
| Clinical data and registries | Proactive | PMCF activities, clinical registries |
| Standards and regulatory updates | Proactive | Standards body notifications, regulatory publications |
| Field safety corrective actions | Reactive | Competent authority notifications |

### 5.3 Data Analysis

1. Data collected per the PMS plan schedule
2. Analysis includes:
   - Trend identification (increasing complaint types, new failure modes)
   - Safety signal detection (unexpected adverse events, new hazards)
   - Benefit-risk ratio assessment
   - Comparison with state of the art
3. Analysis results documented

### 5.4 Safety Signals and Escalation

When a safety signal is detected:

1. Assess signal strength and clinical significance
2. If confirmed safety issue:
   - Update risk management file (per [SOP-003](SOP-003-risk-management.md))
   - Assess need for corrective action (FSCA, per [SOP-012](SOP-012-regulatory-reporting.md))
   - Update clinical evaluation if applicable
   - Consider design changes (per [SOP-015](SOP-015-change-control.md))

### 5.5 PMS Report (Class I Devices)

1. Updated when necessary but at least annually
2. Content: summary of PMS activities, data analysis results, conclusions, actions taken
3. Made available to competent authorities upon request

### 5.6 PSUR (Class IIa and Higher)

1. Frequency:
   - Class IIa: at least every 2 years
   - Class IIb and III: annually
2. Content:
   - Conclusions of benefit-risk determination
   - Main findings from PMS data
   - Volume of sales and estimated population of patients/users
   - Summary of changes made to device during reporting period
   - Corrective actions taken
3. Submitted via EUDAMED (or to competent authority)

### 5.7 Clinical Evaluation Update

1. PMS data feeds into clinical evaluation (per EU MDR Article 61)
2. Clinical evaluation report updated when PMS data warrants it
3. PMCF activities conducted per PMCF plan

## 6. Records

- PMS plans (per device)
- PMS data collection records
- PMS reports (Class I)
- PSURs (Class IIa+)
- Literature search records
- Safety signal assessments

## 7. References

- EU MDR 2017/745 Articles 83-86
- MEDDEV 2.12/1 — Guidelines on a Medical Devices Vigilance System
- ISO 13485:2016 Section 8.2.1
- [SOP-003](SOP-003-risk-management.md) — Risk Management
- [SOP-010](SOP-010-feedback-complaints.md) — Customer Feedback and Complaint Handling
- [SOP-012](SOP-012-regulatory-reporting.md) — Regulatory Reporting
