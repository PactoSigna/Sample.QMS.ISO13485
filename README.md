# Sample.QMS.ISO13485

**ISO 13485 Quality Management System — Complete SaMD Coverage**

This repository contains a complete Quality Management System (QMS) covering all ISO 13485:2016 clauses applicable to Software as a Medical Device (SaMD) companies, including integration with IEC 62304, ISO 14971, and EU MDR requirements.

## Purpose

This is a **gold-standard sample repository** designed for use with [PactoSigna](https://pactosigna.com). Fork this repository to your organization and use it as a starting point for your own QMS documentation.

## How to Use

### 1. Fork This Repository

Click the "Fork" button above to copy this repository to your GitHub organization.

### 2. Connect to PactoSigna

1. Log in to PactoSigna
2. Navigate to Repositories
3. Click "Connect Repository"
4. Select your forked repository

### 3. Customize with AI

Use your preferred AI assistant to adapt this QMS for your organization. Example prompts:

**Customize SOPs:**
> "Act as a Quality Manager. Update SOP-002 Design & Development to reflect our 2-week sprint cycles and GitHub-based design reviews. Keep ISO 13485 clause references intact."

**Add work instructions:**
> "Act as a Quality Engineer. Create a new WI-004 document for 'Conducting Design Reviews in GitHub' that describes how to use PR comments for formal design review feedback."

**Generate training materials:**
> "Act as a Training Coordinator. Based on SOP-001 Document Control, create a training quiz with 10 questions to verify employee understanding of the procedure."

## Repository Structure

```
docs/
├── quality-manual/                    # Quality Manual
│   └── QM-001-quality-manual.md          # QMS scope, exclusions, process map
│
├── policies/                          # Quality Policies
│   └── POL-001-quality-policy.md         # Quality Policy statement
│
├── sops/                              # Standard Operating Procedures
│   ├── SOP-001-document-control.md       # Document Control (4.2.4)
│   ├── SOP-002-design-development.md     # Design & Development (7.3)
│   ├── SOP-003-risk-management.md        # Risk Management (7.1 / ISO 14971)
│   ├── SOP-004-capa.md                   # CAPA (8.5.2 / 8.5.3)
│   ├── SOP-005-control-of-records.md     # Control of Records (4.2.5)
│   ├── SOP-006-management-review.md      # Management Review (5.6.1)
│   ├── SOP-007-training-competence.md    # Training & Competence (6.2)
│   ├── SOP-008-internal-audit.md         # Internal Audit (8.2.4)
│   ├── SOP-009-purchasing-suppliers.md   # Purchasing & Suppliers (7.4.1)
│   ├── SOP-010-feedback-complaints.md    # Feedback & Complaints (8.2.1/8.2.2)
│   ├── SOP-011-nonconforming-product.md  # Nonconforming Product (8.3.1)
│   ├── SOP-012-regulatory-reporting.md   # Regulatory Reporting (8.2.3/8.3.3)
│   ├── SOP-013-software-lifecycle.md     # Software Lifecycle (IEC 62304)
│   ├── SOP-014-production-control.md     # Build & Deployment (7.5.1)
│   ├── SOP-015-change-control.md         # Change Control (7.3.9)
│   ├── SOP-016-data-analysis.md          # Data Analysis (8.4)
│   ├── SOP-017-computer-system-validation.md  # CSV (4.1.6)
│   ├── SOP-018-infrastructure.md         # Infrastructure (6.3/6.4)
│   ├── SOP-019-post-market-surveillance.md    # PMS (MDR Art. 83-86)
│   ├── SOP-020-preservation-labeling.md  # Preservation & Labeling (7.5.11)
│   └── SOP-xxx-quiz.json                # Training quiz for each SOP
│
├── work-instructions/                 # Work Instructions
│   ├── WI-001-github-pr-review.md        # GitHub PR review workflow
│   ├── WI-002-document-approval.md       # Document approval in PactoSigna
│   ├── WI-003-release-signing.md         # Release signature workflow
│   └── WI-xxx-quiz.json                 # Training quiz for each WI
│
└── audits/                            # Audit Reports
    ├── AUD-2026-001.md                   # Internal Audit Report 2026
    └── audit-report.pdf                  # Source PDF
```

## Document Hierarchy

```
Quality Manual (QM-001)
    │
    ├── Policies (POL-xxx)
    │
    ├── Standard Operating Procedures (SOP-xxx)
    │       with training quizzes (SOP-xxx-quiz.json)
    │
    ├── Work Instructions (WI-xxx)
    │       with training quizzes (WI-xxx-quiz.json)
    │
    └── Records & Reports (AUD-xxx)
```

## ISO 13485 Clause Coverage

| Clause | Topic | Documents |
| --- | --- | --- |
| 4.1.6 | Computer software validation | SOP-017 |
| 4.2.2 | Quality Manual | QM-001 |
| 4.2.4 | Document control | SOP-001 |
| 4.2.5 | Control of records | SOP-005 |
| 5.3 | Quality policy | POL-001 |
| 5.6 | Management review | SOP-006 |
| 6.2 | Human resources / Training | SOP-007 |
| 6.3 / 6.4 | Infrastructure / Work environment | SOP-018 |
| 7.1 | Planning of product realization | SOP-002, SOP-003 |
| 7.3 | Design and development | SOP-002, SOP-013, WI-001 |
| 7.3.9 | Design changes | SOP-015 |
| 7.4 | Purchasing | SOP-009 |
| 7.5.1 | Production and service provision | SOP-014, WI-002, WI-003 |
| 7.5.8 / 7.5.9 | Identification / Traceability | SOP-014, SOP-013 |
| 7.5.11 | Preservation of product | SOP-020 |
| 8.2.1 / 8.2.2 | Feedback / Complaint handling | SOP-010 |
| 8.2.3 | Regulatory reporting | SOP-012 |
| 8.2.4 | Internal audit | SOP-008, AUD-2026-001 |
| 8.3 | Nonconforming product | SOP-011 |
| 8.3.3 | Advisory notices | SOP-012 |
| 8.4 | Data analysis | SOP-016 |
| 8.5.2 / 8.5.3 | Corrective / Preventive action | SOP-004 |

### Clauses Excluded for SaMD

The following clauses are formally excluded in QM-001 with justification:

- **6.4.2** — Contamination control (no physical product)
- **7.5.2** — Cleanliness of product (no physical product)
- **7.5.5** — Sterile medical device requirements (software is not sterilized)
- **7.5.7** — Sterilization validation (no sterilization processes)
- **7.5.9.2** — Implantable device traceability (software is not implantable)

### Additional Standards Coverage

| Standard | Topic | Documents |
| --- | --- | --- |
| IEC 62304 | Software lifecycle | SOP-013 |
| ISO 14971 | Risk management | SOP-003 |
| IEC 81001-5-1 | Health software security | SOP-018 |
| EU MDR Art. 83-86 | Post-market surveillance | SOP-019 |
| 21 CFR Part 11 | Electronic signatures | WI-003 |
| 21 CFR Part 820 | Quality System Regulation | Multiple SOPs |

## Training Quizzes

Each SOP and work instruction has an associated training quiz JSON file used for training compliance in PactoSigna. When a document with `training_mode: quiz` is published, team members in the required departments are assigned the quiz.

**Quiz file format:** `{DOC-ID}-quiz.json` alongside the document markdown file.

**Question types:** `single-choice`, `true-false`

Each quiz defines a `passingScore` (percentage) and an array of `questions`. Options include an `explanation` field shown after the learner answers, reinforcing correct understanding.

## Audit Reports

The `docs/audits/` folder contains internal audit reports. Each audit document references a source PDF and links to the SOPs and work instructions that were audited.

## CI / Validation

This repository includes a GitHub Actions workflow at `.github/workflows/qms-validate.yml` that:

- **On pull request** (changes to `docs/`): Validates document frontmatter, structure, and traceability links using [PactoSigna/qms-actions](https://github.com/PactoSigna/qms-actions)
- **On release**: Exports the QMS documentation package

## License

This sample repository is provided under the MIT License for educational and commercial use.

---

*Built for [PactoSigna](https://pactosigna.com) — AI-native Quality Management for Medical Device Software*
