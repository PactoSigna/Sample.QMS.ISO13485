---
documentId: SOP-001
title: Document Control Procedure
docType: sop
status: approved
effectiveDate: 2024-01-01
version: "1.0"
---

# SOP-001: Document Control Procedure

## 1. Purpose

This procedure defines the process for creating, reviewing, approving, distributing, and managing controlled documents within the Quality Management System (QMS). It ensures that documents are properly authorized, current versions are available at points of use, and obsolete documents are prevented from unintended use.

## 2. Scope

This procedure applies to all controlled documents within the QMS, including:

- Quality Manual
- Standard Operating Procedures (SOPs)
- Work Instructions (WIs)
- Policies
- Forms and Templates
- Technical Documentation (Design History Files, Risk Management Files)
- External documents of external origin (standards, regulations)

## 3. Definitions

| Term | Definition |
|------|------------|
| Controlled Document | A document that requires formal review and approval before use and is subject to change control |
| Document Owner | The individual responsible for the content and maintenance of a document |
| Effective Date | The date on which a document becomes active for use |
| Obsolete Document | A document that has been superseded or withdrawn from use |

## 4. Responsibilities

### 4.1 Document Owner
- Initiates document creation or revision
- Ensures technical accuracy of content
- Submits document for review and approval
- Coordinates training on document changes

### 4.2 Quality Assurance
- Maintains the document control system
- Assigns document numbers
- Verifies formatting and compliance
- Archives obsolete documents

### 4.3 Approvers
- Review documents for accuracy and completeness
- Approve documents for release
- Ensure alignment with regulatory requirements

## 5. Procedure

### 5.1 Document Creation

1. **Identify Need**: Document Owner identifies the need for a new controlled document
2. **Request Document Number**: Contact Quality Assurance to obtain a unique document identifier following the naming convention:
   - SOPs: `SOP-XXX-title`
   - Work Instructions: `WI-XXX-title`
   - Policies: `POL-XXX-title`
   - Templates: `TMPL-XXX-title`
3. **Draft Document**: Create document using the appropriate template
4. **Include Required Elements**:
   - Document ID and title
   - Version number
   - Effective date
   - Purpose
   - Scope
   - Responsibilities
   - Procedure steps
   - References

### 5.2 Document Review and Approval

1. **Submit for Review**: Document Owner submits draft via Pull Request in the document repository
2. **Technical Review**: Subject matter experts review for technical accuracy
3. **QA Review**: Quality Assurance reviews for:
   - Compliance with document format standards
   - Consistency with existing QMS documents
   - Regulatory alignment
4. **Approval**: Designated approvers provide electronic signature
5. **Release**: Upon approval, document is merged to main branch and becomes effective

### 5.3 Document Distribution

1. **Automatic Distribution**: Merged documents are automatically available in the document repository
2. **Notification**: Affected personnel are notified of new or revised documents
3. **Training**: Document Owner coordinates training if required
4. **Acknowledgment**: Personnel acknowledge receipt and understanding as needed

### 5.4 Document Revision

1. **Identify Change Need**: Any employee may identify need for document revision
2. **Submit Change Request**: Complete change request form (TMPL-001)
3. **Assess Impact**: Document Owner assesses impact of proposed changes
4. **Revise Document**: Update document content as needed
5. **Update Version**: Increment version number (major.minor)
   - Major: Significant changes affecting process flow
   - Minor: Clarifications, corrections, formatting
6. **Review and Approve**: Follow steps in Section 5.2
7. **Document Changes**: Record changes in revision history

### 5.5 Obsolete Document Control

1. **Identify Obsolescence**: Document is superseded, withdrawn, or no longer applicable
2. **Mark as Obsolete**: Add "OBSOLETE" watermark or status
3. **Remove from Active Use**: Move to archive location
4. **Retain per Schedule**: Maintain obsolete documents per retention requirements
5. **Prevent Unintended Use**: Ensure obsolete documents cannot be mistaken for current versions

### 5.6 External Documents

1. **Identify External Documents**: Standards, regulations, customer specifications
2. **Register in System**: Add to external document register with:
   - Document identifier
   - Title
   - Version/Edition
   - Source
   - Date obtained
3. **Monitor Updates**: Periodically verify documents are current
4. **Control Distribution**: Ensure only authorized copies are in use

## 6. Document Format Requirements

### 6.1 Header Information (YAML Frontmatter)
```yaml
---
documentId: [Document ID]
title: [Document Title]
docType: [sop|wi|policy|template]
status: [draft|in-review|approved|obsolete]
effectiveDate: [YYYY-MM-DD]
version: "[X.Y]"
---
```

### 6.2 Required Sections
1. Purpose
2. Scope
3. Definitions (if applicable)
4. Responsibilities
5. Procedure
6. References
7. Revision History

## 7. References

- ISO 13485:2016 Section 4.2 - Documentation Requirements
- 21 CFR Part 820.40 - Document Controls
- ISO 9001:2015 Section 7.5 - Documented Information

## 8. Revision History

| Version | Date | Author | Description |
|---------|------|--------|-------------|
| 1.0 | 2024-01-01 | Quality Manager | Initial release |

## Links

- parent_of: WI-001
- parent_of: WI-002
