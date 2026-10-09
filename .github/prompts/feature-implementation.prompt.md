# Feature implementation prompt

Implement one approved, bounded GameCurator vertical slice. First inspect the issue, repository state, relevant files, existing tooling, tests, architecture decisions, and applicable scoped instructions. Do not broaden scope.

Preserve the distinction between Game, Platform, Release/Edition, and individual Physical Copy. Treat user data and personal photos as private by default; test cross-user access denial. Validate untrusted input at boundaries, use migrations for schema changes, and keep secrets out of source/client bundles/logs.

Add appropriate tests and update affected documentation/diagrams. Run only existing validation commands and report exact outcomes. Label mocks, seeds, and stubs. Escalate unclear requirements, paid dependencies, rights issues, destructive changes, or consequential decisions instead of silently proceeding. Request independent review; do not self-approve or merge.
