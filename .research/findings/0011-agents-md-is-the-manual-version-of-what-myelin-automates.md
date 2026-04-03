---
id: '0011'
title: AGENTS.md is the manual version of what myelin automates
status: open
evidence: CONFIRMED
sources:
- text: 'addyosmani.com/blog/self-improving-agents/ (content_hash:29263f70)'
  tier: PRIMARY
- text: 'medium.com/@addyosmani/stop-using-init-for-agents-md (content_hash:2454d556)'
  tier: PRIMARY
- text: 'ericmjl.github.io/blog/2026/1/17/how-to-build-self-improving-coding-agents-part-1/
    (content_hash:e6174e77)'
  tier: PRIMARY
created: '2026-04-03'
disconfirmation: 'Searched for evidence that auto-generated AGENTS.md helps. Found
  the opposite: Osmani cites research showing /init-generated files hurt performance
  2-3%. Manual, iterative AGENTS.md growth works; automated generation without curation
  does not. This supports myelin''s human-in-the-loop activation gate.'
---

## Claim

AGENTS.md (Linux Foundation) is the manual version of what myelin automates. Key finding from Addy Osmani: LLM-generated context files (via /init) REDUCED task success by 2-3% while increasing costs 20%+. Only include what agents can't discover by reading code: tool specs, non-obvious conventions, operational constraints. AGENTS.md should grow through iteration not upfront planning, and failure modes include anchoring bias, information decay, and monolithic context waste. Eric Ma: 'model weights don't change mid-week — improvement comes from changing the environment.' Myelin automates this environmental improvement.

## Supporting Evidence

> **Source [SECONDARY]:** addyosmani.com/blog/self-improving-agents/ + agents.md specification, retrieved 2026-04-03

## Disconfirmation Search

Searched for evidence that auto-generated AGENTS.md helps. Found the opposite: Osmani cites research showing /init-generated files hurt performance 2-3%. Manual, iterative AGENTS.md growth works; automated generation without curation does not. This supports myelin's human-in-the-loop activation gate.

## Caveats

None identified yet.
