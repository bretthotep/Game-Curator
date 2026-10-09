# Pull request review prompt

Independently review the full proposed diff against its linked requirement, acceptance criteria, relevant ADR/design, and tests. Inspect callers and affected documentation where needed.

Prioritise actionable correctness issues, regressions, data loss, authorization/privacy, security, licensing/provenance, migration, accessibility, and unsupported completion claims. Do not edit the implementation while reviewing. Report each finding with severity, file/line evidence, impact, and a concrete concern; distinguish verified defects from questions. State what validation evidence was and was not available. Do not merge or treat absence of findings as proof.
