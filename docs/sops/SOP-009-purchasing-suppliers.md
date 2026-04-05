---
id: SOP-009
title: Purchasing and Supplier Management
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

# SOP-009: Purchasing and Supplier Management

> **Document Type**: Standard Operating Procedure
> **Regulatory Basis**: ISO 13485:2016 Section 7.4
> **Status**: Effective
> **Last Updated**: 2026-04-05
> **Owner**: PactoSigna Quality
> **Review Cycle**: Annual

## 1. Purpose

This procedure establishes the requirements for evaluating, selecting, monitoring, and re-evaluating suppliers of products and services that affect medical device software quality. It defines how PactoSigna's supplier document type, SOUP register, and SBOM capabilities support controlled purchasing and supplier management.

## 2. Scope

This SOP applies to all external products and services that affect the quality of the medical device software, including:

- Cloud infrastructure and hosting services (e.g., Google Cloud Platform, Firebase)
- SOUP (Software of Unknown Provenance) and OTS (Off-The-Shelf) software components
- Development tools and CI/CD services
- Consulting and contract development services
- Testing and calibration services
- Data processing and storage services

This SOP does not cover general office supplies, facilities, or services that have no impact on product quality.

## 3. Definitions

| Term | Definition |
| --- | --- |
| **Supplier** | External entity providing products or services that affect medical device quality |
| **Critical Supplier** | A supplier whose product or service directly affects device safety, core functionality, or regulatory compliance |
| **SOUP** | Software of Unknown Provenance -- software not developed for the specific purpose of being incorporated into the medical device (e.g., open-source libraries, third-party SDKs) |
| **SBOM** | Software Bill of Materials -- a comprehensive inventory of all software components, including SOUP, with versions and licenses |
| **Approved Supplier List (ASL)** | The register of qualified suppliers, maintained as supplier documents in PactoSigna |
| **Quality Agreement** | A documented agreement between the organization and a supplier defining quality requirements, responsibilities, and expectations |

## 4. Roles and Responsibilities

| Role | Responsibilities |
| --- | --- |
| **Quality** | Maintains the ASL as supplier documents in PactoSigna; coordinates supplier evaluations; tracks supplier performance; manages re-evaluation schedule |
| **Engineering** | Evaluates technical capability of suppliers; assesses SOUP components for safety and security; maintains the SOUP register and SBOM |
| **Requesting Department** | Defines purchasing requirements; performs incoming verification of received products or services |
| **Regulatory** | Reviews supplier compliance with applicable regulations; assesses impact of supplier changes on regulatory submissions |

## 5. Procedure

### 5.1 Supplier Classification

| Classification | Criteria | Evaluation Rigor | Re-evaluation Frequency |
| --- | --- | --- | --- |
| **Critical** | Direct impact on device safety, regulatory compliance, or core functionality | Full evaluation with documented evidence | Annual |
| **Non-Critical** | Indirect impact on quality (e.g., development tools, non-production services) | Simplified evaluation | Biennial |

### 5.2 Supplier Evaluation

New suppliers shall be evaluated against the following criteria before approval:

1. **Quality capability**: Quality certifications (ISO 13485, ISO 27001, SOC 2), documented quality management practices
2. **Technical capability**: Relevant experience, technical competence, support responsiveness, product maturity
3. **Regulatory compliance**: Compliance with applicable regulations (GDPR, HIPAA), data residency requirements
4. **Security posture**: For cloud and infrastructure suppliers -- security certifications, incident response procedures, encryption standards, vulnerability management
5. **Financial stability**: Business continuity risk, viability for long-term partnership
6. **References**: Customer references and industry reputation

Evaluation results shall be documented in a supplier document in PactoSigna with structured frontmatter including supplier name, category, status, and evaluation date.

### 5.3 Approved Supplier List

1. Suppliers meeting evaluation criteria shall be documented as `supplier` type documents in PactoSigna with frontmatter capturing:
   - Supplier name and contact information
   - Classification (critical / non-critical)
   - Products or services provided
   - Evaluation date and score
   - Next re-evaluation date
   - Approval status
2. The ASL shall be maintained by Quality and accessible to all departments through PactoSigna.
3. Purchases from suppliers not on the ASL require Quality Manager approval with documented justification.

### 5.4 Quality Agreements

1. Critical suppliers shall have a documented quality agreement covering:
   - Quality requirements and acceptance criteria
   - Change notification requirements (supplier must notify of changes that could affect product quality)
   - Right of access for verification or audit
   - Nonconformance reporting requirements
   - Corrective action expectations
   - Record retention requirements
2. Quality agreement requirements shall be documented in the supplier's PactoSigna document as required sections.

### 5.5 SOUP and OTS Component Management

For software components (SOUP/OTS):

1. **Identification**: Document each component with name, version, license, and source.
2. **Risk assessment**: Assess risk per IEC 62304 based on the device's safety classification (Class A, B, or C). Higher safety classes require more rigorous SOUP assessment.
3. **Functional verification**: Verify the component meets functional and security requirements for its intended use.
4. **Vulnerability monitoring**: Monitor for security vulnerabilities, patches, and end-of-life announcements.
5. **SOUP register**: Maintain the SOUP register as part of the device documentation in PactoSigna, linked to risk assessments.
6. **SBOM**: PactoSigna captures the Software Bill of Materials for each release, providing a complete inventory of software components.

### 5.6 Incoming Verification

Purchased products and services shall be verified upon receipt:

| Product/Service Type | Verification Method |
| --- | --- |
| Software components (SOUP) | Version verification, integrity check (checksums/signatures), license compliance, security scan |
| Cloud services | SLA verification, security configuration review, data residency confirmation |
| Consulting deliverables | Technical review against requirements, code review for contributed code |
| Testing services | Review of test reports, methodology validation, certification verification |

### 5.7 Supplier Monitoring and Re-Evaluation

1. Critical suppliers shall be re-evaluated annually; non-critical suppliers biennially.
2. Monitoring inputs include:
   - Delivery performance and timeliness
   - Quality of deliverables and defect rates
   - Incident history and response quality
   - Support responsiveness
   - Security incidents or vulnerability disclosures
   - Compliance with quality agreement terms
3. Supplier nonconformances shall be documented and communicated to the supplier.
4. Persistent nonconformances or critical failures may result in:
   - Corrective action request to the supplier
   - Increased monitoring frequency
   - Removal from the ASL with transition plan
5. Re-evaluation results shall update the supplier document in PactoSigna with new evaluation date and findings.

### 5.8 Supplier Change Management

1. Suppliers shall notify the organization of changes that could affect product quality (per quality agreement).
2. Significant supplier changes shall be assessed for impact on:
   - Device safety and performance
   - Regulatory compliance
   - Existing risk assessments
3. If impact is identified, follow [SOP-002](SOP-002-design-development.md) design change procedures.

## 6. PactoSigna Platform Implementation

| Supplier Management Requirement | PactoSigna Feature |
| --- | --- |
| Approved Supplier List | `supplier` document type with structured frontmatter (name, category, status, evaluation) |
| Quality agreements | Required sections in supplier documents for quality agreement terms |
| SOUP register | SOUP components documented in device repository, linked to risk assessments |
| SBOM | Software Bill of Materials captured per release |
| Supplier status tracking | Document status lifecycle for supplier approval and re-evaluation |
| Evaluation records | Supplier evaluation history maintained in document version history |
| Document control | Supplier documents managed under full document control per SOP-001 |
| Audit trail | All supplier document changes captured in PactoSigna's immutable audit log |

## 7. Related Documents

- [SOP-001](SOP-001-document-control.md) -- Document Control
- [SOP-002](SOP-002-design-development.md) -- Design and Development
- [SOP-004](SOP-004-capa.md) -- Corrective and Preventive Action
- [SOP-006](SOP-006-management-review.md) -- Management Review

## 8. References

| Reference | Description |
| --- | --- |
| ISO 13485:2016 Section 7.4 | Purchasing |
| ISO 13485:2016 Section 7.4.1 | Purchasing process |
| ISO 13485:2016 Section 7.4.2 | Purchasing information |
| ISO 13485:2016 Section 7.4.3 | Verification of purchased product |
| IEC 62304:2006+A1:2015 | SOUP management requirements |
| 21 CFR Part 820.50 | Purchasing controls |

## 9. Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 1.0 | 2026-01-15 | PactoSigna Quality | Initial release |
| 2.0 | 2026-04-05 | PactoSigna Quality | Rewritten with PactoSigna platform integration -- supplier document type, SOUP register, SBOM, quality agreements, supplier status lifecycle |
