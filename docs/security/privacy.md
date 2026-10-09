# Security, privacy, and trust requirements

**Status:** Threat-control outline; no authentication, database, storage, or deployment exists.

## Data classification and defaults

- **Private personal data:** account identity, collection membership, owned-copy details, paid prices, private notes, acquisition context, and personal photos.
- **Catalogue/editorial data:** game/release facts, sourced claims, approved public exhibits and rights-cleared media.
- **Community submissions (future):** submitted art, rights attestation, reports, moderation decisions, and audit history.

Collection records and personal photographs are private by default. Public collection sharing and public use of an individual photograph require explicit, understandable, revocable consent and separate visibility controls. Public views must allow-list fields and never expose private prices, notes, account identifiers, storage keys, or metadata by accident.

## Required controls before implementation/release

| Area | Requirement / evidence |
| --- | --- |
| Authentication/session | Choose secure identity/session approach; protect state-changing actions; plan revocation, session expiry, recovery, and account deletion. Verify with tests. |
| Authorization | Enforce owner scope at server and persistence/storage boundaries; test cross-user read, write, list, and object access denial—not only signed-in success. |
| Database RLS | If supported by chosen service, enable least-privilege policies for every user-owned table and verify privileged/server keys cannot bypass into browser code. |
| Private storage | Non-public buckets/objects by default; short-lived access mechanism if needed; bind every object to owner/copy; authorize upload/read/delete and test guessed identifiers. |
| Upload safety | Allow-list needed formats, size/dimension limits, MIME/signature checks, safe decoding/re-encoding where appropriate, malware/scanning decision, metadata handling, rate limits, and abuse path. |
| Privacy choices | Explain exactly which collection fields/media are public, default private, require explicit action, allow revocation, and test public response allow-list. |
| Export/deletion | Define portable data export and account deletion, object deletion, retention exceptions, backups, and deletion propagation before launch. |
| Secrets | Store server secrets in environment/managed secret service; no privileged keys in source, browser bundles, issue logs, or error messages. Rotate and audit access. |
| Abuse prevention | Rate-limit auth, search, upload, report, and submission paths; anti-automation and account recovery policies need threat review. |
| Audit/logging | Log security-relevant actions with minimum necessary data; never log passwords, tokens, private notes, paid price, signed URLs, or image contents. |
| Dependency handling | Track vulnerabilities, supported versions, update ownership, and severity response. Use dependency/security checks in CI after stack selection. |
| Backup/recovery | Define encryption, access, retention, RPO/RTO targets and test restore; do not claim backup safety from provider availability alone. |
| Moderation | Future public artwork needs reporting, rate limits, review queue, rights attestation, takedown, audit trail, and human handling of uncertainty. |

## Threat scenarios for Gate 1/2

Cross-account record/object enumeration; insecure direct object reference; overly permissive RLS or service-role exposure; public storage/cache leakage; malicious/oversized uploads; EXIF/location disclosure; forged file type; private fields included in public API; account takeover; abuse of correction/art forms; accidental secret exposure; data loss or incomplete deletion from backups.

## Escalation

Stop and escalate any suspected private-data exposure, privileged-key leak, rights dispute, high-impact vulnerability, or untested access boundary. No claim of legal compliance or security certification is made.
