# CLAUDE.md

Guidance for AI agents working with this ISO 13485 QMS sample repository.

## Project Overview

This is a sample Quality Management System (QMS) documentation repository for ISO 13485:2016 compliance, designed for [PactoSigna](https://pactosigna.com). It contains policies, standard operating procedures (SOPs), work instructions, training quizzes, and audit reports for medical device software companies.

## Folder and Document Type Mapping

| Folder | Document Type | ID Prefix | Example |
|--------|--------------|-----------|---------|
| `docs/policies/` | Policy | `POL-` | POL-001 |
| `docs/sops/` | Standard Operating Procedure | `SOP-` | SOP-001 |
| `docs/sops/` | Training Quiz (JSON) | `SOP-` | SOP-001-quiz.json |
| `docs/work-instructions/` | Work Instruction | `WI-` | WI-001 |
| `docs/audits/` | Audit Report | `AUD-` | AUD-2026-001 |

## Frontmatter Schema

Every markdown document requires YAML frontmatter. Required fields:

```yaml
---
id: SOP-001                    # Unique document ID matching the prefix convention
title: Document Control        # Human-readable title
status: approved               # draft | in_review | approved | obsolete
author: quality@example.com    # Author email address
reviewers:
  - engineering                # Team or role names
approvers:
  - quality-lead               # Team or role names
---
```

### Optional Training Block

Documents that require training add a `training` block to frontmatter:

```yaml
training:
  required_departments:
    - Quality
    - Engineering
  training_mode: quiz          # quiz | acknowledge | instructor_led
  due_days: 30                 # Days after publish to complete training
```

Audit reports use a simpler schema: `id`, `title`, `status`, plus `source` (filename of the source PDF in the same folder).

## Quiz JSON Format

Quiz files are named `{SOP-ID}-quiz.json` and placed alongside the corresponding SOP in `docs/sops/`.

```json
{
  "passingScore": 80,
  "questions": [
    {
      "type": "single-choice",
      "text": "Question text here?",
      "options": [
        { "text": "Option A" },
        { "text": "Option B", "correct": true, "explanation": "Why this is correct." }
      ]
    },
    {
      "type": "true-false",
      "text": "Statement to evaluate.",
      "correct": false,
      "explanation": "Why this is false."
    }
  ]
}
```

**Question types:** `single-choice` (one correct), `multi-choice` (multiple correct options marked `"correct": true`), `true-false` (boolean with `correct` at question level). The `passingScore` is a percentage (0-100). The `explanation` field is shown to learners after answering.

## Training Modes

| Mode | Behavior |
|------|----------|
| `quiz` | Learner answers randomized questions; server-side grading against `passingScore` |
| `acknowledge` | Learner reads the document and signs to confirm understanding |
| `instructor_led` | Instructor conducts training session; batch sign-off with evidence upload |

## Document Hierarchy

```
Quality Manual (implied)
    |
    +-- Policies (POL-xxx)
    |       |
    |       +-- SOPs (SOP-xxx) <-- with training quizzes (SOP-xxx-quiz.json)
    |               |
    |               +-- Work Instructions (WI-xxx)
```

Higher-tier documents govern lower-tier documents. SOPs implement policies; work instructions provide step-by-step detail for SOPs.

## Document Status Lifecycle

`draft` --> `in_review` --> `approved` --> `obsolete`

- **draft**: Initial creation, not yet submitted for review
- **in_review**: Submitted via PR, reviewers and approvers assigned
- **approved**: All approvals obtained, PR merged to main
- **obsolete**: Superseded or withdrawn, retained for audit trail

## CI Validation

The repository includes `.github/workflows/qms-validate.yml` which runs:

- **On pull request** (changes to `docs/`): Validates frontmatter schema, document structure, and traceability links via `PactoSigna/qms-actions@v1`
- **On release publish**: Exports the QMS documentation package

## Conventions

- Document IDs must be unique across the entire repository
- Use relative markdown links for cross-references between documents (e.g., `[SOP-001](../sops/SOP-001-document-control.md)`)
- One document per markdown file; filename must match the ID (e.g., `SOP-001-document-control.md` for `id: SOP-001`)
- Quiz files must be co-located with their SOP in `docs/sops/`
- Audit source PDFs must be co-located with their audit report markdown in `docs/audits/`
