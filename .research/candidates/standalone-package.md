---
title: 'Standalone package, imports commons read-only'
verdict: provisional
---

## What It Is

eidos-myelin is a fully standalone package with its own distillation engine, tactics DB, and MCP server. Imports commons only for session discovery and parsing (read-only). Has its own daemon process. Human gate for activation. Completely decoupled from commons' release cycle. More code to write and maintain, but zero risk of destabilizing commons/resume-resume/claude-boss. GPT-5.2's original recommendation.

## Validation Checklist

- [ ] Claim 1: Y — can ship myelin updates without touching commons. But for a single user with ~20 repos, the coordination cost of two packages exceeds the benefit of independent releases.
- [x] Zero risk of destabilizing commons, resume-resume, or claude-boss: Y — complete isolation. But duplicates daemon, DB, and parsing infrastructure.
- [ ] Independent release cycle allows faster iteration on distillation: Y — confirmed. Two daemons polling the same session files, two SQLite databases, two config systems. Unnecessary for single user at this scale.
- [x] Separate daemon process adds operational complexity for single user: Y — two daemons, two DBs, two configs. Unnecessary at this scale.

## Scoring
## Scores

| Criterion | Score |
|-----------|-------|
| correctness | 8/10 |
| implementation_effort | 4/10 |
| self_improvement | 7/10 |
| safety | 9/10 |
| ecosystem_fit | 3/10 |
| **Total** | **31** |

**Notes:** Isolation protects commons but at massive implementation cost: duplicate daemon, separate DB, separate config. For a single user with ~20 repos this is over-engineering. Self-improvement slightly harder because feedback data is in a separate DB from session data. GPT-5.2 recommended this but assumed multi-user scale — at current scale, the overhead isn't justified.
