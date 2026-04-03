---
id: '0016'
title: 'Telemetry-first evaluation: traces are the source of truth for improvement
  claims'
status: open
evidence: REASONED
sources:
- text: 'arize.com/blog/closing-the-loop-coding-agents-telemetry (content_hash:b9d3de23)'
  tier: PRIMARY
created: '2026-04-03'
---

## Claim

Arize's framework establishes that coding agent improvement must be measured through traces (tool invocations, loop counts, failure points, timing). Without telemetry and evaluations on real traces, claiming a change is an improvement has no empirical basis. For myelin: the evaluation harness (G3) should extract session-level metrics from commons' existing parsed data — tool_call_count, user_correction_count, time_to_first_commit, retry_count — and compare sessions with vs without active tactics.

## Supporting Evidence

> **Source [PRIMARY]:** arize.com/blog/closing-the-loop-coding-agents-telemetry (content_hash:b9d3de23), retrieved 2026-04-03

## Caveats

None identified yet.
