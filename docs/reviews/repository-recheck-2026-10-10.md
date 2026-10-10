# GameCurator repository recheck

**Date:** 2026-10-10  
**Reviewed branch:** `main` at commit `44e2a7e168d8a712249db55aba1f4ca31f0ec2b4` at review time  
**Scope:** Current README, requirements, architecture/domain model, design principles, local-development/agent handoff, catalogue/artwork research, and reference-library structure.  
**Status:** Focused documentation review; no application build or runtime security audit.

## Summary

The repository has materially improved since the initial review. The planning is now more traceable: the README describes the source-of-truth roles for requirements, backlog, roadmap, and technical design; the proposed backlog has stable `GC-I-001`–`GC-I-044` identifiers; requirements and the domain model contain more detailed workflows and constraints; and privacy, media precedence, licensing, deletion, provenance, and release gating are better articulated.

The repository remains a Gate 0/Gate 1 planning baseline. These are proposals, not proof of implementation, licensed assets, validated integrations, or approved decisions. The best next step is to use a small set of visual references and resolve the few decisions that block the first vertical slice—not expand documentation indefinitely.

## What has improved

- **Traceability:** the README now explains the distinct responsibility of requirements, backlog, roadmap, and technical design.
- **Backlog readiness:** work items include dependencies, acceptance evidence and specialist handoffs. They remain draft specifications until individually filed as GitHub issues.
- **Domain precision:** the domain model calls out owner-equality invariants, unknown release options, private price-paid data, source-to-claim links, and media category separation.
- **Artwork policy:** personal photos, catalogue defaults, generated interpretations and community submissions have distinct visibility/rights treatment and fallback precedence.
- **Historical provenance:** claim/source/correction relationships and uncertainty are recognised as core integrity needs.
- **Delivery realism:** Gate 2 evidence, automated owner-boundary tests, backup/restore, rollback and explicit human release approval are included.

## Findings and recommendations

### P1 — Approve a bounded first-slice contract

Several central policies remain open: known-release-only versus an honest unmatched-copy workflow; exact condition/completeness vocabularies; collection grouping/membership; export fields/format; and lifecycle/archive/deletion semantics. Resolve only what is needed for the first private collecting loop, record the choice, and avoid implementing future sharing, valuation or moderation in advance.

**Exit evidence:** one approved journey, field dictionary subset, seed fixtures, export contract, and acceptance examples.

### P1 — Use the new visual references to make Gate 1 review concrete

The design principles are clear but still not a tested visual system. This change adds original SVG reference boards under `ideas/references/`: overall direction, collection-screen concept, exhibit/timeline concept, and a generic pixel-art study. They use fictional titles and abstract art, not game-cover reproductions. They are inspiration assets, not final approved screens or production art.

**Exit evidence:** product-owner choice of visual direction, responsive screen hierarchy, typography/colour/spacing tokens, image fallback rules, and accessibility target.

### P1 — Keep requirements and the 44-item backlog synchronised

The document set is much more complete, which creates a new risk: changes can be duplicated or drift between requirement behavior, work-item scope, design, and architecture. Use stable IDs as links; make one file authoritative for each concern; add only cross-links in other documents. Do a small automated or scripted link/ID consistency check before implementation.

**Exit evidence:** valid internal links, unique IDs, no contradictory acceptance criteria, and a traceability table for the first slice.

### P2 — Clarify the meaning of “Gate 0” versus “Gate 1”

The README says Gate 0 while several documents are now described as Gate 1 review models. This is not necessarily contradictory: planning artifacts can be prepared during Gate 0 for Gate 1 approval. Make the gate terminology explicit in the README or a short gate-status record, including which artifacts are drafted, which decisions are pending, and what constitutes Gate 1 approval.

### P2 — Separate reference assets from approved production assets

The reference folder should retain source, author/creator, rights status, intended lesson and approval state. The SVGs are described as repository-authored illustrations, but their individual creator/owner and any applicable licence or redistribution permission are not independently recorded. Repository presence is not permission, so no redistribution right is claimed. For external images, prefer a source link and observations unless permission to commit the actual image is clear.

### P2 — Avoid treating diagrams as proof

Mermaid and SVG diagrams help review architecture and UX, but do not prove authorization, accessibility, provenance, backup, or operational behavior. For each Gate 2 spike, record environment, test procedure, result, limitations, and reviewer. For the first slice, include a two-account denial test and export-owner-boundary test.

## Reference assets added in this change

- `ideas/references/visual-direction/gamecurator-visual-direction.svg` — mood, palette, editorial typography and abstract artwork.
- `ideas/references/collection-ui/collection-screen-concept.svg` — private collection screen, search, add-copy action, and copy counts.
- `ideas/references/game-history-exhibits/history-exhibit-concept.svg` — exhibit layout, timeline, claim/source labels and evidence panel.
- `ideas/references/pixel-art/original-art-direction-study.svg` — generic original pixel-art style study.

These assets are SVG source files, so they remain inspectable and editable in the repository. No externally sourced game artwork was copied. They are illustrative concepts and do not represent completed UX research or accessibility validation.

## Recommended next actions

1. Review and approve the first-slice product choices only.
2. Select or revise one visual direction; convert it into a compact design specification and acceptance checklist.
3. Verify requirement/backlog cross-links and gate terminology.
4. Run the bounded auth/access-control and export spikes before any private data or media implementation.
5. Start implementation only after the human product owner approves Gate 1 evidence.

## Validation limitations

This review inspected current GitHub files and the recursive repository tree. It did not clone the repository, render SVG/Mermaid in a browser, run automated link/ID checks, execute an application, or verify GitHub protection settings. No application code, test suite, provider integration or deployment was validated.
