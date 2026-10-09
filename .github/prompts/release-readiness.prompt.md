# Release readiness prompt

Prepare a release-readiness assessment for the exact candidate commit. Verify the approved scope, linked PRs, required checks, test results, accessibility and security evidence, dependencies, migration behavior, production configuration, secrets handling, monitoring/error handling, backups/restore, operating costs, known limitations, and rollback procedure.

For every check, report evidence and status as passed, failed, not run, or blocked. Never infer success from configuration alone. List defects, residual risks, operational dependencies, and owner decisions. Give a recommendation, but do not deploy or release: the human product owner must explicitly approve Gate 5.
