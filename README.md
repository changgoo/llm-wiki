# LLM Wiki

This repository is a starter kit for an LLM-maintained personal wiki.

The basic pattern is:

1. Put immutable source material in `raw/sources/`.
2. Ask an LLM agent to ingest one source at a time.
3. The agent writes and maintains structured pages in `wiki/`.
4. The agent keeps `wiki/index.md` and `wiki/log.md` current.

The source of truth is always the raw source collection. The wiki is a persistent, compiled knowledge layer built from those sources.

## Repository Layout

```text
raw/
  sources/      Immutable documents, articles, transcripts, notes, and data.
  assets/       Images and other attachments referenced by raw sources.
wiki/
  index.md      Content-oriented catalog of wiki pages.
  log.md        Append-only chronological activity log.
  overview.md   Current high-level map of the knowledge base.
  sources/      One summary page per ingested source.
  entities/     People, organizations, places, products, and other named things.
  concepts/     Ideas, themes, frameworks, and recurring topics.
  questions/    Filed answers to user questions.
  syntheses/    Higher-level analyses that combine multiple sources.
tools/          Optional helper scripts, added only when needed.
```

## How To Use

Add a source file to `raw/sources/`, then ask the agent:

```text
Ingest raw/sources/example.md into the wiki.
```

For questions, ask against the wiki:

```text
Using the wiki, what are the main unresolved tensions in this topic?
```

If the answer is worth preserving, ask the agent to file it as a page under `wiki/questions/` or `wiki/syntheses/`.

## Agent Instructions

`AGENTS.md` defines the operating rules for maintaining the wiki. Update it as your workflow evolves.

