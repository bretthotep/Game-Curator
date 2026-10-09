# Artwork categories, precedence, and moderation policy

**Status:** Proposed content/IP policy; no artwork provider or community submission workflow exists.

## Separate media categories

1. **Personal photographs** document a collector's actual physical copy. Private by default; public use requires an explicit, separate user action and clear visibility explanation.
2. **Catalogue default artwork** is an approved image with documented source/rights and attribution.
3. **GameCurator-generated interpretation** is original artwork inspired by verified metadata/themes/genres/descriptions. It must not deliberately reproduce covers, logos, distinctive characters, or promotional artwork as a substitute for licensed images. Cache approved output; generation is not mandatory for MVP.
4. **Community-submitted artwork** is not publicly distributed until rights attestation, screening, human moderation where needed, and approval are complete.

Do not treat user uploads or an automated similarity/screening result as proof of copyright ownership. Provide reporting, takedown, review queues, rate limits, audit history, and a human escalation path for uncertainty/disputes. Obtain legal guidance for repeat infringement and takedown policy.

## Catalogue-view fallback precedence

For a public/catalogue game or release card:

1. Approved community favourite, only while approval and rights status remain valid.
2. Approved GameCurator-generated default.
3. Licensed/otherwise authorized catalogue default artwork, if an applicable source/permission is documented.
4. Neutral branded placeholder while the catalogue entry is incomplete.

Personal photos are never a catalogue fallback. If no approved source exists, use the neutral placeholder rather than an unlicensed cover.

## Personal collection-card precedence

1. The collector's explicitly selected personal photo for that specific copy, while the photo remains available and the collector has not withdrawn it.
2. The catalogue-view fallback result for its linked game/release (approved community favourite, generated default, documented licensed image, then placeholder).

A vote cannot change or replace the personal selection. A missing/unavailable photo falls through without deleting the collector's preference/record; offer a clear replacement action. Never publish the personal photo merely because the collection or a catalogue artwork entry is public.

## Provider boundary and lifecycle

Keep generation and external image retrieval behind replaceable interfaces. Record source/creator, rights attestation/permission basis, attribution, moderation status, visibility, version, dates, and takedown state. Cache only where rights permit. Do not make expensive generation or catalogue imagery a mandatory MVP dependency.
