---
id: SOP-007
title: Training and Competence
status: approved
author: quality
reviewers:
  - engineering
  - quality
  - management
approvers:
  - quality
training:
  required_departments:
    - Quality
    - Engineering
    - Management
  training_mode: quiz
  due_days: 30
---

# SOP-007: Training and Competence

> **Document Type**: Standard Operating Procedure
> **Regulatory Basis**: ISO 13485:2016 Section 6.2
> **Status**: Effective
> **Last Updated**: 2026-04-05
> **Owner**: PactoSigna Quality
> **Review Cycle**: Annual

## 1. Purpose

This procedure establishes the requirements for ensuring all personnel performing work affecting product quality are competent on the basis of appropriate education, training, skills, and experience. It defines how PactoSigna's Training module automates training assignment, tracks completion, and provides a competency dashboard for compliance monitoring.

## 2. Scope

This SOP applies to all personnel (employees, contractors, consultants) who perform activities within the QMS scope, including:

- Design and development
- Software testing and verification
- Quality assurance and regulatory affairs
- Risk management
- Document control
- Customer support and complaint handling
- Management and supervision

This SOP does not cover general corporate training unrelated to product quality (e.g., HR onboarding, benefits enrollment).

## 3. Definitions

| Term | Definition |
| --- | --- |
| **Competency** | Demonstrated ability to apply knowledge and skills to achieve intended results |
| **Training Task** | A PactoSigna record representing a specific training assignment for a member, with lifecycle states: `assigned` -> `in_progress` -> `completed` / `overdue` |
| **Training Mode** | The method by which training is delivered and verified: `quiz` (knowledge assessment) or `acknowledgment` (read-and-confirm) |
| **Passing Threshold** | The minimum quiz score required to demonstrate competency (default: 80%) |
| **Department** | An organizational unit defined in PactoSigna, used for scoping training assignments to relevant personnel |
| **Job Description** | A controlled document type linking to department and role-specific competency requirements |
| **Competency View** | PactoSigna's derived dashboard showing department -> job descriptions -> training status -> gaps |

## 4. Roles and Responsibilities

| Role | Responsibilities |
| --- | --- |
| **Quality** | Administers the training program; configures training parameters in document frontmatter; monitors compliance dashboard; escalates overdue training |
| **Department Heads** | Defines competency requirements for roles via job description documents; identifies training needs for their personnel; ensures personnel complete assigned training |
| **All Personnel** | Completes assigned training tasks within due dates; applies learned skills in daily work |
| **PactoSigna Administrator** | Configures departments and member assignments in the platform; manages training module settings |

## 5. Procedure

### 5.1 Competency Requirements

1. Each role shall have defined competency requirements documented in a job description document (`job_description` type) with frontmatter linking to the department and optional department role.
2. Competency areas shall be mapped to specific SOPs, work instructions, and policies that personnel must complete.
3. PactoSigna's Competency View provides a derived dashboard showing:
   - Departments and their job descriptions
   - Required training per role
   - Completion status per individual
   - Identified competency gaps

### 5.2 Training Needs Identification

Training needs are identified through the following triggers:

| Trigger | Action |
| --- | --- |
| New hire onboarding | Department head assigns initial training based on job description competency requirements |
| Role change or promotion | Department head identifies additional training for the new role |
| New or updated SOP/WI | PactoSigna automatically assigns training when a release is published (see Section 5.4) |
| CAPA findings | Quality assigns targeted training to address identified knowledge gaps |
| Audit findings | Quality assigns training to address audit nonconformances |
| Annual competency review | Department heads review and update competency requirements |
| New regulatory requirements | Regulatory identifies training needs for new compliance obligations |

### 5.3 Training Delivery Methods

| Method | Configuration | Verification | When to Use |
| --- | --- | --- | --- |
| **Quiz-based** | `training_mode: quiz` in frontmatter | Member must pass quiz with score >= passing threshold (default 80%) | SOPs and procedures with testable knowledge |
| **Acknowledgment** | `training_mode: acknowledgment` in frontmatter | Member confirms they have read and understood the document | Policies, informational documents, simple updates |
| **Instructor-led** | Tracked externally; record uploaded to PactoSigna | Instructor sign-off documented | Hands-on skills, complex procedures |
| **On-the-job** | Tracked externally; record uploaded to PactoSigna | Supervisor verification documented | Practical skills application |

### 5.4 Automatic Training Assignment

1. Documents with a `training` frontmatter block specify training parameters:
   - `required_departments`: List of departments whose members must complete training
   - `training_mode`: Either `quiz` or `acknowledgment`
   - `due_days`: Number of days from assignment to due date
2. When a PactoSigna Release is published, the **training assignment worker** (Cloud Tasks) automatically:
   - Identifies all documents in the release that have `training` frontmatter
   - Creates training tasks for all members in the specified `required_departments`
   - Sets due dates based on the `due_days` parameter
3. Each training task enters the `assigned` state and appears on the member's training dashboard.
4. PactoSigna's audit trail records the assignment event with the release ID and document references.

### 5.5 Training Task Lifecycle

| State | Description | Transition |
| --- | --- | --- |
| `assigned` | Task created; member notified | Member opens the training task |
| `in_progress` | Member has started the training (quiz or acknowledgment) | Member completes the assessment |
| `completed` | Member has successfully completed the training | Terminal state; Part 11 electronic signature recorded |
| `overdue` | Due date has passed without completion | PactoSigna's overdue notification worker (daily CRON) flags and notifies |

### 5.6 Quiz-Based Assessment

1. Each SOP or procedure with `training_mode: quiz` shall have an accompanying quiz file (e.g., `SOP-001-quiz.json`).
2. Quiz questions shall test:
   - Understanding of the procedure's purpose and scope
   - Knowledge of key steps and responsibilities
   - Awareness of PactoSigna platform features that support the procedure
   - Regulatory requirements relevant to the procedure
3. The passing threshold is configurable (default 80%). Quiz definitions and correct answers are stored server-side to prevent client-side tampering (Part 11 compliance).
4. Upon passing, PactoSigna records a Part 11-compliant electronic signature confirming training completion.
5. Failed attempts are recorded in the audit trail. Members may re-attempt after reviewing the material.

### 5.7 New Employee Onboarding

New employees shall complete the following within 30 days of start date:

1. Quality Policy acknowledgment ([POL-001](../policies/POL-001-quality-policy.md))
2. Document Control training ([SOP-001](SOP-001-document-control.md))
3. Role-specific SOP training as identified by the department head based on job description competency requirements
4. Any additional training required by the most recent release

### 5.8 Overdue Training Management

1. PactoSigna's **overdue notification worker** runs daily (Cloud Scheduler CRON) and:
   - Identifies training tasks past their due date
   - Sends notifications to the assigned member and their department head
   - Updates the training task status to `overdue`
2. Overdue training shall be escalated through the following path:
   - Day 1 overdue: Notification to member
   - Day 7 overdue: Notification to department head
   - Day 14 overdue: Escalation to Quality Management Representative
3. Persistent overdue training (more than 30 days) shall be reported in the management review per [SOP-006](SOP-006-management-review.md).

### 5.9 Training Effectiveness Evaluation

Training effectiveness shall be evaluated through:

- Quiz scores and first-attempt pass rates
- Completion rates by department and document
- Reduction in errors or nonconformances related to trained areas
- Annual competency review by department heads
- CAPA recurrence analysis (repeat issues in trained areas indicate ineffective training)

### 5.10 Training Records

PactoSigna maintains the following training records:

| Record | Storage | Retention |
| --- | --- | --- |
| Training task assignment | PactoSigna Training module | Lifetime of organization |
| Quiz attempt results (score, timestamp, answers) | PactoSigna Training module (server-side) | Lifetime of organization |
| Completion electronic signatures | PactoSigna Signatures collection | Lifetime of organization |
| Overdue notifications | PactoSigna Notifications collection | Per retention policy |
| Competency review records | Job description documents | Per document retention policy |

## 6. PactoSigna Platform Implementation

| Training Requirement | PactoSigna Feature |
| --- | --- |
| Training assignment | Automatic assignment via training assignment worker when releases are published |
| Department scoping | Training scoped to `required_departments` defined in document frontmatter |
| Quiz assessment | Server-side quiz engine with configurable passing threshold (default 80%) |
| Acknowledgment tracking | Read-and-confirm mode with electronic signature |
| Completion records | Part 11-compliant electronic signatures on training completion |
| Overdue monitoring | Daily CRON worker sends notifications for overdue tasks |
| Compliance dashboard | Training module shows completion status per department, per document |
| Competency view | Derived dashboard: department -> job descriptions -> training -> gaps |
| Task lifecycle | State machine: `assigned` -> `in_progress` -> `completed` / `overdue` |
| Audit trail | All training events (assignment, attempts, completion, overdue) logged immutably |

## 7. Related Documents

- [SOP-001](SOP-001-document-control.md) -- Document Control
- [SOP-006](SOP-006-management-review.md) -- Management Review
- [POL-001](../policies/POL-001-quality-policy.md) -- Quality Policy

## 8. References

| Reference | Description |
| --- | --- |
| ISO 13485:2016 Section 6.2 | Human resources -- competence, training, and awareness |
| 21 CFR Part 820.25 | Personnel |
| 21 CFR Part 11 | Electronic records; electronic signatures (training completion records) |

## 9. Revision History

| Version | Date | Author | Description |
| --- | --- | --- | --- |
| 1.0 | 2026-01-15 | PactoSigna Quality | Initial release |
| 2.0 | 2026-04-05 | PactoSigna Quality | Rewritten with PactoSigna platform integration -- automatic training assignment, quiz engine, overdue worker, competency view, Part 11 signatures |
