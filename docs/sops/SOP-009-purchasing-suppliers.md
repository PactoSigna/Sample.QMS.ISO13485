---
id: SOP-009
title: Purchasing and Supplier Management
status: approved
author: quality@example.com
reviewers:
  - engineering
approvers:
  - quality-lead
training:
  required_departments:
    - Quality
    - Engineering
  training_mode: quiz
  due_days: 30
---

# SOP-009: Purchasing and Supplier Management

## 1. Purpose

Ensure purchased products and services conform to specified requirements through supplier evaluation, selection, monitoring, and re-evaluation.

## 2. Scope

Applies to all external products and services that affect the quality of the medical device software, including:

- Cloud infrastructure and hosting services
- SOUP (Software of Unknown Provenance) and OTS (Off-The-Shelf) software components
- Development tools and CI/CD services
- Consulting and contract development services
- Calibration and testing services

## 3. Definitions

| Term | Definition |
| --- | --- |
| Supplier | External entity providing products or services |
| Critical Supplier | Supplier whose product or service directly affects device safety or regulatory compliance |
| SOUP | Software of Unknown Provenance — software that is already developed and generally available but not developed for the purpose of being incorporated into the medical device |
| Approved Supplier List (ASL) | Register of suppliers qualified to provide products or services |

## 4. Responsibilities

- **Quality**: Maintain the ASL, coordinate supplier evaluations, track supplier performance
- **Engineering**: Evaluate technical capability of suppliers, assess SOUP components
- **Requesting Department**: Define purchasing requirements, perform incoming verification

## 5. Procedure

### 5.1 Supplier Classification

| Classification | Criteria | Evaluation Rigor |
| --- | --- | --- |
| Critical | Direct impact on device safety, regulatory compliance, or core functionality | Full evaluation, annual re-evaluation |
| Non-Critical | Indirect impact on quality (e.g., office tools, non-production services) | Simplified evaluation, biennial re-evaluation |

### 5.2 Supplier Evaluation

New suppliers are evaluated against:

1. **Quality capability**: Quality certifications (ISO 13485, ISO 27001, SOC 2), quality management practices
2. **Technical capability**: Relevant experience, technical competence, support responsiveness
3. **Regulatory compliance**: Compliance with applicable regulations, data protection (GDPR, HIPAA)
4. **Financial stability**: Business continuity risk assessment
5. **Security posture**: For cloud/infrastructure suppliers — security certifications, incident response

Evaluation results are documented on the Supplier Evaluation Form.

### 5.3 Approved Supplier List

1. Suppliers meeting evaluation criteria are added to the ASL
2. ASL records: supplier name, classification, products/services, evaluation date, next re-evaluation date
3. ASL maintained by Quality and accessible to all departments
4. Purchases from non-ASL suppliers require Quality Manager approval

### 5.4 Purchasing Requirements

Purchase orders or service agreements must specify:

- Product or service description
- Quality requirements and acceptance criteria
- Applicable standards or specifications
- Right of access for verification (where applicable)

### 5.5 SOUP/OTS Component Management

For software components:

1. Identify component (name, version, license)
2. Assess risk per IEC 62304 based on safety classification
3. Verify component meets functional and security requirements
4. Monitor for updates, patches, and security vulnerabilities
5. Maintain SOUP register (per device documentation)

### 5.6 Incoming Verification

Purchased products and services are verified upon receipt:

- Software components: version verification, integrity check (checksums), license compliance
- Cloud services: SLA verification, security configuration review
- Consulting deliverables: technical review against requirements

### 5.7 Supplier Monitoring and Re-evaluation

1. Critical suppliers re-evaluated annually; non-critical suppliers biennially
2. Monitoring inputs: delivery performance, quality of deliverables, incident history, support responsiveness
3. Supplier nonconformances documented and communicated to supplier
4. Persistent nonconformances may result in removal from ASL

## 6. Records

- Supplier evaluation forms
- Approved Supplier List
- Purchase orders and service agreements
- Incoming verification records
- Supplier performance records
- Supplier nonconformance reports

## 7. References

- ISO 13485:2016 Section 7.4
- 21 CFR 820.50
- IEC 62304 — SOUP management requirements
- [SOP-013](SOP-013-software-lifecycle.md) — Software Lifecycle
