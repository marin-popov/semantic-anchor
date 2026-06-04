# Changelog — Semantic Anchor Standard

## 1.1 — 04.06.2026
- Refined JSON‑LD reference architecture following a technical peer review and validation audit by [Álvaro Pichó Torres](https://www.linkedin.com/in/alvaropicho/).
- Implemented the "Mirror Property Pattern" (`worksFor` → `Role` → `worksFor`) to resolve Schema.org domain/range conflicts, ensuring 100% deterministic adherence for all parsers.
- Re-anchored the primary identity by reordering the `worksFor` array to place the current Role in the first position, establishing a circular authority link to the Organization `@id`.
- Standardized commercial nodes by wrapping `Service` entities in `Offer` types and replacing `workExample` with `subjectOf` to achieve a zero-error validation state.
- Sanitized UTF-8 encoding artifacts (—, €, ó) across the reference implementation to maximize machine-readability and signal-to-noise ratio.
- Deployed v1.1 refinements to the live reference implementation at [1euroseo.com/identity.jsonld](https://1euroseo.com/identity.jsonld) to serve as the production-ready proof of concept.
- Renamed original v1.0 identity file to `canonical-identity-v1.0.jsonld` to preserve technical provenance.

## 1.0 — 07.04.2026
- Initial publication of the Semantic Anchor specification.
- Defined the Identity Gap problem.
- Introduced the `Identity:` header for llms.txt.
- Added minimal JSON‑LD identity requirements.
- Published example llms.txt and identity.jsonld files.
