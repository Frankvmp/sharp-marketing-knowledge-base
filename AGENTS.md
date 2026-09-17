---
title: Agent instructions
description: How to navigate this repository as a read-only marketing knowledge wiki.
---

# Agent instructions

This repository is a portable, read-only marketing knowledge wiki: plain Markdown files linked to each other. **No server, MCP connection, or installed tool of any kind is required or expected.** Open the repository (locally, via `git clone`, or through the GitHub UI/API) and navigate by reading files and following the relative links inside them, the same way you would follow links in an online wiki.

## Where to start

1. [`index.md`](./index.md) — the repository's front door.
2. [`knowledge/index.md`](./knowledge/index.md) — the table of contents for the corpus: one entry per chapter, plus a set of cross-chapter records.
3. [`knowledge/cross-chapter-authority-map.md`](./knowledge/cross-chapter-authority-map.md) — start here instead when a question could span more than one chapter or concept. It names the preferred detailed record for overlapping topics.

From either starting point, follow `[text](./path.md)`-style links to move between documents. Every chapter folder (`knowledge/chapter-NN-*/`) has its own `index.md` listing that chapter's concept files.

## How one knowledge file is structured

Every file under `knowledge/` carries YAML frontmatter followed by a body with a predictable shape. This is the whole contract — there is no external schema or app to consult:

- **Frontmatter**: `type`, `title`, `description`, `tags`, and a `sources` entry (`id` plus an internal `resource` link — never an external URL or named work).
- **Core statement / Definitions** — the concept in plain terms.
- **Mechanism and relationships** — how it works and what it connects to.
- **Evidence and data requirements**, **Conditions and limits** — what supports the claim and where it stops applying.
- **Decision implications** — bounded, conditional next actions.
- **Related** — links to sibling concept files worth reading next. Follow these to explore adjacent knowledge.
- Numbered footnotes at the bottom (e.g. `[^mechanism]`) cite the file named in `sources[].resource`, with a chapter/page locator. The source's bibliographic identity is intentionally not disclosed anywhere in this release — locators exist only as internal traceability.

## Checking the wiki holds together (linting)

There is no bundled linter or app dependency. To check the wiki is well-formed, an agent or script needs only three things, all checkable by reading plain text:

1. Every `.md` file under `knowledge/` has frontmatter with at least `type`, `title`, and `description`.
2. Every relative Markdown link (`[text](./path.md)`) resolves to a file that actually exists in the repository.
3. Every footnote reference in a file's body (`[^id]`) has a matching `[^id]: ...` definition in that same file.

A quick manual spot-check when in doubt: open the linked target and confirm it exists and is itself a knowledge file with frontmatter — the same way you'd verify any wiki link.

## What counts as knowledge, and what doesn't

Only files under `knowledge/` are approved marketing evidence. `index.md` and this file are navigation aids, not evidence — do not cite them as a source for a marketing claim.

## Answering a question

1. Identify the concept(s) the question touches. Use the chapter index or the cross-chapter authority map to find the right starting file(s).
2. Read the detailed concept file(s), and follow `Related` links when the question spans more than one concept.
3. Separate what the retrieved record actually supports from your own inference, and say so.
4. Name the specific file(s) you used when giving a substantive answer.
5. If the corpus doesn't support an answer, say that plainly rather than filling the gap from general knowledge.
