# Risk and assumption register

**Status:** Initial Gate 0 register. Owners are proposed roles; no issue tracker work items have been created.

| ID | Risk / assumption | Impact | Initial response / evidence needed | Proposed owner / gate |
| --- | --- | --- | --- | --- |
| R-01 | Cross-user data or photo access through policy/configuration errors | Critical privacy breach | Threat model, owner-scoped authorization and RLS/storage negative tests before multi-user data. | Security + Architect / Gate 1–2 |
| R-02 | Catalogue/artwork provider terms do not permit required use, cache, export, or commercial display | Legal/product blocker | Compare current terms and provenance; start with clearly labelled seed data; human/legal review as needed. | Research + Content / Gate 1 |
| R-03 | Inaccurate or untraceable game-history claims damage trust | High reputational harm | Structured claims, source provenance, human editorial review, corrections/version history; GC-DATA-001 and GC-AI-001. | Content Curator / Gate 1 |
| R-04 | Private photos leak or expose location/device metadata | High privacy harm | Private storage, upload validation, metadata review, explicit sharing consent, deletion and access tests. | Security + DevOps / Gate 2 |
| R-05 | Managed platform limits, current pricing, lock-in, or recovery capability are unsuitable | Cost/continuity risk | Verify current plans/terms and data export/restore; compare self-managed alternative before commitment. | Research + Architect / Gate 2 |
| R-06 | Scope expands to catalogue, valuation, community, and mobile before core loop is validated | Delivery/quality risk | Gate-approved thin vertical slices and explicit deferrals in MVP scope. | Product Manager + Organiser / each gate |
| R-07 | PWA/browser camera/barcode capabilities vary across devices | UX/technical risk | Small cross-device spike; do not require scanner for first slice. | Architect + QA / Gate 2 |
| R-08 | Community-submitted art is unauthorized despite automated screening | Legal/moderation risk | Rights attestation, reports, limits, human review, takedowns; do not imply automated verification proves rights. | Content + Security / before public submissions |
| R-09 | Backup, restore, deletion, or cancellation policy fails collectors | Potential irreversible user-data loss | Define portability, retention, tested restore, archive/read-only cancellation behavior. | DevOps + Product / Gate 2–4 |
| R-10 | Proposed personas and success signals are unvalidated hypotheses | Product misfit | Product-owner-approved discovery; revise scope based on evidence without presenting hypotheses as research. | Product Manager / Gate 1 |

## Assumptions needing validation

- Collectors want a private web-first collection workflow before public sharing.
- A small seed catalogue and collector-entered details can prove value without comprehensive licensed data.
- Users value individual-copy records, condition/completeness, and source-backed editorial context.
- A managed relational platform can satisfy owner isolation, private media, export, backup, and an approved cost envelope.
- Responsive browser workflows meet initial device needs; camera/barcode/offline support can wait for evidence.

None has been tested in this repository. No likelihood scoring, cost figure, external legal opinion, or user research is represented as fact.
