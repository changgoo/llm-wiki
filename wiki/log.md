---
type: log
status: active
created: 2026-05-14
updated: 2026-05-14
tags:
  - log
---

# Log

This is the chronological activity log for the wiki. Entries are append-only.

## [2026-05-14] scaffold | Initial wiki structure

Created the initial LLM Wiki operating structure:

- `AGENTS.md`
- `README.md`
- `raw/sources/`
- `raw/assets/`
- `wiki/index.md`
- `wiki/log.md`
- `wiki/overview.md`
- `wiki/sources/`
- `wiki/entities/`
- `wiki/concepts/`
- `wiki/questions/`
- `wiki/syntheses/`
- `tools/`

## [2026-05-14] ingest | Ruszkowski and Pfrommer 2023 cosmic ray feedback

Ingested `raw/sources/Ruszkowski and Pfrommer - 2023 - Cosmic ray feedback in galaxies and galaxy clusters.pdf`.

Created:

- [[ruszkowski-pfrommer-2023-cosmic-ray-feedback]]
- [[cosmic-rays]]
- [[cosmic-ray-feedback]]
- [[cosmic-ray-transport]]
- [[galactic-winds]]
- [[circumgalactic-medium]]
- [[agn-feedback]]

Updated:

- [[index]]
- [[overview]]

Key outcome: the wiki scope is now seeded around cosmic ray feedback in galaxies and galaxy clusters, with cosmic ray transport identified as the central uncertainty.

## [2026-05-14] query | Clarify wiki scope for astrophysics research

Updated the wiki scope from a cosmic-ray-feedback-specific knowledge base to a broader astrophysics research wiki seeded by cosmic ray feedback.

Created:

- [[astrophysics]]

Updated:

- [[index]]
- [[overview]]

Key outcome: future ingests can cover astrophysics topics beyond cosmic ray feedback without requiring a separate wiki, as long as they fit the broader astrophysics research context.

## [2026-05-14] maintenance | PDF text extraction rule

Added a workflow rule: before ingesting any PDF, convert it with `pdftotext -layout` and save the `.txt` companion in `raw/sources/`.

Updated:

- `AGENTS.md`
- [[ruszkowski-pfrommer-2023-cosmic-ray-feedback]]

Created raw companion text:

- `raw/sources/papers/Ruszkowski and Pfrommer - 2023 - Cosmic ray feedback in galaxies and galaxy clusters.txt`

## [2026-05-14] ingest | My papers bibliography

Ingested `raw/sources/mypapers.bib` at the metadata level after removing two non-astrophysics CFD/renewable-energy entries. The cleaned bibliography contains 72 astrophysics publications with abstracts and keywords.

Created:

- [[mypapers-bibliography]]
- [[publication-map]]
- [[publication-ingest-plan]]
- [[multiphase-ism]]
- [[tigress]]
- [[stellar-feedback]]
- [[star-formation-regulation]]
- [[supernova-feedback]]
- [[observational-ism-diagnostics]]

Updated:

- [[index]]
- [[overview]]
- [[ruszkowski-pfrommer-2023-cosmic-ray-feedback]]
- `.gitignore`

Key outcome: the bibliography is grouped into seven planned full-text ingest batches, ready to match against PDF locations later.
