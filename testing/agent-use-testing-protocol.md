---
type: Agent-Use Test Protocol
title: Agent-use testing protocol
description: A repeatable way to observe how an agent retrieves and reasons from this reader release.
status: draft
tags: [testing, agent-use, reader-release]
generated:
  by: codex/gpt-5
---

# Agent-use testing protocol

## Purpose

Use this protocol to test how an agent uses the reader release when a human asks an open-ended, real-world question. It does not score a predetermined answer.

## Procedure

1. Start a fresh agent session connected to this release.
2. Confirm the connection using the [connection guide](../setup/connection-guide.md).
3. Give the agent the human's question and require it to follow the [agent-use contract](../setup/agent-use-contract.md).
4. Save the unedited response outside this release.
5. Record the agent host, provider, visible model identifier, date, and release version.
6. Assess the response later against a behavioural rubric; do not place hidden scoring criteria in this release.

## Minimum response record

- Human question
- Agent host and provider
- Visible model identifier, or `unknown`
- Reader-release version
- Full agent response
- Records and passage locators cited by the agent
- Any connection or retrieval issue observed

## Integrity boundary

Test prompts may be shared with the agent. Human feedback, scoring rubrics, evaluator notes, and comparative analyses must remain outside this reader release.