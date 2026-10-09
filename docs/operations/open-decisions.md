# Open decisions for human product-owner review

**Status:** All items below remain open; Gate 0 does not grant implementation or purchasing approval.

| Decision | Gate 0 recommendation | Evidence/approval needed |
| --- | --- | --- |
| First user outcome and MVP boundary | Start with a private first-copy collection loop using a small identified seed dataset. | Validate priorities/personas and approve acceptance criteria at Gate 1. |
| Web-first versus native-first | Provisional responsive web default; keep SwiftUI-first as a meaningful alternative. | Review user needs and camera/offline importance; compare spike results before commitment. |
| Framework and managed backend | Evaluate proposed Next.js/TypeScript/PostgreSQL/Auth/Storage defaults; no provider selected. | Approve comparative evidence, current terms, cost assumptions, export/restore and ownership-policy tests. |
| Collection structure and lifecycle | Model individual copies separately; collection grouping, deletion/archive, soft-delete, and multi-collection behavior remain undecided. | Review data model, export/deletion, retention, and recovery consequences. |
| Copy attribute vocabularies | Record region, condition, completeness/components, date, optional paid price/currency; exact vocabularies and unknown states need definition. | Product/design/collector review and validation criteria. |
| Personal photo storage and visibility | Private by default; public display requires explicit action independent of collection visibility. | Gate 2 secure upload/access/deletion, metadata, cost, and restore evidence. |
| Public collections/profile | Defer until privacy controls and public-field allow-list are approved. | Decide separate control granularity, discoverability/indexing, revocation, and abuse response. |
| Catalogue data and imagery | Use clearly labelled seed data and collector-entered details first. | Rights/terms assessment before importing, caching, attribution, or redistribution. |
| Community/generated artwork | Not required for MVP; retain separate categories, fallback policies, and moderation safeguards. | Approve cost, rights, reporting/takedown process, human review, and provider choice before launch. |
| Historical exhibit publication | Require traceable claims and editorial review; no sample exhibit is claimed. | Approve claim schema, correction process, source rights, editorial accountability, and first sourced exhibit. |
| Accessibility target and design tokens | Use accessible responsive defaults; exact formal target/component system not chosen. | Agree conformance target, manual/automated checks, and initial design system at Gate 1. |
| Subscription, affiliate, and paid services | No pricing, commercial commitment, or paid provider is approved. | Sourced unit economics, cancellation/archive policy, rights/security review, and explicit human approval. |
| Operational service levels | No hosting, backup schedule, recovery objective, or monitoring service is selected. | Gate 2 cost/restore evidence and Gate 4 approved operational runbook/targets. |

The organiser should track resulting approvals and dependencies in the issue/decision records. No decision should be inferred from this recommendation table.
