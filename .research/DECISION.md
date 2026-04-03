# Decision

**Date:** 2026-04-03
**Status:** Decided
**ADR:** ADR-001

## Decision

Commons-first with human gate. Core distillation modules (distill.py, tactics.py, user_model.py) live in claude-session-commons. eidos-myelin is the MCP server + CLI front door. All tactics require human approval to activate. Auto-promote is a V2 upgrade path after the feedback loop proves which tactic types are safe to auto-activate.

## Rationale

Scored 46/50, beating auto-promote (37) and standalone (31).

The decisive evidence is finding 0015 (CONFIRMED, 3 sources): auto-generated context files reduce task success by 2-3% while increasing costs 20%+. Human-written context improves success by 4%. The human gate is not a bottleneck — it's the mechanism that separates the +4% outcome from the -3% outcome.

commons-human-gate wins on:
- Safety (10/10): human gate prevents the AGENTS.md failure mode
- Ecosystem fit (10/10): reuses existing daemon, DB, same pattern as resume-resume
- Correctness (9/10): only surfaces non-inferable knowledge (tool specs, constraints, anti-patterns per 0015)
- Self-improvement (9/10): tactic_feedback() closes the recursive loop (finding 0018)
- Implementation effort (8/10): 3 new modules in commons + thin MCP front door, no new daemon

Auto-promote rejected for V1 because finding 0015 directly shows auto-activation hurts. But it's a valid V2 path after the feedback loop identifies which tactic types have 95%+ acceptance rates.

Standalone rejected because at single-user scale (~20 repos, ~200 sessions), the operational overhead of a separate daemon, DB, and config system isn't justified. GPT-5.2's recommendation assumed multi-user scale we don't have yet.
