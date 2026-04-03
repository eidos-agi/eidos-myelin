---
title: 'Commons-first with human gate'
verdict: provisional
---

## What It Is

Core distillation in commons (distill.py, tactics.py, user_model.py). Daemon runs distillation after indexing. All tactics start as DRAFT. Human must approve via `myelin review` CLI to activate. eidos-myelin is MCP server + CLI front door only. Feedback loop via tactic_feedback() closes the self-improvement cycle. Anti-patterns prioritized over positive tactics (finding 0017). Max 5 items at boot. Tactic schema: {id, scope, type, claim, conditions, evidence_sessions, confidence, lifecycle, created, last_seen}.

## Validation Checklist

- [ ] Claim 1: Y — finding 0002: resume-resume already imports commons for all data ops. Same pattern works. claude-boss can surface tactics in orchestration context.
- [x] Human curation gate prevents the -3% AGENTS.md failure mode (finding 0015): Y — finding 0015 CONFIRMED: auto-generated context hurts -3%, human-written helps +4%. Human gate is the proven differentiator.
- [ ] Core modules in commons can be reused by resume-resume and claude-boss: Y — finding 0018: tactic_feedback(id, worked) closes the loop. Activation/rejection rates calibrate thresholds. Meta-tactics about myelin's own effectiveness emerge naturally.
- [x] Feedback loop enables self-improvement of distillation quality over time: Y — finding 0018: tactic_feedback(id, worked) closes the recursive loop. Activation/rejection rates self-calibrate thresholds.
- [ ] Daemon extension adds minimal operational complexity vs new daemon: Y — commons daemon already polls every 5 min. Distillation is one more pass after indexing. No new process, no new config.

## Scoring
## Scores

| Criterion | Score |
|-----------|-------|
| correctness | 9/10 |
| implementation_effort | 8/10 |
| self_improvement | 9/10 |
| safety | 10/10 |
| ecosystem_fit | 10/10 |
| **Total** | **46** |

**Notes:** Strongest on safety (human gate proven by finding 0015) and ecosystem fit (reuses daemon, DB, same pattern as resume-resume). Self-improvement enabled by feedback loop (finding 0018). Only weakness: human bottleneck slows initial learning — but research shows this is a feature, not a bug.
