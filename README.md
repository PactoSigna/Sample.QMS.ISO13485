# Sample.QMS.ISO13485

**ISO 13485 Quality Management System Procedures**

This repository contains a foundational Quality Management System (QMS) with Standard Operating Procedures (SOPs), work instructions, policies, audit reports, and training quizzes aligned with ISO 13485:2016 requirements.

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
├── sops/                              # Standard Operating Procedures
│   ├── SOP-001-document-control.md       # Document Control
│   ├── SOP-001-quiz.json                 # Training quiz for SOP-001
│   ├── SOP-002-design-development.md     # Design & Development
│   ├── SOP-002-quiz.json                 # Training quiz for SOP-002
│   ├── SOP-003-risk-management.md        # Risk Management
│   ├── SOP-003-quiz.json                 # Training quiz for SOP-003
│   ├── SOP-004-capa.md                   # CAPA
│   └── SOP-004-quiz.json                 # Training quiz for SOP-004
│
├── work-instructions/                 # Work Instructions
│   ├── WI-001-github-pr-review.md        # GitHub PR review workflow
│   ├── WI-002-document-approval.md       # Document approval in PactoSigna
│   └── WI-003-release-signing.md         # Release signature workflow
│
├── policies/                          # Quality Policies
│   └── POL-001-quality-policy.md         # Quality Policy statement
│
└── audits/                            # Audit Reports
    ├── AUD-2026-001.md                   # Internal Audit Report 2026
    └── audit-report.pdf                  # Source PDF
```

## Document Hierarchy

```
Quality Manual (implied)
    │
    ├── Policies (POL-xxx)
    │       │
    │       └── SOPs (SOP-xxx) ← with training quizzes (SOP-xxx-quiz.json)
    │               │
    │               └── Work Instructions (WI-xxx)
```

## ISO 13485 Clause Coverage

| Clause | Topic | Documents |
|--------|-------|-----------|
| 4.2 | Documentation Requirements | SOP-001 |
| 7.1 | Planning of Product Realization | SOP-002 |
| 7.3 | Design and Development | SOP-002, WI-001 |
| 7.5 | Production and Service Provision | WI-002, WI-003 |
| 8.2 | Monitoring and Measurement | SOP-003, AUD-2026-001 |
| 8.5 | Improvement | SOP-004 |

## Training Quizzes

Each SOP has an associated training quiz JSON file (e.g., `SOP-001-quiz.json`) used for training compliance in PactoSigna. When a document with `training_mode: quiz` is published, team members in the required departments are assigned the quiz.

**Quiz file format:** `{SOP-ID}-quiz.json` alongside the SOP markdown file.

**Question types:** `single-choice`, `multi-choice`, `true-false`

Each quiz defines a `passingScore` (percentage) and an array of `questions`. Options include an `explanation` field shown after the learner answers, reinforcing correct understanding.

## Audit Reports

The `docs/audits/` folder contains internal audit reports. Each audit document references a source PDF and links to the SOPs and work instructions that were audited. Audit reports support ISO 13485 Clause 8.2 (Internal Audits) and provide traceability to the procedures being evaluated.

## CI / Validation

This repository includes a GitHub Actions workflow at `.github/workflows/qms-validate.yml` that:

- **On pull request** (changes to `docs/`): Validates document frontmatter, structure, and traceability links using [PactoSigna/qms-actions](https://github.com/PactoSigna/qms-actions)
- **On release**: Exports the QMS documentation package

## License

This sample repository is provided under the MIT License for educational and commercial use.

---

*Built for [PactoSigna](https://pactosigna.com) - AI-native Quality Management for Medical Device Software*
