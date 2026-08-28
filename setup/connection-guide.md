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

`Byron-Sharp-Marketing-book-KB-reader-release`

The project includes local OpenKnowledge MCP configuration. Approve or enable that configuration in the agent host if the host asks.

## Connection procedure

1. Open this release directory in the chosen agent environment.
2. Enable the project's OpenKnowledge MCP server configuration.
3. Confirm that the agent can use OpenKnowledge search and document-reading tools.
4. Give the agent the [agent-use contract](./agent-use-contract.md), or tell it to read that document before answering.
5. Run the connection check below.

## Connection check

Ask the agent:

> Read `release-information/release-manifest.md` and retrieve the approved record that explains mental availability in choice situations. Report the release version, the record path, and one limit stated in that record.

A successful check names release version `0.1.0-draft`, retrieves from `knowledge/`, and does not attempt to read source, construction, or evaluation material.

## If connection fails

Confirm that the agent host supports MCP, that the local project configuration is enabled, and that the agent is opened in this release directory. Do not point the agent at the private construction workspace as a workaround.