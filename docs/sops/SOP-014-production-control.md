---
id: SOP-014
title: Production Control (Build and Deployment)
status: approved
author: quality@example.com
reviewers:
  - engineering
approvers:
  - quality-lead
training:
  required_departments:
    - Engineering
    - Quality
  training_mode: quiz
  due_days: 30
---

# SOP-014: Production Control (Build and Deployment)

## 1. Purpose

Control production and service provision processes for medical device software, ensuring reproducible builds, controlled deployments, and proper product identification.

## 2. Scope

Applies to the build, deployment, distribution, and identification of all medical device software products.

## 3. Definitions

| Term | Definition |
| --- | --- |
| Build | The process of compiling source code and dependencies into a deployable artifact |
| Deployment | The process of installing a software release into a target environment |
| Release Artifact | The output of a build process intended for deployment (e.g., compiled application, container image) |
| UDI-DI | Unique Device Identification — Device Identifier, a unique code assigned to a device model |

## 4. Responsibilities

- **Engineering**: Maintain build and deployment pipelines, execute deployments, verify build integrity
- **Quality**: Define release criteria, approve deployments, verify product identification
- **DevOps/Infrastructure**: Maintain build and deployment infrastructure

## 5. Procedure

### 5.1 Build Process

1. Builds are automated via continuous integration (CI) pipeline
2. Build environment is defined and version-controlled (dependencies, tool versions, OS)
3. Builds are reproducible: same source code + same environment = same output
4. Build outputs include:
   - Compiled application artifacts
   - Build manifest (source commit, dependency versions, build timestamp)
   - Integrity hash (SHA-256) of all artifacts

### 5.2 Build Verification

1. Automated test suite executes on every build:
   - Unit tests
   - Integration tests
   - Static analysis
   - Dependency vulnerability scan
2. Build is rejected if any verification step fails
3. Build verification results are recorded and associated with the build identifier

### 5.3 Product Identification

Every release is identified by:

| Element | Format | Example |
| --- | --- | --- |
| Product name | As registered | CardioSense |
| Version number | Semantic versioning (MAJOR.MINOR.PATCH) | 2.1.0 |
| Build identifier | Commit SHA (short) | abc1234 |
| Build timestamp | ISO 8601 | 2026-01-15T14:30:00Z |
| Integrity hash | SHA-256 of release artifact | sha256:e3b0c44... |
| UDI-DI | Per UDI system requirements | (assigned per device registration) |

### 5.4 Deployment Process

#### Pre-deployment

1. Release criteria verified (per [SOP-013](SOP-013-software-lifecycle.md) Section 5.9)
2. Deployment checklist completed:
   - All required signatures collected
   - Release notes prepared
   - Known anomalies documented
   - Rollback plan documented
3. Quality approves deployment

#### Deployment Execution

1. Deploy to staging environment first
2. Execute smoke tests in staging
3. Promote to production upon successful staging verification
4. Verify production deployment (health checks, smoke tests)

#### Post-deployment

1. Monitor production metrics (error rates, performance, availability)
2. Document deployment record (version, timestamp, deployer, verification results)
3. Archive release artifacts

### 5.5 Rollback

If critical issues are discovered post-deployment:

1. Assess severity and scope of impact
2. Execute rollback to previous known-good version
3. Document rollback (reason, timing, affected users)
4. Create nonconformance report per [SOP-011](SOP-011-nonconforming-product.md)

### 5.6 Production Monitoring

Ongoing monitoring includes:

- Application availability and uptime
- Error rates and error types
- Response time and performance metrics
- Security events and anomalies
- Automated alerting for threshold breaches

## 6. Records

- Build manifests and verification results
- Deployment records and checklists
- Release artifact archives
- Production monitoring reports
- Rollback records

## 7. References

- ISO 13485:2016 Sections 7.5.1, 7.5.6, 7.5.8
- IEC 62304 Sections 5.8, 8
- 21 CFR 820.70, 820.120
- [SOP-013](SOP-013-software-lifecycle.md) — Software Lifecycle
- [SOP-011](SOP-011-nonconforming-product.md) — Nonconforming Product
