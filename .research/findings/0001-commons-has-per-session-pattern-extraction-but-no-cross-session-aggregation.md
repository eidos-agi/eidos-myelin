---
id: '0001'
title: 'commons has per-session pattern extraction but no cross-session aggregation'
status: open
evidence: LOW
sources:
- text: 'claude-session-commons source code — summarize.py:analyze_patterns()'
  tier: SECONDARY
created: '2026-04-03'
---

## Claim

claude-session-commons v0.1.0 has analyze_patterns() extracting prompt_patterns, workflow_patterns, anti_patterns, and key_lesson per session. No cross-session clustering, promotion, or scoring exists.

## Supporting Evidence

> **Source [SECONDARY]:** claude-session-commons source code — summarize.py:analyze_patterns(), retrieved 2026-04-03

## Caveats

None identified yet.
