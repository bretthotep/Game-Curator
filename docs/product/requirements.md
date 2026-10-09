# Requirements outline

**Status:** Initial Gate 0 outline; requirements and priorities require product-owner approval.

## User outcomes

- **R1 — Record ownership:** A collector can catalogue actual physical copies and distinguish them from catalogue game/release data.
- **R2 — Describe a copy:** A collector can record release/edition, region, condition, completeness/components, acquisition date, optional price paid/currency, notes, and ownership status.
- **R3 — Find and present:** A collector can search, filter, sort, and view an accessible, responsive collection with useful statistics.
- **R4 — Preserve personal context:** A collector can add private photographs of their own items and retain/export their collection records.
- **R5 — Explore context:** A visitor can read structured historical exhibits with source traceability, timelines, uncertainty, and corrections.
- **R6 — Share by choice:** A collector can make a collection public only through explicit, understandable action; private price/acquisition details and photos need their own clear visibility rules.
- **R7 — Contribute safely (future):** Community artwork and corrections have rights attestations, moderation, reporting, review, and takedown processes before public distribution.

## Functional requirements (candidate)

| ID | Requirement | Outcome(s) | Acceptance reference(s) | Proposed disposition |
| --- | --- | --- | --- | --- |
| F-01 | Account creation/authentication and session handling | R1 | AC-05, AC-06 | First slice; required before multi-user persistence |
| F-02 | Useful empty collection state and add-copy entry point | R1 | AC-06 | First slice |
| F-03 | Search/select from a small, clearly identified seed catalogue or controlled dataset | R1 | AC-04, AC-08 | First slice |
| F-04 | Create, read, edit, and remove/mark ownership status for multiple physical copies | R1 | AC-01, AC-02, AC-05 | First slice; deletion policy needs review |
| F-05 | Capture edition, region, condition, completeness/components, date, optional paid price/currency, notes | R2 | AC-03 | First slice; exact vocabularies for Gate 1 |
| F-06 | Upload personal photos to private storage with validation | R4 | AC-10 | Candidate follow-on slice, subject to Gate 2 security/operations spike |
| F-07 | Responsive art-forward collection cards and a game detail view distinct from copy details | R3 | AC-01, AC-06 | First slice |
| F-08 | Search, filters, sorting, and basic counts | R3 | AC-08, AC-14 | Search in first slice; filters/statistics may follow |
| F-09 | Sample structured historical exhibit with citations, references, timeline, and correction path | R5 | AC-11 | Separate editorial slice after provenance workflow |
| F-10 | Accessible loading, empty, error, and permission-denied states | R1, R3 | AC-06 | Required for all implemented journeys |
| F-11 | Automated checks and reproducible CI | R1–R7 | AC-07 | Required before implementation completion |
| F-12 | Public collector profile / public collection sharing | R6 | AC-12 | Deferred until privacy model and explicit-consent design are approved |
| F-13 | Export a collector's collection records in a documented, portable format | R4 | AC-09 | First slice; format and included fields require Gate 1 review |
| F-14 | Community artwork and correction submissions with rights attestation, moderation, reporting, and takedown | R7 | AC-13 | Deferred until rights and moderation processes are approved |

## Outcome coverage and disposition

| Outcome | Linked requirements | Acceptance references | Proposed coverage/disposition |
| --- | --- | --- | --- |
| R1 — Record ownership | F-01–F-04, F-10, F-11 | AC-01, AC-02, AC-04–AC-08 | Covered by the proposed first slice. |
| R2 — Describe a copy | F-05 | AC-03 | Covered by the proposed first slice. |
| R3 — Find and present | F-07, F-08, F-10 | AC-06, AC-08, AC-14 | Responsive presentation and seed-catalogue search are first slice; filters/statistics may follow. |
| R4 — Preserve personal context | F-06, F-13 | AC-09, AC-10 | Record export is in the proposed first slice; private photos are a candidate follow-on slice. |
| R5 — Explore context | F-09 | AC-11 | Separate editorial slice; depends on sourced-content and correction workflows. |
| R6 — Share by choice | F-12 | AC-12 | Deferred pending privacy and explicit-consent approval. |
| R7 — Contribute safely (future) | F-14 | AC-13 | Deferred pending rights, moderation, reporting, and takedown processes. |

No R1–R7 outcome is left unmapped. Follow-on and deferred outcomes are proposals, not first-slice commitments.

## Acceptance criteria references

These are proposed acceptance criteria; exact implementation details and evidence are subject to Gate 1 review.

| Reference | Acceptance criterion | Proposed scope |
| --- | --- | --- |
| AC-01 | A collector can distinguish catalogue title/release information from each individually owned physical copy. | First slice |
| AC-02 | Multiple copies of one release can be recorded independently. | First slice |
| AC-03 | Optional price paid is stored as a transaction detail and is never presented as market value. | First slice |
| AC-04 | Seed data is labelled as sample data, and missing catalogue details are not invented. | First slice |
| AC-05 | A collection is private by default; a second user is denied read and write access. | First slice |
| AC-06 | Core add/view/edit paths work with keyboard and a narrow viewport; loading, empty, error, and permission-denied states are understandable. | First slice |
| AC-07 | Automated tests cover domain rules and the access boundary, and CI results are recorded. | Required delivery foundation |
| AC-08 | A collector can search the labelled seed catalogue and select a game/release for a copy. | First slice |
| AC-09 | A collector can export their own collection records in a documented portable format; the export excludes other users' private records. | First slice; format and included fields need Gate 1 review |
| AC-10 | Personal-photo upload validates files and keeps each photo private to its owner unless a separately approved visibility action is implemented. | Candidate follow-on slice; requires security/operations evidence |
| AC-11 | A sample exhibit presents traceable sources, a timeline, uncertainty where applicable, and a correction path. | Separate editorial slice |
| AC-12 | Sharing requires explicit action with understandable visibility controls; private price/acquisition details and photos follow separately approved visibility rules. | Deferred |
| AC-13 | Community submissions have rights attestation, moderation, reporting, and a takedown path before public distribution. | Deferred |
| AC-14 | Any follow-on filters, sorting, or statistics are accessible and do not frame monetary value as the primary achievement measure. | Follow-on |

## Non-functional requirements

- **Accessibility:** Semantic, keyboard-operable UI; visible focus; sufficient contrast; responsive text/layout; reduced-motion support; accessible errors. Define a target and evaluation approach at Gate 1.
- **Privacy/security:** Least privilege, private-by-default records/media, tested cross-user denial, validated uploads, controlled secrets, deletion/export plan, abuse prevention for public features.
- **Data integrity:** Preserve distinctions between game, platform, release, copy, price paid, and valuation. Represent incomplete/uncertain catalogue facts honestly; use migrations and documented constraints.
- **Maintainability:** Strict TypeScript if selected, explicit domain types, testable business rules, modular monolith, replaceable external-provider boundaries.
- **Portability:** Avoid tying user data/API design to one client; support export and future native client without prematurely building one.
- **Reliability/operations:** Document backup, restore, migration, monitoring, error handling, and rollback requirements before production.
- **Cost sustainability:** No mandatory large paid catalogue or image-generation service for MVP; record storage/bandwidth/auth/operations assumptions before adopting providers.
- **Content integrity:** Historical factual claims have traceable sources (GC-DATA-001); AI output alone is not evidence (GC-AI-001).

## Cross-cutting acceptance expectations

For relevant features, acceptance must cover: loading/empty/error/permission states; mobile and keyboard usage; ownership boundaries; uncertain or missing metadata; multiple copies/releases; privacy defaults; test evidence; and updates to directly affected documentation/diagrams. Product owner approves exact feature acceptance before implementation.
