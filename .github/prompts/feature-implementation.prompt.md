# Feature implementation prompt

Implement one approved, bounded GameCurator vertical slice. First inspect the issue, repository state, relevant files, existing tooling, tests, architecture decisions, and applicable scoped instructions. Do not broaden scope.

Resolve the issue's stable GC-I identifier in `docs/operations/proposed-backlog.md`; read its linked F/NFR and AC references in `docs/product/requirements.md`, phase in `docs/product/roadmap.md`, technical design in `docs/architecture/overview.md`, and handoff contract in `docs/operations/local-development.md`. Confirm recorded human approvals and prerequisite evidence. Issue drafts and diagrams do not authorize implementation; stop on missing approvals or conflicting scope.

Preserve the distinction between Game, Platform, Release/Edition, and individual Physical Copy. Treat user data and personal photos as private by default; test cross-user access denial. Validate untrusted input at boundaries, use migrations for schema changes, and keep secrets out of source/client bundles/logs.

Add appropriate tests and update affected documentation/diagrams. Run only existing validation commands and report exact outcomes. Label mocks, seeds, and stubs. Escalate unclear requirements, paid dependencies, rights issues, destructive changes, or consequential decisions instead of silently proceeding. Request independent review; do not self-approve or merge.

Hand off criterion-by-criterion evidence, candidate commit, actual commands/manual procedures and results, security/privacy impact, affected documents, limitations and rollback notes to the named independent reviewers. Use `docs/quality/testing-and-delivery.md` for the evidence contract. Keep credentials and private collector data out of all evidence.
