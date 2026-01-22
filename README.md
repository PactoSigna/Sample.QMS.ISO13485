# Sample.QMS.ISO13485

**ISO 13485 Quality Management System Procedures**

This repository contains a foundational Quality Management System (QMS) structure with Standard Operating Procedures (SOPs), work instructions, and templates aligned with ISO 13485:2016 requirements.

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
├── sops/                           # Standard Operating Procedures
│   ├── SOP-001-document-control.md    # Document Control procedure
│   ├── SOP-002-design-development.md  # Design & Development
│   ├── SOP-003-risk-management.md     # Risk Management
│   └── SOP-004-capa.md                # CAPA procedure
│
├── work-instructions/              # Work Instructions
│   ├── WI-001-github-pr-review.md     # GitHub PR review workflow
│   ├── WI-002-document-approval.md    # Document approval in PactoSigna
│   └── WI-003-release-signing.md      # Release signature workflow
│
├── policies/                       # Quality Policies
│   └── POL-001-quality-policy.md      # Quality Policy statement
│
└── templates/                      # Document Templates
    ├── TMPL-001-change-request.md     # Change Request form
    └── TMPL-002-training-log.md       # Training log template
```

## ISO 13485 Clause Coverage

| Clause | Topic | Documents |
|--------|-------|-----------|
| 4.2 | Documentation Requirements | SOP-001 |
| 7.1 | Planning of Product Realization | SOP-002 |
| 7.3 | Design and Development | SOP-002, WI-001 |
| 7.5 | Production and Service Provision | WI-002, WI-003 |
| 8.2 | Monitoring and Measurement | SOP-003 |
| 8.5 | Improvement | SOP-004 |

## Document Status

| Document | Status | Description |
|----------|--------|-------------|
| SOP-001, WI-001 | Complete | Fully written examples |
| All others | Skeleton | Template structure for you to complete |

## Document Hierarchy

```
Quality Manual (implied)
    │
    ├── Policies (POL-xxx)
    │       │
    │       └── SOPs (SOP-xxx)
    │               │
    │               └── Work Instructions (WI-xxx)
    │                       │
    │                       └── Templates (TMPL-xxx)
```

## License

This sample repository is provided under the MIT License for educational and commercial use.

---

*Built for [PactoSigna](https://pactosigna.com) - AI-native Quality Management for Medical Device Software*
