---
okf_version: "0.2"
---

# Byron Sharp marketing knowledge-base reader release

This is version `0.1.0-rc1`, a read-only, portable release candidate of source-grounded marketing knowledge extracted from *Marketing: Theory, Evidence, Practice*, second edition.

Start with [Release overview](./release-information/release-overview.md). Agents should then follow the [agent-use contract](./setup/agent-use-contract.md) and retrieve only from the [approved knowledge corpus](./knowledge/index.md).

## Use

- [Connection guide](./setup/connection-guide.md)
- [Agent-use contract](./setup/agent-use-contract.md)
- [Release manifest](./release-information/release-manifest.md)
- [Source provenance](./knowledge/release-information/source-provenance.md)
- [Agent-use testing protocol](./testing/agent-use-testing-protocol.md)
- [Example prompts](./testing/example-prompts.md)

## Boundary

This release intentionally excludes source files, extraction materials, construction notes, semantic-audit working papers, and prior evaluation responses. It is not an editing workspace.

## Release-candidate status

The source tag is `reader-release-v0.1.0-draft`, at source commit `8b8c8c4be24c849bb5c711b790e39b6dbfe14f72`. OpenKnowledge search is restricted to `knowledge/`, including source provenance. Setup, testing, release administration, and the portable skill bundle remain outside searchable marketing.

Install `portable-skill/marketing-kb-grounded-reasoning.zip` in the agent host before testing. The release includes `release-manifest.json`, `SHA256SUMS`, and `release-verification.json` for machine-readable verification. No public URL or credentials are supplied; deployment and final approval remain pending. No claim is made that unrestricted `exec` is safe.
