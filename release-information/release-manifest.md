---
type: Release Manifest
title: Reader release manifest
description: Version, corpus boundary, and compatibility information for this release.
status: draft
tags: [reader-release, version, manifest]
generated:
  by: codex/gpt-5
---

# Reader release manifest

| Field | Value |
| --- | --- |
| Release name | Byron Sharp marketing knowledge-base reader release |
| Release version | 0.1.0-rc1 |
| Release status | Release candidate; final approval pending |
| Source tag | reader-release-v0.1.0-draft |
| Source commit | 8b8c8c4be24c849bb5c711b790e39b6dbfe14f72 |
| Searchable root | knowledge/ |
| Portable skill | portable-skill/marketing-kb-grounded-reasoning.zip |
| Knowledge-record count | 130 |
| Source scope | *Marketing: Theory, Evidence, Practice*, second edition, Chapters 1–16 |
| Access mode | Read-only retrieval and reasoning |
| Required interface | OpenKnowledge MCP-compatible agent host |
| Human verification | Not claimed |
| Construction material | Excluded |
| Evaluation responses and rubrics | Excluded |

## Compatibility

An agent needs the OpenKnowledge MCP server configured for this directory. The project includes local MCP configuration. Follow the [connection guide](../setup/connection-guide.md) before use.

## Version reporting

When recording a test or a consequential answer, identify this release as `0.1.0-rc1`. Do not treat a release version as evidence of human verification.

## Search and package boundary

OpenKnowledge search is restricted to `knowledge/`, including [source provenance](../knowledge/release-information/source-provenance.md). Root-level `setup/`, `testing/`, and `release-information/` remain outside searchable marketing. They provide operating instructions and release records, not marketing evidence.

The portable skill is bundled as `portable-skill/marketing-kb-grounded-reasoning.zip`. It must be installed in the chosen agent host; it is not indexed as marketing knowledge.

## Verification artifacts

`release-manifest.json` defines the package boundary. `SHA256SUMS` records payload hashes. `release-verification.json` records the checks and their results. These files do not replace human release approval.

No public URL or credentials are supplied. Deployment and final approval remain pending. This release candidate makes no claim that unrestricted `exec` is safe.
