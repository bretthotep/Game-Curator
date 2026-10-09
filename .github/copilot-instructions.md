# GameCurator Copilot instructions

## Mission and current stage

Build GameCurator as a trustworthy, art-forward digital museum for physical video-game collecting—not merely an inventory, marketplace, or conventional game database. Preserve the distinctions between a Game, Platform, Release/Edition, and individually owned Physical Copy. The repository is currently at Gate 0; do not implement the application until Gate 1 decisions have been reviewed and approved.

## Decision authority and honesty

- The human product owner retains approval of material product/architecture decisions, commercial commitments, production releases, and merges.
- Mark proposals, assumptions, seeds, mocks, and unvalidated integrations accurately. Never state that a test, review, independent agent, issue, PR, or integration happened unless evidence confirms it.
- Do not claim licensing rights based on availability or user upload. Escalate legal ambiguity, disputed artwork, material costs, privacy risks, and irreversible choices.
- Do not merge your own work, bypass protection, or weaken quality gates.

## Product and domain invariants

- Catalogue titles, releases, owned copies, collections, and media are separate concepts. Multiple releases may belong to one game; users may own multiple copies of a release.
- A copy's price paid is not its estimated market value. Keep condition, completeness, region, currency, date, methodology, and provenance with any valuation.
- Historical claims presented as fact require traceable evidence (GC-DATA-001); generative AI is never evidence by itself (GC-AI-001). Flag disagreement and uncertainty.
- Personal photos remain private by default and cannot be overwritten by community voting. Catalogue art, generated art, community art, and personal photos have separate rights and lifecycle rules.
- Prefer an accessible, responsive editorial-card experience. Do not use virtual shelves or cabinets as the primary metaphor, overvalue expensive games, or make paid services mandatory for MVP.

## Engineering requirements

When implementation is approved:

- Use strict TypeScript, explicit domain types, runtime validation at trust boundaries, and consistent errors.
- Keep business rules independent of UI and persistence; use modular boundaries and interfaces where they improve testability or replaceability.
- Use migrations for schema changes; identify seed/test data; test domain rules, persistence/access control, and critical journeys at appropriate levels.
- Design authorization and storage so no user can access another user's private records or photographs. Keep server secrets out of browser code and logs.
- Add focused changes, tests, and documentation/diagram updates. Preserve existing functionality; inspect references and tests before any substantial removal.
- Use only existing repository tooling until the stack is approved. Do not invent commands or test results.

## Collaboration and delivery

Use the specialist definitions in `.github/agents/` as role boundaries. Assign bounded work, state dependencies and handoffs, and obtain independent review before work is considered complete. If native delegation is unavailable, label simulated role analysis honestly.

Every change should identify its requirement, acceptance evidence, tests, security/privacy impact, documentation impact, and known limitations. Follow the PR template. Escalate open product choices instead of silently deciding them.
