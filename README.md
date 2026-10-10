# GameCurator

GameCurator is a proposed community-powered digital museum for physical video-game collecting. It is intended to help collectors catalogue the physical games they own, discover their history, and share curated collections.

## Project status

This repository is at **Gate 0 — Project Foundation**. It contains project governance and planning documentation only; no application, production integration, or validated technical spike is present. Product and architecture proposals are provisional pending human product-owner review.

## Start here

- [Product vision and personas](docs/product/vision-and-personas.md)
- [Detailed requirements, user stories, and workflows](docs/product/requirements.md)
- [Proposed MVP](docs/product/mvp-scope.md) · [Prioritised roadmap](docs/product/roadmap.md)
- [User journeys](docs/product/user-journeys.md) · [Phased, issue-ready backlog](docs/operations/proposed-backlog.md)
- [Technical design document for review](docs/architecture/overview.md) · [Domain model and data dictionary](docs/architecture/domain-model.md)
- [Technology evaluation](docs/architecture/technology-evaluation.md)
- [Risk and assumption register](docs/operations/risks-and-assumptions.md)
- [Open product-owner decisions](docs/operations/open-decisions.md)
- [Quality and delivery strategy](docs/quality/testing-and-delivery.md)
- [Contributor and agent instructions](.github/copilot-instructions.md)

## Decisions and status

The initial technology choices, domain model, and architecture are proposals, not approved commitments. See [ADR-0001](docs/architecture/decisions/0001-provisional-technology-and-modular-monolith.md), the [proposed MVP](docs/product/mvp-scope.md), and the [prioritised roadmap](docs/product/roadmap.md). Paid services, public sharing, production deployment, and irreversible architecture decisions require explicit human approval.

No GitHub issues, tests, integrations, or deployments are claimed as completed by this foundation. Continue with Gate 1 product and architecture review before implementation.

## Review and build guide

1. Review the requirements and MVP boundary, then the technical design, domain model, privacy controls, and content policies.
2. Resolve the [open decisions](docs/operations/open-decisions.md) through the Gate 1 approval issues. Diagrams describe proposed workflows, not running services.
3. Use the backlog's stable `GC-I-*` identifiers to review and file individual issues. These are detailed issue drafts, **not created GitHub issues**; record real issue URLs when they are filed.
4. Review Gate 2 evidence before authorizing the private collecting slice. Photos, editorial content, and public/community features remain separately gated; they are not mandatory for a private-first release.
5. Follow the [agent handoff and setup contract](docs/operations/local-development.md) and [acceptance evidence strategy](docs/quality/testing-and-delivery.md). No verified application commands exist yet.

Requirements own feature behavior and acceptance references; the backlog owns work-item scope and dependencies; the roadmap owns phase sequencing; the technical design owns proposed system boundaries. Changes to any of these must update affected references together.