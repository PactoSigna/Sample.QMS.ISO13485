---
id: SOP-020
title: Product Preservation and Labeling
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
    - Regulatory
  training_mode: quiz
  due_days: 30
---

# SOP-020: Product Preservation and Labeling

## 1. Purpose

Preserve conformity of medical device software during processing, storage, handling, and distribution. Ensure correct and compliant labeling throughout the product lifecycle.

## 2. Scope

Applies to:

- Software build artifacts and release packages
- Distribution channels and delivery mechanisms
- Product labeling including Instructions for Use (IFU), product labels, and in-app labeling
- Archive and retention of release artifacts

## 3. Definitions

| Term | Definition |
| --- | --- |
| Release Artifact | Compiled software package ready for distribution |
| Instructions for Use (IFU) | Documentation accompanying the device that provides information for safe and effective use |
| UDI-DI | Unique Device Identification — Device Identifier |
| Digital Signature | Cryptographic signature ensuring authenticity and integrity of an artifact |

## 4. Responsibilities

- **Engineering**: Build, sign, and distribute release artifacts; maintain distribution infrastructure
- **Regulatory**: Define labeling requirements, review and approve label content
- **Quality**: Verify labeling compliance, maintain release archives

## 5. Procedure

### 5.1 Product Preservation

#### Build Artifact Integrity

1. All release artifacts include SHA-256 integrity hashes
2. Artifacts digitally signed where distribution channel supports it
3. Signature verification documented in release records

#### Secure Storage

1. Release artifacts stored in access-controlled repositories
2. Artifacts encrypted at rest
3. Access limited to authorized personnel (Engineering, DevOps)

#### Distribution Security

1. Software distributed only through authorized channels
2. Distribution channels use encrypted transport (HTTPS/TLS)
3. Download integrity verifiable by end users (published checksums)

#### Archive Retention

1. Release artifacts archived per retention schedule in [SOP-005](SOP-005-control-of-records.md)
2. Archives include: source code snapshot, compiled artifacts, build manifest, test results
3. Archives verified annually for integrity and accessibility

### 5.2 Labeling Requirements

All medical device software labeling must include:

| Element | Location | Requirement |
| --- | --- | --- |
| Product name | Product label, IFU, in-app | Legal name as registered |
| Software version | Product label, in-app (About/Settings) | Current installed version |
| UDI-DI | Product label, IFU | As assigned per UDI system |
| Manufacturer name and address | Product label, IFU | Legal entity name, registered address |
| Intended use / Intended purpose | IFU | Clear statement of intended use |
| Indications and contraindications | IFU | As determined by clinical evaluation |
| Warnings and precautions | IFU | Safety-critical information |
| Instructions for installation and use | IFU | Step-by-step user guidance |
| Technical specifications | IFU | System requirements, compatibility |
| Date of manufacture / release | Product label | Release date |
| Regulatory markings | Product label | CE mark (EU), as applicable |

### 5.3 Labeling Review and Approval

1. New labels or label changes reviewed by Regulatory and Quality
2. Review verifies compliance with applicable regulations (EU MDR Annex I Ch. III, 21 CFR 801)
3. Regulatory approves label content before use
4. Approved labels tracked with version and approval date

### 5.4 Labeling Change Control

1. Label changes follow the change control process (per [SOP-015](SOP-015-change-control.md))
2. Impact assessment includes: regulatory submission impact, translated versions affected, distribution timing
3. Updated labels deployed with the corresponding software release

### 5.5 Instructions for Use (IFU)

1. IFU content developed by Engineering with Regulatory review
2. IFU covers: intended use, user profile, installation, configuration, operation, troubleshooting, safety information
3. IFU available electronically (in-app help, downloadable PDF)
4. IFU versioned and updated with each release that affects user-facing behavior

### 5.6 Translated Labels

1. Translations required for each market language
2. Translations performed by qualified translators
3. Back-translation or review by native-speaking subject matter expert
4. Translation accuracy verified before release

## 6. Records

- Release artifact archives and integrity verification
- Labeling approval records
- IFU version history
- Translation and review records
- Distribution records

## 7. References

- ISO 13485:2016 Sections 7.5.1, 7.5.11
- EU MDR 2017/745 Annex I, Chapter III, Section 23
- 21 CFR 801 — Labeling
- 21 CFR 820.120 — Device labeling
- [SOP-005](SOP-005-control-of-records.md) — Control of Records
- [SOP-014](SOP-014-production-control.md) — Production Control
- [SOP-015](SOP-015-change-control.md) — Change Control
