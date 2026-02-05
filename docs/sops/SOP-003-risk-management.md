---
id: SOP-003
title: Risk Management
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
    - Regulatory
  training_mode: quiz
  due_days: 30
---

# SOP-003: Risk Management

## Purpose

Define the risk management process for medical device software per ISO 14971:2019.

## Scope

Applies to all identified hazards and risks throughout the product lifecycle.

## Responsibilities

- **Risk Manager**: Coordinates risk management activities
- **Engineering**: Identifies hazards and implements controls
- **Quality**: Reviews risk acceptability

## Procedure

### 1. Hazard Identification

1. Analyze each software requirement for potential failures
2. Create hazard documents (HAZ-XX-XXX) in appropriate category:
   - Software hazards: `risk/software/HAZ-SW-XXX.md`
   - Usability hazards: `risk/usability/HAZ-US-XXX.md`
   - Security hazards: `risk/security/HAZ-SEC-XXX.md`
3. Link hazard to analyzed item using `analyzes:` in frontmatter

### 2. Hazard Analysis

For each hazard, document:

- Failure mode and cause
- Detection method
- Hazardous situations (`**Leads to:**` links to HS-XXX)

### 3. Risk Estimation

1. Create hazardous situation documents (HS-XXX) with probability
2. Create harm documents (HARM-XXX) with severity
3. Calculate risk = severity x probability

### 4. Risk Evaluation

1. Create risk analysis documents (RISK-XX-XXX)
2. Link to hazard, situation, and harm
3. Determine if inherent risk is acceptable

### 5. Risk Control

For unacceptable risks:

1. Identify control measures (requirements that mitigate)
2. Document controls in risk analysis with heading format:
   `### [SRS-XXX](path) - Control Name`
3. Specify what the control reduces: `sequence_probability`, `harm_probability`, or `severity`

### 6. Residual Risk

1. Re-estimate probability after controls
2. Document residual risk assessment
3. If still unacceptable, provide risk-benefit analysis

## Risk Document Structure

```
docs/risk/
├── software/       # HAZ-SW-*, RISK-SW-*
├── usability/      # HAZ-US-*, RISK-US-*
├── security/       # HAZ-SEC-*, RISK-SEC-*
├── situations/     # HS-*
└── harms/          # HARM-*
```

## Related Documents

- [SOP-002](SOP-002-design-development.md) - Design and Development

## References

- ISO 14971:2019
- IEC 62304:2006+A1:2015 Section 7
