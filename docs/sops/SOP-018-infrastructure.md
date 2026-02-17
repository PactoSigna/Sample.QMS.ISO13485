---
id: SOP-018
title: Infrastructure and Work Environment
status: approved
author: quality@example.com
reviewers:
  - engineering
  - security
approvers:
  - quality-lead
training:
  required_departments:
    - Engineering
    - Security
  training_mode: quiz
  due_days: 30
---

# SOP-018: Infrastructure and Work Environment

## 1. Purpose

Determine, provide, and maintain the infrastructure and work environment needed to achieve conformity to product requirements.

## 2. Scope

Applies to all infrastructure and environmental conditions that affect the quality of medical device software, including:

- Development environments
- Cloud infrastructure and hosting
- Network and communication systems
- Security controls
- Backup and disaster recovery systems

## 3. Definitions

| Term | Definition |
| --- | --- |
| Infrastructure | System of facilities, equipment, and services needed for operation |
| Work Environment | Set of conditions under which work is performed, including physical and logical security |
| Disaster Recovery (DR) | Process for restoring systems after a disruption |
| Recovery Point Objective (RPO) | Maximum acceptable data loss measured in time |
| Recovery Time Objective (RTO) | Maximum acceptable downtime |

## 4. Responsibilities

- **Engineering/DevOps**: Provision, maintain, and monitor infrastructure; execute backup and DR procedures
- **Security**: Define security requirements, conduct security assessments, manage access controls
- **Quality**: Oversee infrastructure qualification, review maintenance records

## 5. Procedure

### 5.1 Infrastructure Inventory

1. Maintain an inventory of all infrastructure components
2. Inventory includes: component name, purpose, provider, configuration, owner, criticality
3. Inventory reviewed and updated quarterly

### 5.2 Infrastructure Provisioning

1. New infrastructure requests include: purpose, requirements, security considerations
2. Infrastructure provisioned per documented configurations
3. Configuration stored as code (Infrastructure as Code) where feasible
4. New infrastructure verified before production use

### 5.3 Maintenance

| Activity | Frequency | Responsible |
| --- | --- | --- |
| Operating system patching | Monthly (critical patches within 72 hours) | Engineering/DevOps |
| Dependency updates | Monthly scan, quarterly update cycle | Engineering |
| SSL/TLS certificate renewal | Before expiration (automated where possible) | Engineering/DevOps |
| Access review | Quarterly | Security |
| Capacity review | Quarterly | Engineering/DevOps |

### 5.4 Security Controls

#### Access Control

- Role-based access control (RBAC) for all systems
- Multi-factor authentication (MFA) required for production access
- Principle of least privilege applied
- Access granted via documented request and approval
- Access revoked within 24 hours of role change or departure

#### Network Security

- Production environment isolated from development
- Network traffic encrypted in transit (TLS 1.2+)
- Firewall rules documented and reviewed quarterly
- Intrusion detection/prevention monitoring

#### Data Security

- Data encrypted at rest (AES-256 or equivalent)
- Data classification applied (confidential, internal, public)
- Data handling procedures per classification level

### 5.5 Backup and Disaster Recovery

| Parameter | Production Data | Configuration |
| --- | --- | --- |
| Backup frequency | Daily (incremental), weekly (full) | With each change (version controlled) |
| Retention | 30 days | Indefinite (Git history) |
| RPO | ≤ 24 hours | ≤ 1 hour |
| RTO | ≤ 4 hours | ≤ 2 hours |

1. Backup integrity verified monthly (restore test)
2. DR plan tested annually (tabletop exercise or live failover)
3. DR test results documented and deficiencies addressed

### 5.6 Monitoring

1. Infrastructure monitoring covers: availability, performance, errors, security events
2. Alerts configured for threshold breaches
3. On-call rotation for production incident response
4. Incident response follows escalation procedures

### 5.7 Decommissioning

1. Systems identified for decommissioning reviewed for data retention obligations
2. Data migrated or archived per [SOP-005](SOP-005-control-of-records.md) retention requirements
3. System removed from inventory after decommissioning
4. Decommissioning documented

## 6. Records

- Infrastructure inventory
- Provisioning and configuration records
- Maintenance logs (patching, updates)
- Access review records
- Backup verification records
- DR test results
- Decommissioning records

## 7. References

- ISO 13485:2016 Sections 6.3, 6.4
- IEC 81001-5-1:2021 — Health software security
- [SOP-005](SOP-005-control-of-records.md) — Control of Records
- [SOP-017](SOP-017-computer-system-validation.md) — Computer System Validation
