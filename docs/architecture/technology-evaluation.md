# Provisional technology evaluation

**Status:** Desk-level proposal only. No technical spike, pricing verification, or human approval has occurred. Validate current versions, terms, and costs before adoption.

## Candidate approaches

| Approach | Benefits | Trade-offs / risks | Gate 0 view |
| --- | --- | --- | --- |
| **Responsive Next.js/React web + TypeScript; Supabase/PostgreSQL/Auth/Storage** | Fast responsive public/private web experience; SQL and relational constraints fit game/release/copy model; managed auth/storage can reduce initial operations; web sharing is natural. | Provider coupling, evolving product/pricing, RLS configuration burden, server/client boundaries, image-storage costs, framework maintenance. TypeScript does not alone guarantee runtime-safe input. | Provisional MVP default; validate authorization, data export, upload, deployment, and costs. |
| **Native SwiftUI-first + custom backend** | Strong Apple platform integration, camera/barcode access, native accessibility conventions, offline/device UX. | iOS-only first; slower public collection sharing/discovery; separate backend/auth/storage still needed; greater initial implementation/operations scope; Android/web absent. | Meaningful alternative; consider if validated research makes native capture the primary first outcome. |
| **Cross-platform native (e.g. React Native) + shared backend** | Shared JavaScript/TypeScript skills and mobile camera potential; native-like interaction. | Still requires app distribution and web experience for public sharing; platform-specific behavior and web/native divergence; increases surface area before product validation. | Not preferred for first proof; revisit after capture/channel evidence. |
| **Custom-managed PostgreSQL/API + web frontend** | Greater control, portability, and tailored backend boundaries. | More operational responsibility for auth, storage, upgrades, backups, monitoring, and security; slower MVP without evidence of a managed-service blocker. | Viable alternative if managed-provider constraints become material. |

## Evaluation dimensions

- **Development speed:** Managed web stack likely supports quickest test of private catalogue/collection loop; this is a hypothesis, not measured.
- **Camera/barcode:** Native SwiftUI has direct platform APIs; mobile browsers may provide capture but availability and scan quality require a Gate 2 spike. Barcode search provider/licensing is separate.
- **Public sharing:** Web-first URLs offer a low-friction shareable surface; sharing remains off until privacy controls are designed.
- **Cost/deployment:** Managed services reduce operations but may incur authentication, database, storage, egress, and bandwidth costs. No current cost quote or service commitment is approved.
- **Accessibility:** All candidates can support accessible experiences; actual behavior depends on component/interaction implementation and testing.
- **Future iOS:** A documented domain/API boundary and portable PostgreSQL schema can serve native clients later. Web choice does not require a native application now.
- **Maintenance:** Prefer small modular monolith and managed infrastructure where costs/terms/controls are acceptable; avoid premature microservices and multiple clients.

## Provisional defaults to test, not commitments

Next.js and React, strict TypeScript, Tailwind CSS with an accessible component system, Supabase/PostgreSQL for initial database/auth/storage, Zod at runtime trust boundaries, Vitest and React Testing Library for unit/component tests, Playwright for critical browser journeys, GitHub Actions for CI. Evaluate Progressive Web App/offline capabilities rather than assuming they are required.

No packages, providers, current pricing, licenses, service-level commitments, API capabilities, or platform policies have been verified. Before dependency adoption, validate package health/security and current terms; before commercial use, get human approval.

## Gate 2 spikes recommended

1. Demonstrate authenticated user isolation at the API/database/storage layers, including negative tests for cross-user read/write and object access.
2. Upload, retrieve, replace, and delete an allowed personal photo privately; test file validation, metadata leakage, size limits, access URLs, and deletion semantics.
3. Exercise catalogue search against only an owned/licensed seed dataset; document incomplete data behavior and provider replacement boundary.
4. Prototype responsive collection card/detail form with keyboard, narrow viewport, zoom, and reduced motion checks.
5. Assess browser camera/barcode feasibility on target devices without assuming support.
6. Verify CI reproducibility, migration workflow, backup/restore options, deployment constraints, and estimated costs using current published plans and a stated usage model.

Each spike needs recorded environment, exact steps/results, limitations, and recommendation. No spike is claimed complete.
