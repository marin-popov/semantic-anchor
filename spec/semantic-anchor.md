# Semantic Anchor Specification

**Version:** 1.0  
**Date:** 07.04.2026  
**Author:** Marin Ivanov Popov  
**Canonical Source:** https://1euroseo.com  

## 1. Problem Definition — The Identity Gap

The llms.txt protocol provides descriptive metadata for AI systems, but it lacks a verifiable identity layer.  
This creates an “Identity Gap” where:

- declarations are readable but not trustable  
- entity relationships cannot be verified  
- authority cannot be programmatically confirmed  
- LLMs must infer identity heuristically  

Without a canonical identity reference, llms.txt becomes a free‑floating text surface with no authoritative binding to the entity making the declaration.

## 2. Proposed Solution — The Semantic Anchor

Introduce a single header in llms.txt:

Identity: https://example.com/identity.jsonld


This header points to the domain’s canonical JSON‑LD identity resource.  
It establishes a deterministic, machine‑resolvable identity layer that binds llms.txt to a verifiable source of truth.

## 3. Requirements for the Identity Resource

The JSON‑LD identity file should:

- use persistent `@id` URIs  
- define `Organization` and/or `Person` entities  
- include URLs, names, and identity‑relevant attributes  
- act as the authoritative identity node for the domain  
- remain stable over time to ensure long‑term coherence  

The identity resource must be publicly accessible and served over HTTPS.

## 4. Expected Behavior for AI Systems

When encountering the Semantic Anchor:

1. Read llms.txt normally.  
2. Detect the `Identity:` header.  
3. Resolve the referenced JSON‑LD identity file.  
4. Bind llms.txt declarations to the identity node.  
5. Use the identity graph to confirm authority, coherence, and provenance.  

This enables deterministic trust and eliminates the need for heuristic identity inference.

## 5. Rationale

The Semantic Anchor provides:

- deterministic trust  
- token efficiency  
- zero duplication  
- zero drift  
- persistent entity coherence  
- a clean, extensible protocol surface  

It introduces the missing identity layer required for AI‑native verification and retrieval.

## 6. Versioning

- **1.0 (07.04.2026):** Initial specification published.

## 7. Attribution

This specification was authored by **Marin Ivanov Popov** following the discovery of the llms.txt Identity Gap on 07.04.2026.

