---
id: "ADR-001"
type: "decision"
title: "ADR-001: Commons-first with human gate"
status: "proposed"
date: "2026-04-03"
---

## Decision

Core distillation modules (distill.py, tactics.py, user_model.py) live in claude-session-commons. eidos-myelin is the MCP server + CLI front door. All tactics require human approval to activate.

## Context

18 research findings, 3 candidates scored against 5 weighted criteria. GPT-5.2 peer review.

## Rationale

Scored 46/50, beating auto-promote (37) and standalone (31).

The decisive evidence is finding 0015 (CONFIRMED, ETH Zurich + 2 studies): auto-generated context files reduce task success by 2-3% while increasing costs 20%+. Human-written context improves success by 4%. The human gate separates the +4% outcome from the -3% outcome.

## Consequences

- G1: Add distill.py, tactics.py, user_model.py to claude-session-commons
- G2: eidos-myelin is MCP server + CLI only (same pattern as resume-resume)
- Daemon distillation runs after indexing, no new process
- Tactics table in existing insights.db
- Anti-patterns prioritized over positive tactics (finding 0017)
- Max 5 items surfaced at boot (GUARD-005)
- tactic_feedback() enables recursive self-improvement (finding 0018)

## Rejected Alternatives

- **Auto-promote**: directly contradicts finding 0015. Valid V2 path after feedback loop proves safe tactic types.
- **Standalone package**: over-engineering for single-user scale. Duplicate daemon/DB/config not justified.
