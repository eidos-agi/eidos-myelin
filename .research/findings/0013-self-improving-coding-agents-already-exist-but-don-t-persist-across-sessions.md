---
id: '0013'
title: 'Self-improving coding agents already exist but don''t persist across sessions'
status: open
evidence: CONFIRMED
sources:
- text: 'arxiv.org/abs/2504.15228 — A Self-Improving Coding Agent, ICLR 2025 (content_hash:4b1020d7)'
  tier: PRIMARY
- text: 'arize.com/blog/closing-the-loop-coding-agents-telemetry (content_hash:b9d3de23)'
  tier: PRIMARY
created: '2026-04-03'
disconfirmation: 'Searched for any system that does cross-session learning from real
  user coding sessions (not benchmarks). Found AGENTS.md pattern (manual), Reflexion
  (within-trial), A-Mem (within-session), Mem0 (conversational facts). None automate
  cross-session tactical distillation from coding agent transcripts. The gap is real.'
---

## Claim

Self-improving coding agents (ICLR 2025) achieve 17-53% improvement on SWE-Bench Verified through self-editing. But all operate within a single benchmark run. The cross-session gap remains: no system learns from a user's actual work history across weeks/months of sessions to make future sessions more productive. AGENTS.md is the closest but requires manual curation. The Arize telemetry approach is the most relevant: traces capture tool invocations, loop counts, failure points — same signals myelin needs. Key quote: 'Without telemetry, there is no source of truth. Without evaluations on real traces, there is no empirical basis for claiming a change is an improvement.'

## Supporting Evidence

> **Source [SECONDARY]:** arxiv.org/abs/2504.15228 — A Self-Improving Coding Agent (ICLR 2025), retrieved 2026-04-03

## Disconfirmation Search

Searched for any system that does cross-session learning from real user coding sessions (not benchmarks). Found AGENTS.md pattern (manual), Reflexion (within-trial), A-Mem (within-session), Mem0 (conversational facts). None automate cross-session tactical distillation from coding agent transcripts. The gap is real.

## Caveats

None identified yet.
