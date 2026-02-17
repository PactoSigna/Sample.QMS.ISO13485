---
id: SOP-010
title: Customer Feedback and Complaint Handling
status: approved
author: quality@example.com
reviewers:
  - engineering
  - regulatory
approvers:
  - quality-lead
training:
  required_departments:
    - Quality
    - Engineering
  training_mode: quiz
  due_days: 30
---

# SOP-010: Customer Feedback and Complaint Handling

## 1. Purpose

Collect, evaluate, and act on customer feedback. Investigate and resolve complaints in a timely manner. Ensure potential safety issues are identified and escalated appropriately.

## 2. Scope

Applies to all feedback and complaints received from customers, users, healthcare professionals, distributors, and regulatory authorities related to medical device software products.

## 3. Definitions

| Term | Definition |
| --- | --- |
| Feedback | Any communication from a customer about the product, positive or negative, that does not allege a specific deficiency |
| Complaint | Any written, electronic, or oral communication that alleges deficiencies related to identity, quality, durability, reliability, usability, safety, or performance of a medical device after release |
| Adverse Event | An incident involving a medical device that led to or might have led to death or serious deterioration of health |

## 4. Responsibilities

- **Quality**: Receive and log complaints, conduct investigations, determine regulatory reporting needs, maintain complaint database
- **Engineering**: Provide technical assessment for complaint investigations
- **Regulatory**: Assess regulatory reporting requirements, submit vigilance reports
- **Customer Support**: Collect and forward feedback and complaints to Quality

## 5. Procedure

### 5.1 Feedback Collection

Feedback is collected through:

- Customer support channels (email, tickets)
- User surveys and satisfaction questionnaires
- Sales and account management interactions
- App store reviews and ratings
- User analytics and usage data

### 5.2 Feedback Analysis

1. Feedback is categorized: feature request, usability, performance, satisfaction, safety concern
2. Safety concerns are immediately escalated to Quality for complaint evaluation
3. Feedback trends are analyzed quarterly
4. Trending data is input to management review (per [SOP-006](SOP-006-management-review.md))

### 5.3 Complaint Receipt and Logging

1. All potential complaints are logged within 1 business day of receipt
2. Complaint record includes: date received, source, product/version, description, initial severity assessment
3. Quality assigns a unique complaint ID

### 5.4 Complaint Assessment

Within 3 business days of receipt, Quality determines:

1. Is this a complaint per the definition? (If not, categorize as feedback)
2. Initial severity classification:
   - **Critical**: Potential patient safety risk or adverse event
   - **Major**: Significant functional impact or regulatory non-compliance
   - **Minor**: Low impact, cosmetic, or inconvenience

3. Critical complaints trigger immediate assessment for regulatory reporting (per [SOP-012](SOP-012-regulatory-reporting.md))

### 5.5 Complaint Investigation

1. Quality assigns investigator (typically Engineering for technical issues)
2. Investigation scope: root cause analysis, scope of impact, risk assessment
3. Investigation to be completed within 30 days (critical: 15 days)
4. Investigation documented in complaint record

### 5.6 Determination and Action

Based on investigation:

1. **Corrective action needed?** → Initiate CAPA per [SOP-004](SOP-004-capa.md)
2. **Regulatory reporting needed?** → Follow [SOP-012](SOP-012-regulatory-reporting.md)
3. **Advisory notice needed?** → Follow [SOP-012](SOP-012-regulatory-reporting.md)
4. **Nonconforming product?** → Follow [SOP-011](SOP-011-nonconforming-product.md)
5. **No action needed?** → Document rationale for no action

### 5.7 Complaint Closure

1. All actions completed and verified
2. Complainant notified of resolution (where contact information available)
3. Complaint record closed by Quality

### 5.8 Trending

1. Complaint trends analyzed quarterly (type, severity, product area, root cause category)
2. Adverse trends escalated to CAPA
3. Safety signals escalated to risk management for update
4. Trends reported in management review

## 6. Records

- Feedback log
- Complaint records (including investigation and determination)
- Complaint trend reports
- Regulatory reporting decisions

## 7. References

- ISO 13485:2016 Sections 8.2.1, 8.2.2
- 21 CFR 820.198
- EU MDR 2017/745 Article 87
- [SOP-004](SOP-004-capa.md) — CAPA
- [SOP-011](SOP-011-nonconforming-product.md) — Nonconforming Product
- [SOP-012](SOP-012-regulatory-reporting.md) — Regulatory Reporting
