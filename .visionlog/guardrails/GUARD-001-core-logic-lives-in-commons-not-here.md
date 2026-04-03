---
id: "GUARD-001"
type: "guardrail"
title: "Core logic lives in commons, not here"
status: "active"
date: "2026-04-03"
---

Distillation, tactics storage, and user model modules belong in claude-session-commons. eidos-myelin is the front door (MCP server + CLI) — same pattern as resume-resume. Never duplicate commons functionality.
