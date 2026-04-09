# Semantic Anchor — Identity Layer Standard for llms.txt

The Semantic Anchor is a protocol‑level identity extension for the llms.txt standard.  
It resolves the structural “Identity Gap” identified on 07.04.2026 — the absence of a verifiable entity layer linking llms.txt declarations to a canonical source of truth.

## Purpose

llms.txt currently functions as a readable but unverifiable text surface.  
It describes content, but it does not prove *who* is making the declaration.

The Semantic Anchor introduces a single header that binds llms.txt to a canonical JSON‑LD identity resource, enabling:

- deterministic trust  
- token efficiency  
- persistent entity coherence  
- verifiable authority for AI systems  
- zero duplication and zero drift  

## The Header

