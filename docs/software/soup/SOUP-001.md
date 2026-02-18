---
id: SOUP-001
title: "SOUP Register — PactoSigna QMS"
status: approved
---

# SOUP Register

Software of Unknown Provenance (SOUP) components used in the PactoSigna QMS application, maintained per IEC 62304 and SOP-013 Section 5.10.

## SOUP Components

| # | Component | Version | Manufacturer | License | Safety Class | Purpose | Supplier |
|---|-----------|---------|-------------|---------|-------------|---------|----------|
| 1 | React | 19.x | Meta Platforms, Inc. | MIT | A | UI rendering framework | [SUP-001](../../quality/suppliers/SUP-001.md) |
| 2 | React DOM | 19.x | Meta Platforms, Inc. | MIT | A | DOM rendering for React | [SUP-001](../../quality/suppliers/SUP-001.md) |
| 3 | React Router | 7.x | Remix Software, Inc. | MIT | A | Client-side routing | — |
| 4 | Material UI (MUI) | 6.x | MUI SAS | MIT | A | UI component library | — |
| 5 | React Query | 5.x | Tanner Linsley | MIT | A | Server-state management | — |
| 6 | Firebase Auth | 11.x | Google LLC | Apache 2.0 | B | User authentication (Part 11) | [SUP-002](../../quality/suppliers/SUP-002.md) |
| 7 | Cloud Firestore SDK | 11.x | Google LLC | Apache 2.0 | B | Database access | [SUP-002](../../quality/suppliers/SUP-002.md) |
| 8 | Cloud Functions SDK | 6.x | Google LLC | Apache 2.0 | A | Serverless function runtime | [SUP-002](../../quality/suppliers/SUP-002.md) |
| 9 | Fastify | 5.x | Fastify Team | MIT | A | HTTP server framework | — |
| 10 | Zod | 3.x | Colin McDonnell | MIT | B | Schema validation | — |
| 11 | Vite | 6.x | Evan You | MIT | A | Build tooling / dev server | — |
| 12 | Acme Telemetry SDK | 2.x | Acme Analytics Corp. | Proprietary | A | Crash reporting and telemetry | [SUP-003](../../quality/suppliers/SUP-003.md) |

## Monitoring

All SOUP components are monitored for:
- Published security vulnerabilities (via Dependabot alerts)
- Version updates and breaking changes
- End-of-life or deprecation announcements

## References

- [SOP-013 Software Lifecycle](../../sops/SOP-013-software-lifecycle.md) Section 5.10
- [SOP-009 Purchasing and Suppliers](../../sops/SOP-009-purchasing-suppliers.md) Section 5.5
