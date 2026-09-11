---
type: Connection Guide
title: Connect an agent to this reader release
description: Provider-neutral procedure for connecting an MCP-capable agent to the local read-only release.
status: draft
tags: [mcp, setup, reader-release]
generated:
  by: codex/gpt-5
---

# Connect an agent to this reader release

## Before starting

Open this directory as the agent's project or workspace:

`Byron-Sharp-Marketing-book-KB-reader-release-v0.1.0-rc1`

The project includes local OpenKnowledge MCP configuration. Approve or enable that configuration in the agent host if the host asks.

This release candidate was validated with OpenKnowledge `0.68.24`. Its `npx` fallback is pinned to that version so a later package update cannot silently change the tested behavior.

## Connection procedure

1. Open this release directory in the chosen agent environment.
2. Enable the project's OpenKnowledge MCP server configuration.
3. Confirm that the agent can use OpenKnowledge search and document-reading tools.
4. Give the agent the [agent-use contract](./agent-use-contract.md), or tell it to read that document before answering.
5. Install `portable-skill/marketing-kb-grounded-reasoning.zip` using the chosen host's normal skill-install process.
6. Confirm that OpenKnowledge search returns only paths under `knowledge/`.
7. Run the connection check below.

## Connection check

Ask the agent:

> Read `release-information/release-manifest.md` and retrieve the approved record that explains mental availability in choice situations. Report the release version, the record path, and one limit stated in that record.

A successful check names release version `0.1.0-rc1`, retrieves from `knowledge/`, and does not attempt to read source, construction, or evaluation material.

## If connection fails

Confirm that the agent host supports MCP, that the local project configuration is enabled, that the portable skill is installed, and that the agent is opened in this release directory. Do not point the agent at the private construction workspace as a workaround.

## Release-candidate boundary

Version `0.1.0-rc1` derives from source tag `reader-release-v0.1.0-draft` at source commit `8b8c8c4be24c849bb5c711b790e39b6dbfe14f72`. Reading the release manifest for the connection check is an administrative step, not marketing retrieval.

This guide supplies no public URL or credentials. Deployment and final approval remain pending. Tool availability and a successful connection check do not establish that unrestricted `exec` is safe.
