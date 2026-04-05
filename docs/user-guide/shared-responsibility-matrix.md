---
id: GUIDE-SRM-001
title: "Shared Responsibility Matrix"
status: approved
author: quality
---

# Shared Responsibility Matrix

## Purpose

This document defines the shared responsibilities between PactoSigna (the platform) and the customer organization for meeting ISO 13485:2016 requirements. PactoSigna provides the infrastructure, automation, and tooling; the customer organization is responsible for content authoring, process execution, and regulatory compliance decisions.

## Scope

This matrix covers all ISO 13485:2016 clauses relevant to a medical device software company using PactoSigna as its QMS platform.

## How to Read This Matrix

- **PactoSigna Handles**: Capabilities provided by the platform out of the box or via configuration.
- **Customer Handles**: Responsibilities the customer organization must fulfill using the platform.
- **Shared**: Activities where both PactoSigna and the customer have responsibilities.

## Responsibility Matrix

| ISO 13485 Clause | Requirement Description | PactoSigna (Platform) Handles | Customer Organization Handles | Notes |
| --- | --- | --- | --- | --- |
| **4.1** | QMS General Requirements | Provides platform infrastructure, document management, and process automation | Establishes, documents, implements, and maintains the QMS; defines scope and exclusions | Customer defines QMS scope; PactoSigna provides the tooling |
| **4.2.1** | Documentation General | Provides 30+ document types with Zod-validated frontmatter schemas | Authors all QMS documentation content; defines quality policy and objectives | Platform enforces structure; customer provides substance |
| **4.2.2** | Quality Manual | Provides `quality_manual` document type with required sections validation | Authors and maintains the Quality Manual content | |
| **4.2.3** | Medical Device File | Provides Records Page with compiled views (DMR, DHR, RMF, V&V) | Ensures completeness of device documentation for each product | PactoSigna compiles; customer authors source documents |
| **4.2.4** | Control of Documents | Git-native version control; sync engine with schema validation; document status lifecycle (`draft` -> `in_review` -> `approved` -> `effective` -> `archived`); electronic signature gates | Authors document content; defines review and approval workflows; maintains document currency | See [SOP-001](../sops/SOP-001-document-control.md) |
| **4.2.5** | Control of Records | Immutable audit trail (80+ action types); server-generated timestamps; release snapshots | Ensures records are complete and accurate; defines retention periods per record type | PactoSigna provides immutability and retention infrastructure |
| **5.1** | Management Commitment | Not applicable (organizational responsibility) | Top management demonstrates commitment to QMS; communicates importance of meeting requirements | |
| **5.2** | Customer Focus | Provides Quality Events module for complaint and feedback tracking | Determines and meets customer requirements; monitors customer satisfaction | |
| **5.3** | Quality Policy | Provides `policy` document type with status tracking | Establishes, reviews, and communicates the quality policy | |
| **5.4** | Planning | Provides Quality Objectives collection with measurable targets and trending | Establishes quality objectives; plans QMS changes | |
| **5.5** | Responsibility, Authority, and Communication | Provides `job_description` document type with department and role frontmatter; role-based access control | Defines organizational structure; assigns responsibilities; appoints Management Representative | PactoSigna provides the doc type; customer populates role definitions |
| **5.6** | Management Review | Provides Quality Reviews collection; quality metrics dashboard; Quality Objectives tracking; compiled record views as evidence | Conducts management reviews; makes decisions on resources and improvements; records minutes and actions | See [SOP-006](../sops/SOP-006-management-review.md) |
| **6.1** | Provision of Resources | Not applicable (PactoSigna provides platform infrastructure only) | Determines and provides resources needed for QMS implementation, maintenance, and improvement | Customer-managed entirely |
| **6.2** | Human Resources | Training module with automatic assignment, quiz engine, overdue CRON worker, Part 11 signed completions; Competency View dashboard | Defines competency requirements; authors job descriptions; identifies training needs; evaluates training effectiveness | See [SOP-007](../sops/SOP-007-training-competence.md) |
| **6.3** | Infrastructure | Provides cloud platform infrastructure (hosting, storage, compute) for PactoSigna itself | Determines, provides, and maintains infrastructure needed for product realization | Customer-managed; PactoSigna provides only the QMS platform infrastructure |
| **6.4** | Work Environment | Not applicable | Determines and manages work environment needed for product conformity | Customer-managed entirely |
| **7.1** | Planning of Product Realization | Provides release workflow with DCO, signing obligations, and gap detection | Plans and develops processes needed for product realization; determines quality objectives and requirements | |
| **7.2** | Customer-Related Processes | Provides requirements document types (UN, PRS) with traceability frontmatter | Determines product requirements; reviews requirements; maintains customer communication | |
| **7.3** | Design and Development | Traceability engine (UN -> PRS -> SRS -> Tests/Risks -> HLD/SDD); gap detection for coverage analysis; release workflow with DCO; design review records (virtual views); IEC 62304 safety classification enforcement | Authors all design documents; performs design reviews; executes verification and validation; makes design decisions | See [SOP-002](../sops/SOP-002-design-development.md) |
| **7.4** | Purchasing | Provides `supplier` document type with evaluation frontmatter; SOUP register; SBOM per release; document status lifecycle for ASL management | Evaluates and selects suppliers; defines purchasing requirements; performs incoming verification; maintains quality agreements | See [SOP-009](../sops/SOP-009-purchasing-suppliers.md) |
| **7.5** | Production and Service Provision | Not directly applicable for pure SaMD; PactoSigna provides release snapshots as production records | Manages production processes; validates production and service provision | N/A for pure SaMD; customer-managed for hybrid devices |
| **7.6** | Control of Monitoring and Measuring Equipment | Not directly applicable for pure SaMD | Manages calibration and maintenance of monitoring equipment | N/A for pure SaMD; customer-managed for hybrid devices |
| **8.1** | Measurement, Analysis, Improvement | Provides quality metrics dashboard; trend analysis for CAPAs, complaints, training | Plans and implements monitoring, measurement, analysis, and improvement processes | |
| **8.2.1** | Feedback | Provides Quality Events module for feedback and complaint intake and trending | Collects customer feedback; analyzes trends; acts on findings | See [SOP-010](../sops/SOP-010-feedback-complaints.md) |
| **8.2.2** | Complaint Handling | Provides complaint state machine (`received` -> `investigation` -> `disposition` -> `closed`); automatic NC/CAPA escalation; audit trail | Investigates complaints; determines regulatory reporting needs; communicates with complainants | See [SOP-010](../sops/SOP-010-feedback-complaints.md) |
| **8.2.3** | Reporting to Regulatory Authorities | Provides audit trail evidence of reporting timeliness; complaint records with regulatory assessment fields | Prepares and submits vigilance and MDR reports; determines reportability | Customer responsibility; PactoSigna provides evidence |
| **8.2.4** | Internal Audit | Provides `audit_schedule` and `audit_report` document types; immutable audit trail as evidence; compliance packages for export; CAPA integration for findings | Plans and conducts internal audits; selects and qualifies auditors; follows up on findings | See [SOP-008](../sops/SOP-008-internal-audit.md) |
| **8.3** | Control of Nonconforming Product | Provides NC workflow in Quality Events module with state machine and escalation to CAPA | Identifies, documents, and dispositions nonconforming product; implements controls | |
| **8.4** | Analysis of Data | Provides quality metrics dashboard; CAPA, complaint, training, and release trending | Determines, collects, and analyzes appropriate data; identifies improvement opportunities | |
| **8.5.2** | Corrective Action | Provides CAPA state machine (6 states) with electronic signature gates; root cause classification; action tracking; effectiveness verification | Investigates nonconformities; determines root causes; implements corrective actions; verifies effectiveness | See [SOP-004](../sops/SOP-004-capa.md) |
| **8.5.3** | Preventive Action | Provides CAPA module (same as corrective action); trend analysis to identify potential issues | Identifies potential nonconformities; implements preventive actions; verifies effectiveness | See [SOP-004](../sops/SOP-004-capa.md) |

## Key Principles

1. **PactoSigna is infrastructure, not delegation.** The platform automates workflows, enforces structure, and provides audit trails -- but the customer organization retains full responsibility for the content, decisions, and compliance of their QMS.

2. **Content belongs in git.** PactoSigna's git-native architecture means all document content is authored by the customer in their git repositories. PactoSigna syncs, validates, and presents the content -- it does not author it.

3. **Electronic signatures are the customer's accountability.** PactoSigna provides the Part 11 compliant signature mechanism, but the customer's personnel are accountable for the meaning and intent behind each signature.

4. **Regulatory compliance decisions are the customer's.** PactoSigna provides tools and data to support compliance decisions (e.g., gap detection, complaint trending, regulatory framework mappings) but does not make regulatory determinations on behalf of the customer.

## References

- ISO 13485:2016 -- Medical Devices -- Quality Management Systems -- Requirements for Regulatory Purposes
- 21 CFR Part 820 -- Quality System Regulation
- 21 CFR Part 11 -- Electronic Records; Electronic Signatures
- IEC 62304:2006+A1:2015 -- Medical Device Software -- Software Life Cycle Processes
