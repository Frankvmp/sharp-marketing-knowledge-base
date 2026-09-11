---
type: Agent Use Contract
title: Agent-use contract for the reader release
description: Retrieval, reasoning, and read-only rules for agents using this knowledge base.
status: draft
tags: [agent-use, retrieval, read-only, provenance]
generated:
  by: codex/gpt-5
---

# Agent-use contract for the reader release

## Permitted knowledge access

Use OpenKnowledge tools to search and read only the [approved knowledge corpus](../knowledge/). Start with the [cross-chapter authority map](../knowledge/cross-chapter-authority-map.md) when a question could match more than one record.

Do not read outside `knowledge/` to answer a marketing question. Root-level `release-information/`, `setup/`, `testing/`, and `portable-skill/` provide administration, operating instructions, tests, and installation material. They are not evidence for marketing claims. [Source provenance](../knowledge/release-information/source-provenance.md) is inside `knowledge/` so source identity and limits remain accessible.

## Prohibited actions

Do not edit, create, delete, move, or propose edits to knowledge records. Do not use web search, external sources, native filesystem retrieval, source documents, construction materials, or evaluation materials to supplement an answer based on this release.

## Answer standard

For a substantive answer:

1. Answer the question directly.
2. Identify the detailed knowledge records used, with paths and any cited passage locators available in them.
3. Separate source-backed statements from inference.
4. State material limits and unknowns.
5. Give a bounded next action only when the retrieved knowledge supports one.

Do not invent source claims, citations, page references, facts about the user's situation, or human verification.

## Retrieval standard

Prefer detailed chapter records for mechanisms, conditions, procedures, and source support. Use navigation summaries only for orientation or where the authority map identifies them as a cross-chapter synthesis.

If the corpus does not support an answer, say so plainly.

## Release-candidate and skill context

This contract applies to version `0.1.0-rc1`, derived from source tag `reader-release-v0.1.0-draft` at source commit `8b8c8c4be24c849bb5c711b790e39b6dbfe14f72`.

Install and use `portable-skill/marketing-kb-grounded-reasoning.zip` alongside this contract. Its reference to outside-tool permission does not authorize outside evidence for an answer based on this release; the prohibited actions above still apply.

The package includes `release-manifest.json`, `SHA256SUMS`, and `release-verification.json`. No public URL or credentials are supplied; deployment and final approval remain pending. The read-only access policy is not a claim that unrestricted `exec` is safe.
