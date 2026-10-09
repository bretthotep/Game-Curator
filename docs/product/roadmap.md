# Prioritised roadmap proposal

**Status:** Gate 0 sequencing proposal; not a delivery commitment.

| Order | Outcome / gate | Dependencies and exit evidence |
| --- | --- | --- |
| P0 | Gate 0 — Foundation | Governance, role definitions, initial product/architecture/security/research/quality documents, risk register, and open decisions. This repository change establishes planning artifacts only. |
| P1 | Gate 1 — Product and architecture approval | Approved MVP and acceptance criteria; journeys/navigation; initial design; architecture/data model/security; catalogue/artwork/content rights assessment; ADRs and diagrams. Human product-owner review required. |
| P2 | Gate 2 — Technical proof of concept | Small experiments for authentication/access control, private upload, catalogue search, responsive cards, camera/barcode feasibility, CI/deploy options, and cost assumptions. Record actual results, limitations, and recommendation; do not imply untested capability. |
| P3 | Gate 3a — Private collecting loop | Approved stack and thin slice: identity, small seed catalogue, add/edit individual copy, private responsive collection, owner-only record export, authorization tests, and CI. Independent review and docs required. |
| P4 | Gate 3b — Preserve and discover | If approved: secure personal photos, collection filters/statistics, then sourced exhibit/references/correction workflow as separate slices with appropriate evidence. |
| P5 | Gate 3c — Optional sharing/community | Only after privacy, moderation, rights/takedown, abuse controls, and human review are approved and implemented. |
| P6 | Gate 4 — Release candidate | Required test suite, accessibility/security/dependency/production-config checks, migrations, backup/restore, monitoring, known limitations, and rollback evidence. |
| P7 | Gate 5 — Human release approval | Evidence-based readiness report and explicit product-owner approval before production release. |

## Sequencing rules

- Keep the first implementation issue bounded to the approved first vertical slice; split photo upload and editorial exhibit if their prerequisites are not ready.
- No native app, paid provider, large catalogue, valuation service, or expensive generation pipeline before documented recommendation and human approval.
- Roadmap order is a dependency hypothesis, not a schedule. Reprioritize only with product-owner review and recorded rationale.
