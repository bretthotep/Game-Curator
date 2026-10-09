# Proposed MVP scope

**Status:** Gate 0 recommendation only; the product owner must approve scope and Gate 1 artifacts before implementation.

## Objective

Prove that a collector can privately catalogue a real physical game copy, understand what is game/release metadata versus their owned object, and return to a clear, attractive collection view. Keep the initial catalogue small and explicit; do not require a paid proprietary catalogue.

## Minimum viable first vertical slice (proposal)

1. A collector signs in (or uses an explicitly approved secure single-user prototype during a technical spike).
2. The collector searches a small labelled seed dataset and selects a game/release.
3. The collector records one or more physical copies, including edition/region and optional condition/completeness/acquisition/price fields.
4. The collector sees and edits their copy in a responsive private collection card/list.
5. Another account cannot read or change those records; empty, loading, error, and denied states are handled.

The proposed first slice does not require public sharing, valuation, community artwork, or purchase of a large catalogue. Secure personal photo upload is a highly valued candidate follow-on slice and must pass a storage/access-control spike before inclusion. It must not be called complete if only a local/mock upload exists.

## Capability disposition

| Capability | Proposed disposition | Reason/dependency |
| --- | --- | --- |
| Authentication | First slice or proven secure prototype | Multi-user data requires trustworthy identity and session behavior. |
| Useful empty state | First slice | Core onboarding and accessibility. |
| Small searchable seed catalogue | First slice | Proves the collecting loop without proprietary dependency. |
| Physical-copy create/edit and edition/region/condition/completeness/date/optional paid price | First slice, staged fields | Core product outcome; exact controlled vocabularies need Gate 1 review. |
| Secure personal photographs | Candidate next slice | Strong user value; depends on storage policy, validation, cost, deletion, and recovery evidence. |
| Responsive collection cards | First slice | Central presentation, subordinate to task clarity/accessibility. |
| Game detail distinct from copy | First slice | Enforces core domain distinction. |
| Search, filters, sorting | Search first; refine after evidence | Search supports selection; advanced refinement can follow. |
| Basic collection statistics | Follow-on | Not required to prove first-copy loop; avoid monetary success framing. |
| Sample sourced historical exhibit | Separate editorial slice | Requires structured evidence, review, citations, and corrections. |
| CI and reproducible automated tests | Required delivery foundation | Must be established with selected stack before feature claims. |
| Public collection sharing | Deferred | Needs explicit visibility, abuse, privacy, and indexing decisions. |
| Community artwork submissions/voting | Deferred | Needs rights attestation, moderation, reporting, takedowns, and human review. |
| Valuation feeds, AI content generation at scale, leaderboards, marketplace, paid catalogue, native iOS | Deferred | Business value, evidence, licensing, cost, and approval prerequisites absent. |

## Proposed acceptance for the first slice

- A user can distinguish catalogue title/release from every individual owned copy.
- Multiple copies of one release can be recorded independently.
- Optional price paid is stored as a transaction detail and is never presented as market value.
- A small seed dataset is labelled as seed/sample data; missing catalogue details are not invented.
- A collection is private by default; a second user is denied read and write access.
- Core add/view/edit paths work with keyboard and narrow viewport; loading, empty, error, and permission-denied states are understandable.
- Automated tests cover the domain rules and access boundary, and CI results are recorded.
- Documentation/diagrams reflect implemented behavior, not future architecture.

Acceptance details require review alongside the security model, design direction, and selected technology at Gate 1.

## Explicit non-goals for initial MVP

No comprehensive game database, price/valuation prediction, marketplace, public community image catalogue, automated historical prose, elaborate gamification, insurance reports, native iOS application, paid subscription enforcement, or production-scale operation until prerequisite decisions and business value are established.
