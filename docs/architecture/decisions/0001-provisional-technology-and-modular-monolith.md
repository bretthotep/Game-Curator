# ADR-0001: Provisional web-first technology direction and modular monolith

- **Status:** Proposed, not approved.
- **Date:** 2026-10-09
- **Decision owners:** Human product owner (approval pending); architecture recommendation prepared for Gate 1.

## Context

GameCurator needs to prove a private physical-copy collection experience, while the long-term product also includes shareable web exhibits and may later support native iOS. There is no implementation, user research, technical spike, approved budget, or provider evaluation in the repository yet. The relational domain has many explicit relationships and strong ownership/privacy constraints.

## Options considered

1. Responsive Next.js/React/strict TypeScript web application, with PostgreSQL/auth/private storage through a managed service such as Supabase.
2. Native SwiftUI-first client with a separately operated backend.
3. Cross-platform native client plus shared backend.
4. Web frontend plus self-managed PostgreSQL/API and operational stack.

## Decision

**Proposed:** Start with a responsive web application and modular monolith; evaluate PWA capabilities without assuming they are mandatory. Use explicit domain/API boundaries and a relational data model. Treat Next.js, React, TypeScript, Tailwind, accessible component system, Supabase/PostgreSQL/Auth/Storage, Zod, Vitest, React Testing Library, Playwright, and GitHub Actions as candidate defaults only. Defer selecting/adding dependencies and paid providers until Gate 1 approval and relevant Gate 2 evidence.

## Rationale

A web-first experience best tests collection entry and public editorial presentation across devices without requiring mobile-store distribution. Relational persistence fits game/release/copy ownership relationships and constraints. A modular monolith limits initial operational burden while server-side APIs and domain boundaries can later serve an iOS client. Native-first remains credible if validated users prioritize camera/barcode capture over public web discovery.

## Consequences

- Gate 1 must confirm first-slice requirements, security model, data model, API boundary, visual interaction direction, and provider terms.
- Gate 2 must test authentication/access isolation, private media lifecycle, catalogue search against permitted data, responsive cards/accessibility, camera/barcode feasibility, CI/deployment, backup/restore, and cost assumptions.
- Keep provider integrations behind replaceable interfaces and make MVP usable with a small labelled seed dataset and collector-provided metadata/photos.
- No app, database, service, package, API, paid plan, or production deployment is established by this ADR.

## Risks

- Managed service terms, pricing, limits, and platform behavior may change or not meet access-control/export/recovery needs.
- Browser camera/barcode behavior may be inconsistent across devices.
- Web-first may under-serve collectors who prioritize offline/native capture.
- Without explicit RLS and storage rules, a convenient managed backend can still expose private collections/media.
- Framework choice before user validation can create avoidable maintenance or provider lock-in.

## Conditions for reconsideration

Reopen if user research shows native capture/offline use is essential to the first outcome; a Gate 2 spike finds managed auth/storage cannot meet privacy/export/recovery requirements; current costs/terms exceed an approved budget; or deployment/accessibility/maintenance evidence favors an alternative. Reconsideration requires comparative evidence and human product-owner approval.
