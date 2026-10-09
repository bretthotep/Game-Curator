# Local development and deployment status

**Status:** No application or toolchain has been selected or implemented. This document intentionally does not invent setup commands.

At Gate 0 the repository contains documentation, GitHub workflow templates, and editor settings only. There is no package manifest, application code, test suite, database migration, seed SQL, deployment configuration, or CI workflow. Therefore there is no verified local run/build/test command.

After Gate 1 approval, the first implementation issue should establish the approved web stack and reproducible local setup, including:

- supported runtime/package manager versions and exact install, development, lint, type-check, build, and test commands;
- example environment-variable names without secrets and secure secret setup;
- local database/auth/storage or isolated test equivalents and migration/seed/reset instructions;
- how to run access-control and end-to-end tests without production data;
- CI workflow matching local checks, dependency/security scanning, and artifact handling;
- deployment environment separation, migration order, rollback limitations, backup/restore, monitoring, and incident contacts.

Do not add real credentials, production data, or privileged keys to examples. Do not describe local service emulation or mocks as a production integration.
