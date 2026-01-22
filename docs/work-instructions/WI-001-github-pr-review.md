---
documentId: WI-001
title: GitHub Pull Request Review Workflow
docType: work-instruction
status: approved
effectiveDate: 2024-01-01
version: "1.0"
---

# WI-001: GitHub Pull Request Review Workflow

## 1. Purpose

This work instruction provides step-by-step guidance for conducting document reviews using GitHub Pull Requests. It implements the review requirements defined in SOP-001 Document Control Procedure.

## 2. Scope

This instruction applies to all controlled documents managed in GitHub repositories, including:

- Quality Management System documents
- Design History File documents
- Risk Management File documents
- Technical specifications

## 3. Prerequisites

Before performing this procedure, ensure:

- [ ] You have a GitHub account with access to the document repository
- [ ] You are assigned as a reviewer on the Pull Request
- [ ] You have appropriate training on this work instruction
- [ ] You understand the document subject matter (for technical review)

## 4. Procedure

### 4.1 Accessing the Pull Request

1. Open your web browser and navigate to the repository
2. Click the **Pull requests** tab
3. Locate the PR requiring your review (you may filter by "Review requested")
4. Click on the PR title to open it

### 4.2 Understanding the Change

1. Read the **PR description** to understand:
   - What document is being changed
   - Why the change is being made
   - Any specific areas requiring attention

2. Review the **Commits** tab to see the change history

3. Check the **linked issues** (if any) for additional context

### 4.3 Reviewing the Changes

1. Click the **Files changed** tab

2. Review each file systematically:

   **For Document Content:**
   - [ ] Content is technically accurate
   - [ ] Language is clear and unambiguous
   - [ ] Procedure steps are complete and logical
   - [ ] References are correct and current

   **For Document Format:**
   - [ ] YAML frontmatter is complete and correct
   - [ ] Document ID follows naming convention
   - [ ] Version number is appropriately incremented
   - [ ] Required sections are present
   - [ ] Links to related documents are valid

3. To add a comment on a specific line:
   - Hover over the line number
   - Click the **+** button that appears
   - Type your comment
   - Click **Add single comment** or **Start a review**

4. Use these comment conventions:
   - `[REQUIRED]` - Must be addressed before approval
   - `[SUGGESTION]` - Optional improvement
   - `[QUESTION]` - Clarification needed
   - `[NIT]` - Minor/stylistic (non-blocking)

### 4.4 Submitting Your Review

1. After reviewing all changes, click **Review changes** (green button)

2. Write a summary of your review:
   - Overall assessment
   - Key concerns (if any)
   - Acknowledgment of what was done well

3. Select your review decision:

   | Decision | When to Use |
   |----------|-------------|
   | **Approve** | All required items addressed, document ready for release |
   | **Request changes** | Required items must be addressed before approval |
   | **Comment** | Providing feedback without explicit approval/rejection |

4. Click **Submit review**

### 4.5 Following Up on Review Comments

**If you are the Document Owner:**

1. Address each comment:
   - Make requested changes in new commits
   - Reply to comments explaining your changes
   - Mark conversations as resolved when addressed

2. Request re-review if changes were requested

**If you are the Reviewer:**

1. Review responses to your comments
2. Verify changes address your concerns
3. Resolve conversations or provide additional feedback
4. Update your review decision as appropriate

### 4.6 Final Approval and Merge

1. **Required Approvals**: Ensure minimum required approvals are obtained:
   - Technical reviewer (subject matter expert)
   - Quality reviewer (QA representative)

2. **Approval Signatures**: Each approval in GitHub serves as an electronic signature per 21 CFR Part 11 requirements when:
   - Reviewer is authenticated (logged in)
   - Approval is timestamped
   - Approval cannot be modified after submission

3. **Merge the PR**:
   - Only designated personnel may merge
   - Use "Squash and merge" for clean history
   - Delete the feature branch after merge

4. **Post-Merge**:
   - Verify document appears correctly in main branch
   - Notify affected personnel of the change
   - Update training records if required

## 5. Troubleshooting

| Issue | Resolution |
|-------|------------|
| Cannot see Files changed | Check repository access permissions |
| Cannot submit review | Verify you are assigned as reviewer |
| Merge button disabled | Required approvals not yet obtained |
| Conflicts reported | Contact Document Owner to resolve |

## 6. Records

The following records are automatically maintained by GitHub:

- Review comments and responses
- Approval decisions with timestamps
- User identity (authenticated)
- Complete audit trail of all changes

## 7. References

- SOP-001: Document Control Procedure
- GitHub Documentation: About Pull Request Reviews
- 21 CFR Part 11: Electronic Records; Electronic Signatures

## 8. Revision History

| Version | Date | Author | Description |
|---------|------|--------|-------------|
| 1.0 | 2024-01-01 | Quality Engineer | Initial release |

## Links

- child_of: SOP-001
