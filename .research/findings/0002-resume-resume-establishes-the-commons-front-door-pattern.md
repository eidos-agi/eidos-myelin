---
id: '0002'
title: 'resume-resume establishes the commons front-door pattern'
status: open
evidence: LOW
sources:
- text: 'resume-resume repo — imports from claude_session_commons for all data operations'
  tier: SECONDARY
created: '2026-04-03'
---

## Claim

resume-resume is an MCP server + TUI wrapping commons' discovery, parsing, and summarization. It contains no core logic — it's a front door. eidos-myelin should follow the same architecture: core distillation in commons, MCP+CLI in eidos-myelin.

## Supporting Evidence

> **Source [SECONDARY]:** resume-resume repo — imports from claude_session_commons for all data operations, retrieved 2026-04-03

## Caveats

None identified yet.
