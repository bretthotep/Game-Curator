# Proposed follow-up issue backlog

**Status:** Issue proposals only. These items have not been created in GitHub; the available session tools do not include issue creation.

Each proposal is structured so it can be filed with `.github/ISSUE_TEMPLATE/feature.yml`. Priorities/dependencies are provisional and do not authorize implementation ahead of the relevant gate.

## P1 — Review and approve product MVP definition (Gate 1)

- **Requirement and rationale:** Confirm which collector outcome the first release must prove; Gate 0 personas, requirements, MVP, and journeys are hypotheses.
- **User story/outcome:** As product owner, I want a bounded, testable first-release definition so implementation solves a validated collector problem.
- **Acceptance criteria:** Review personas and assumptions; approve first vertical slice and exclusions; define required fields, privacy behavior, success signals, and testable acceptance criteria; record decisions and unresolved validation needs.
- **Dependencies:** Gate 0 documentation.
- **References:** `docs/product/vision-and-personas.md`, `requirements.md`, `mvp-scope.md`, `roadmap.md`, `user-journeys.md`.
- **Required tests/evidence:** Product-owner review; user-research evidence if undertaken; no code test implied.
- **Documentation impact:** Update approved status, acceptance criteria, roadmap, and decision record.
- **Definition of done:** Explicit human product-owner approval; assumptions remain labeled; no scope silently expanded.

## P2 — Approve architecture, data, and security boundaries (Gate 1; depends on P1)

- **Requirement and rationale:** Confirm a technically viable, privacy-preserving path for multi-user physical-copy records.
- **User story/outcome:** As the product team, we need approved domain and access boundaries before persisting personal collections.
- **Acceptance criteria:** Compare web-first recommendation with SwiftUI-first and self-managed alternatives; review Game/Platform/Release/Copy relationships; decide owner/access model, public/private policy, migration/export/deletion requirements, and managed-provider evaluation criteria; approve/revise ADR-0001.
- **Dependencies:** P1 product/MVP direction.
- **References:** `docs/architecture/overview.md`, `domain-model.md`, `technology-evaluation.md`, `decisions/0001-provisional-technology-and-modular-monolith.md`, `docs/security/privacy.md`.
- **Required tests/evidence:** Architecture and security review; identify Gate 2 spike evidence, not claims that spikes already passed.
- **Documentation impact:** Update approved ADR, diagrams, constraints, and risks.
- **Definition of done:** Human approval for material choices; unresolved provider/cost questions captured.

## P3 — Approve catalogue, artwork, and historical-content policies (Gate 1; parallel with P2 after P1)

- **Requirement and rationale:** Prevent unlawful reuse and unsupported history/art claims while defining an MVP data/content source.
- **User story/outcome:** As a collector or reader, I want trustworthy metadata, imagery, and exhibits with transparent provenance.
- **Acceptance criteria:** Approve seed-data provenance and completeness behavior; define provider/license evaluation; confirm catalogue/personal-card artwork fallbacks, rights attestation, moderation/takedown, citation model, fact classifications, and correction review workflow.
- **Dependencies:** P1 scope; coordinate domain decisions with P2.
- **References:** `docs/research/catalogue-and-licensing.md`, `artwork-policy.md`, `historical-provenance.md`, `docs/architecture/domain-model.md`.
- **Required tests/evidence:** Rights/terms review for any real source; sample exhibit editorial evidence before publishing content.
- **Documentation impact:** Update policy with actual reviewed sources/decisions and unresolved rights.
- **Definition of done:** Product-owner approval; no provider or public community artwork enabled by documentation alone.

## P4 — Run Gate 2 technical risk spikes (depends on P2 and applicable P3 decisions)

- **Requirement and rationale:** Validate the highest-risk auth, isolation, private-upload, search, responsive UX, device, deployment, and cost assumptions before feature implementation.
- **User story/outcome:** As the team, we need reproducible evidence before selecting services and committing to an implementation path.
- **Acceptance criteria:** Test owner isolation including denied cross-user reads/writes/objects; test private photo lifecycle and validation if storage is considered; exercise search using permitted seed data; prototype responsive accessible cards; investigate camera/barcode on target devices; verify CI, migrations, export/restore options, and cost assumptions.
- **Dependencies:** P2 architecture/security approval; P3 rights decisions for provider/data/media experiments.
- **References:** `docs/architecture/technology-evaluation.md`, `docs/security/privacy.md`, `docs/quality/testing-and-delivery.md`, `docs/operations/risks-and-assumptions.md`.
- **Required tests/evidence:** Exact environment/steps/results, failure cases, source-dated costs/terms, limitations, reproducible tests.
- **Documentation impact:** Record spike reports, revise ADR, risk register, and recommendations.
- **Definition of done:** Human review of evidence and approval of Gate 3 direction; no untested capability represented as validated.

## P5 — Implement approved private collection vertical slice (Gate 3; depends on P1–P4 approval)

- **Requirement and rationale:** Deliver the smallest central collector experience without a proprietary catalogue dependency.
- **User story/outcome:** As a collector, I want to find a seed title/release, record individual physical copies, and privately view/edit them.
- **Acceptance criteria:** Implement only approved stack/scope; support multiple copies per release; distinguish game/release/copy and paid price from valuation; provide privacy-safe empty/loading/error/denied states and responsive, accessible collection view.
- **Dependencies:** Product/architecture/security approval and relevant spikes; licensed/owned seed content.
- **References:** Approved MVP and ADR; `docs/architecture/domain-model.md`, `docs/security/privacy.md`, `docs/design/design-principles.md`.
- **Required tests/evidence:** Domain tests, cross-user access denial, relevant persistence and end-to-end journeys, existing CI gates, independent review.
- **Documentation impact:** Update architecture/data-flow diagrams, local-development/deployment instructions, security and quality docs with actual implementation.
- **Definition of done:** Acceptance evidence, actual test results, docs, security review, independent review, and human gate review; no production release implied.

## Recommended next issue

Start with **P1 — Review and approve product MVP definition**. The other decisions depend on knowing which user outcome and privacy expectations the initial slice must satisfy.
