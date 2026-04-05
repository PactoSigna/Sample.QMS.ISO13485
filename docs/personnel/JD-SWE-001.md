---
id: JD-SWE-001
title: Software Engineer
type: job_description
version: '1.0'
status: approved
department: Engineering
department_role: member
author: '[Organization Name] Quality Team'
reviewers:
  - Quality
approvers:
  - Executive
effective_date: '2026-01-15'
---

# Software Engineer

## Purpose

The Software Engineer develops and maintains [Organization Name] software products under the IEC 62304 software lifecycle. This role is responsible for translating software requirements into working, tested, and documented code that meets the quality and safety standards required by the applicable device classification and regulatory requirements.

## Responsibilities

- Implement features according to Software Requirements Specifications (SRS), following the architecture defined in the Software Architecture (HLD) and Detailed Design (SDD) documents.
- Author unit, integration, and system tests for all new functionality, maintaining test coverage thresholds defined in the Software Test Plan.
- Participate in code reviews, providing constructive feedback on design, correctness, and compliance with coding standards.
- Contribute to design documentation (SDD sections) for modules and components they own.
- Evaluate SOUP (Software of Unknown Provenance) components for suitability, documenting risk assessments and license compatibility in the SOUP register.
- Investigate and resolve software anomalies, documenting root causes and fixes through the anomaly management process.
- Author and maintain technical documentation, including API specifications, deployment guides, and configuration references.
- Follow change control procedures for all software modifications, ensuring traceability from requirements through implementation and testing.
- Maintain awareness of safety class implications when implementing features that affect device safety or regulatory compliance.

## Qualifications

- Bachelor's degree in Computer Science, Software Engineering, or equivalent practical experience.
- Minimum 3 years of professional software development experience.
- Proficiency in the programming languages and frameworks used by [Organization Name] products.
- Experience with version control systems (Git) and collaborative development workflows.
- Understanding of software testing methodologies (unit, integration, system, regression).
- Familiarity with regulated software development practices preferred.
- Experience with CI/CD pipelines and automated build systems.
- Strong written communication skills for technical documentation.

## Authorities

- Merge approved pull requests after all review comments are resolved and CI checks pass. Direct commits to protected branches are prohibited.
- Create and update technical design documents (SDD contributions) for owned modules.
- Flag technical risks and design concerns during design reviews and planning meetings.
- Propose SOUP component additions or upgrades for architectural review.
- Report software anomalies and initiate investigations.
- Reject code changes during review that do not meet coding standards or introduce unmitigated risks.

## Reporting Structure

- **Reports to**: Engineering Lead or Software Architect.
- **Key collaborators**: [Quality Manager](./JD-QM-001.md) (document reviews, training completion, CAPA support), other Software Engineers (code review, pair programming), [Regulatory Affairs Specialist](./JD-RA-001.md) (compliance questions, labeling review).

## Training Requirements

- IEC 62304 software lifecycle processes (initial + biennial refresher).
- Secure coding practices (OWASP Top 10, input validation, authentication and authorization patterns).
- Version control and document management procedures per [SOP-DOC-001](../sops/SOP-DOC-001.md).
- Software change control and anomaly management procedures.
- ISO 14971 risk management awareness (software contribution to risk).
- FDA 21 CFR Part 11 awareness (electronic records and signatures relevant to product software).
- SOUP evaluation and management procedures.
- Annual cybersecurity awareness training.
