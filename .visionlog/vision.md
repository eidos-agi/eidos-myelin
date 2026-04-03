---
title: "Make Claude Code smarter through experience"
type: "vision"
date: "2026-04-03"
---

eidos-myelin is the tactical intelligence front door for claude-session-commons. It distills cross-session patterns into learned knowledge — tactics, anti-patterns, and user behavioral models — and surfaces them when they matter.

The biological metaphor: myelin doesn't create new neurons. It insulates existing pathways so signals travel faster. Same Claude Code, same tools — but the pathways that work get reinforced and the ones that don't get pruned.

Architecture: core distillation logic lives in claude-session-commons as new modules (distill.py, tactics.py, user_model.py). eidos-myelin is the MCP server + CLI that exposes it — same pattern as resume-resume wraps commons' discovery/parsing into MCP tools and a TUI.

Three kinds of learned knowledge:
1. **Tactics** — cross-session patterns that consistently work. Confidence-scored, scoped (global/project), decay without reinforcement.
2. **Anti-patterns** — things to stop doing. From high-effort/low-progress sessions, user corrections, repeated failures.
3. **User model** — behavioral profile predicting productive sessions. Not biographical (memory handles that). Transparent, editable, resettable.
