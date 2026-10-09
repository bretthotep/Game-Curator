# Testing, quality gates, and delivery strategy

**Status:** Gate 0 policy. Tool choices are provisional in `docs/architecture/technology-evaluation.md`; no test/build/lint workflow currently exists.

## Quality principles

Test outcomes and trust boundaries, not merely happy paths. Keep domain rules testable independently of UI/persistence. Maintain strict typing, runtime validation at trust boundaries, consistent errors, accessibility, security checks, migrations, and actual documentation. Do not weaken tests/gates or remove functionality to obtain a pass.

## Test layers after stack approval

| Layer | Focus | Candidate evidence |
| --- | --- | --- |
| Unit/domain | Game/release/copy distinction, multiple copies, completeness/condition rules, price-vs-valuation distinction, uncertainty, validation | Vitest candidate; deterministic business-rule tests |
| Component | Forms, responsive cards, empty/loading/error/denied states, keyboard behavior, accessible names/feedback | React Testing Library candidate |
| Integration | Persistence, migrations, owner scoping, database policies, private storage lifecycle, export/delete boundaries | Isolated test database/storage or controlled test environment |
| End-to-end | Sign-in, search seed catalogue, add/edit copy, view private collection, permission denial, correction journey when implemented | Playwright candidate |
| Non-functional | Keyboard and screen-reader checks, contrast/reduced motion, responsive viewport, dependency/security checks, performance/cost bounds | Explicit checklist and recorded tools/results |

Test negative cases including a second user's attempts to read/update/delete records and objects; unknown/incomplete catalogue data; multiple copies of one release; malformed and oversized uploads; revoked photo visibility; migration compatibility; and failures/timeouts.

## Pull request quality gate

Every implementation PR should have issue/acceptance linkage, focused diff, automated tests and exact results, independent review, security/privacy considerations, documentation/diagram updates, known limitations, and migration/rollback notes. Required checks should include formatting/lint/type checking, tests, dependency/security scan, and build once the actual stack exists. Do not claim any check passed unless observed on the candidate commit.

## Gate-aware validation

- Gate 0: cross-check documents and templates; no application tests expected.
- Gate 1: approval of requirements, architecture/security/design, and ADRs.
- Gate 2: repeatable spike evidence for the highest-risk assumptions.
- Gate 3: per-slice tests/review/docs with passing mandatory checks.
- Gate 4: release candidate test suite, accessibility/security/dependency review, production config, migration, backup/restore, monitoring, and rollback evidence.
- Gate 5: human approval after a release-readiness report; do not deploy before approval.

## Reporting

Record commit/PR, command, environment, result, and known omissions. Mark each validation as passed, failed, not run, or blocked. Distinguish static review from executed tests and design review from accessibility conformance testing.
