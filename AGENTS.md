# LLM Wiki Agent Instructions

This repository is an LLM-maintained wiki. The human curates sources and asks questions. The agent maintains the wiki.

## Core Principles

- Treat `raw/` as immutable source material. Read from it, but do not edit it unless the user explicitly asks.
- Treat `wiki/` as the maintained knowledge layer. Create, update, cross-link, and reorganize pages there as needed.
- Prefer source-backed claims. If a claim comes from a source, cite the relevant source page or raw file.
- Preserve uncertainty. Mark contradictions, weak evidence, and open questions instead of smoothing them over.
- Keep pages useful for future sessions. Cross-link aggressively, update summaries, and maintain indexes.
- Keep changes scoped to the current ingest, query, or lint task.

## Directory Conventions

```text
raw/
  sources/      Immutable source documents.
  assets/       Images, PDFs, and other source attachments.
wiki/
  index.md      Content catalog maintained on every wiki update.
  log.md        Append-only chronological log.
  overview.md   High-level map and current state of the wiki.
  sources/      Source summary pages.
  entities/     Named entities.
  concepts/     Concepts, themes, and recurring topics.
  questions/    Preserved answers to user questions.
  syntheses/    Multi-source analyses and higher-level summaries.
```

## Naming Rules

- Use lowercase kebab-case filenames: `example-topic.md`.
- Use descriptive page titles in H1 headings: `# Example Topic`.
- Prefer singular names for entity and concept pages.
- Avoid renaming existing pages unless there is a clear benefit. If renaming, update all wiki links.
- Use Obsidian-style internal links where useful: `[[concept-name]]`.
- Markdown links to raw files are also acceptable when citing source material.

## Page Frontmatter

Use YAML frontmatter for maintained wiki pages:

```yaml
---
type: source | entity | concept | question | synthesis | overview
status: seed | active | partial | stale
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources:
  - wiki/sources/example-source.md
tags:
  - example
---
```

For source summary pages, include the raw source path:

```yaml
raw_source: raw/sources/example.md
```

## Source Summary Template

```markdown
---
type: source
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
raw_source: raw/sources/example.md
tags: []
---

# Source Title

## Summary

Briefly explain what the source says and why it matters.

## Key Claims

- Claim with citation or raw-source reference.

## Notable Details

- Important facts, examples, definitions, or evidence.

## Connections

- Related entity: [[entity-name]]
- Related concept: [[concept-name]]

## Tensions And Contradictions

- Note conflicts with existing wiki pages or earlier sources.

## Open Questions

- Questions raised by this source.
```

## Entity Page Template

```markdown
---
type: entity
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: []
tags: []
---

# Entity Name

## Snapshot

One-paragraph summary.

## Known Facts

- Fact with source link.

## Relationships

- Related entities, concepts, events, or sources.

## Timeline

- YYYY-MM-DD: Event or update.

## Open Questions

- Unknowns or claims needing better support.
```

## Concept Page Template

```markdown
---
type: concept
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: []
tags: []
---

# Concept Name

## Definition

Short working definition.

## Why It Matters

Explain its role in the knowledge base.

## Supporting Evidence

- Evidence or example with source link.

## Related Pages

- [[related-page]]

## Open Questions

- Questions to investigate.
```

## Question Page Template

```markdown
---
type: question
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: []
tags: []
---

# Question

## Answer

Direct answer synthesized from the wiki.

## Evidence

- Source-backed point.

## Caveats

- Uncertainties, contradictions, or missing sources.

## Follow-Up Questions

- Useful next questions.
```

## Synthesis Page Template

```markdown
---
type: synthesis
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: []
tags: []
---

# Synthesis Title

## Thesis

The current best synthesis.

## Main Points

- Cross-source point with links.

## Contradictions Or Tensions

- Where sources disagree or imply different conclusions.

## Implications

- What this changes about the wiki's broader understanding.

## Related Pages

- [[related-page]]
```

## Ingest Workflow

When the user asks to ingest a source:

1. Read the raw source from `raw/sources/`.
2. Read `wiki/index.md`, `wiki/overview.md`, and any obviously related wiki pages.
3. Create or update a source summary page in `wiki/sources/`.
4. Create or update relevant entity, concept, question, or synthesis pages.
5. Add cross-links between affected pages.
6. Update `wiki/index.md`.
7. Update `wiki/overview.md` if the source changes the high-level understanding.
8. Append an entry to `wiki/log.md`.
9. Report which pages changed and call out unresolved questions or contradictions.

## Query Workflow

When answering a question against the wiki:

1. Read `wiki/index.md` first.
2. Read relevant wiki pages.
3. Search the wiki if needed.
4. Answer with links to supporting wiki pages and raw sources where appropriate.
5. If the answer is reusable, offer to file it under `wiki/questions/` or `wiki/syntheses/`.

## Lint Workflow

When asked to lint or health-check the wiki, look for:

- broken internal links
- orphan pages
- missing entries in `wiki/index.md`
- pages without sources
- stale pages that conflict with newer sources
- important concepts mentioned repeatedly without their own page
- contradictions that should be called out explicitly
- unanswered questions worth pursuing

Append a lint entry to `wiki/log.md` if files are changed.

## Index Rules

`wiki/index.md` is content-oriented. Keep it organized by page type. Each entry should include:

- link
- one-line summary
- status when useful
- source count when useful

Update it whenever pages are added, removed, renamed, or materially changed.

## Log Rules

`wiki/log.md` is chronological and append-only. Use this heading format:

```markdown
## [YYYY-MM-DD] ingest | Source Title
## [YYYY-MM-DD] query | Question
## [YYYY-MM-DD] lint | Scope
```

Each entry should briefly list changed pages and key outcomes.

