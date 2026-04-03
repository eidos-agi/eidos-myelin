---
title: 'Commons-first with auto-promote'
verdict: provisional
---

## What It Is

Same as commons-human-gate but tactics auto-promote to ACTIVE when confidence exceeds threshold (5+ supporting sessions, 2+ repos, 0 contradictions). No human gate for high-confidence tactics. Human review only for CANDIDATE-stage items below threshold. Faster learning loop but higher risk of garbage activation (finding 0015 warns against this). Feedback loop can auto-retire tactics that get negative feedback.

## Validation Checklist

- [ ] Claim 1: PARTIAL — finding 0006: diversity threshold helps but finding 0015 shows even high-quality auto-generated content hurts when it's redundant with what the agent already knows. Threshold prevents garbage but not redundancy.
- [x] Auto-promotion enables faster learning without human bottleneck: Y — but finding 0015 shows this is exactly the -3% failure mode. Speed vs safety tradeoff.
- [ ] High-confidence threshold (5+ sessions, 2+ repos, 0 contradictions) prevents garbage: Y — auto-retire is safe because it removes, not adds. Removing bad tactics can't make things worse. But the damage happens between activation and retirement.
- [x] Auto-retire via negative feedback prevents accumulation of bad tactics: Y — removal is safe. But damage occurs between auto-activation and auto-retirement.

## Scoring
## Scores

| Criterion | Score |
|-----------|-------|
| correctness | 6/10 |
| implementation_effort | 7/10 |
| self_improvement | 10/10 |
| safety | 4/10 |
| ecosystem_fit | 10/10 |
| **Total** | **37** |

**Notes:** Fastest self-improvement loop but directly contradicts finding 0015 (auto-generated context hurts -3%). The auto-promote threshold prevents garbage but not redundancy. Auto-retire helps but damage occurs between activation and retirement. Same ecosystem fit as commons-human-gate. Could be a V2 upgrade path after the human gate proves which tactics are worth auto-promoting.
