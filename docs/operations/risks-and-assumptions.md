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

## Mitigation and acceptance evidence linkage

| Risk | Proposed work-item evidence |
| --- | --- |
| R-01 | GC-I-002 threat/access design; GC-I-005 isolation spike; GC-I-021 independent regression evidence; GC-I-035 release security review. |
| R-02 | GC-I-003 policy/rights review; GC-I-007 permitted seed search; GC-I-037 future provider comparison. |
| R-03 | GC-I-003 evidence rules; GC-I-025 structured claim/editorial model; GC-I-026 sourced publication and corrections. |
| R-04 | GC-I-006 private upload/metadata evidence; GC-I-023 lifecycle; GC-I-029–GC-I-030 separate photo consent and revocation when sharing is selected. |
| R-05 | GC-I-009 current provider/cost/recovery comparison; GC-I-010 go/no-go; GC-I-034 operational validation. |
| R-06 | GC-I-001 scope approval; GC-I-022/028/033 slice review; GC-I-035 declared release scope; GC-I-037–GC-I-044 remain investigations. |
| R-07 | GC-I-008 device spike; GC-I-039 future native/offline/barcode investigation; manual input remains the proposed core path. |
| R-08 | GC-I-003 policy; GC-I-031 attestations and restricted submissions; GC-I-032 reporting/moderation/takedown; GC-I-033 enablement review. |
| R-09 | GC-I-020 export; GC-I-027 deletion/retention; GC-I-034 restore/suppression; GC-I-040 future cancellation/essential-record access research. |
| R-10 | GC-I-001 outcome/discovery review; GC-I-004 UX contract; GC-I-008 prototype evidence. No persona is reported as validated. |

Issue closure requires evidence, not removal of a risk label. The organiser records residual exposure and the responsible human's acceptance at the relevant gate. A rights dispute, untested owner boundary, or unresolved production deletion/recovery policy blocks the affected release.
