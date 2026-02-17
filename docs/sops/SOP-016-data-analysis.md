---
id: SOP-016
title: Data Analysis
status: approved
author: quality@example.com
reviewers:
  - management
approvers:
  - quality-lead
training:
  required_departments:
    - Quality
  training_mode: quiz
  due_days: 30
---

# SOP-016: Data Analysis

## 1. Purpose

Determine, collect, and analyze appropriate data to demonstrate the suitability, adequacy, and effectiveness of the QMS and to identify opportunities for improvement.

## 2. Scope

Applies to all quality data generated across QMS processes, including product quality data, process performance data, supplier data, and post-market data.

## 3. Definitions

| Term | Definition |
| --- | --- |
| Trend Analysis | Statistical examination of data over time to identify patterns |
| Key Quality Indicator (KQI) | Measurable value that demonstrates QMS effectiveness |
| Adverse Trend | A pattern indicating deterioration in quality, safety, or process performance |

## 4. Responsibilities

- **Quality**: Define data collection requirements, perform analysis, generate reports, escalate adverse trends
- **Department Heads**: Provide process performance data, participate in data review
- **Management**: Review data analysis results during management review, allocate resources for improvement

## 5. Procedure

### 5.1 Data Sources

| Data Source | Responsible | Frequency |
| --- | --- | --- |
| Customer complaints and feedback | Quality | Ongoing collection, quarterly analysis |
| Nonconformance reports | Quality | Ongoing collection, quarterly analysis |
| CAPA records and effectiveness | Quality | Ongoing collection, quarterly analysis |
| Internal audit findings | Quality | Per audit schedule |
| Supplier performance | Quality | Annually per supplier |
| Training compliance | Quality | Monthly monitoring |
| Product defect metrics | Engineering | Per release, monthly trending |
| Production/deployment metrics | Engineering | Continuous monitoring |
| Post-market surveillance data | Regulatory | Per PMS plan schedule |
| Process cycle times | All departments | Quarterly |

### 5.2 Key Quality Indicators

| KQI | Target | Escalation Threshold |
| --- | --- | --- |
| CAPA closure rate (within due date) | ≥ 90% | < 80% |
| CAPA effectiveness (no recurrence) | ≥ 90% | < 80% |
| Training completion (within due date) | 100% | < 95% |
| Customer complaint response time | ≤ 3 business days | > 5 business days |
| Complaint investigation closure | ≤ 30 days | > 45 days |
| Defect escape rate (post-release defects / total defects) | ≤ 5% | > 10% |
| Supplier nonconformance rate | ≤ 2 per supplier per year | > 4 per supplier per year |
| Internal audit finding closure | ≤ 30 days | > 45 days |

### 5.3 Analysis Methods

| Method | Application |
| --- | --- |
| Trend charts (run charts, control charts) | Monitoring KQIs over time |
| Pareto analysis | Identifying top contributors to complaints, defects, nonconformances |
| Root cause categorization | Classifying CAPA root causes to identify systemic issues |
| Comparative analysis | Comparing performance across products, releases, or periods |

### 5.4 Reporting

| Report | Audience | Frequency |
| --- | --- | --- |
| Quality Dashboard | All departments | Monthly |
| Quarterly Quality Report | Management, department heads | Quarterly |
| Annual Quality Trend Report | Top management (management review input) | Annually |
| Supplier Performance Summary | Quality, procurement | Annually |

### 5.5 Escalation

When an adverse trend is identified:

1. Quality documents the trend with supporting data
2. Risk assessment performed (is there a safety impact?)
3. If safety-related: escalate to risk management for update
4. If process-related: initiate CAPA per [SOP-004](SOP-004-capa.md)
5. Report adverse trends to management

### 5.6 Input to Management Review

Data analysis outputs are a required input to management review (per [SOP-006](SOP-006-management-review.md)):

- KQI performance vs. targets
- Identified trends (positive and negative)
- Recommended improvement actions
- Resource needs identified through data analysis

## 6. Records

- Quality dashboards and reports
- Quarterly and annual quality reports
- Trend analysis records
- Escalation and risk assessment records

## 7. References

- ISO 13485:2016 Section 8.4
- 21 CFR 820.250
- [SOP-004](SOP-004-capa.md) — CAPA
- [SOP-006](SOP-006-management-review.md) — Management Review
- [SOP-010](SOP-010-feedback-complaints.md) — Customer Feedback and Complaint Handling
