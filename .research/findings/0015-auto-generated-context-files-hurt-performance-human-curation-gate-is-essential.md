---
id: '0015'
title: 'Auto-generated context files hurt performance — human curation gate is essential'
status: open
evidence: CONFIRMED
sources:
- text: 'arxiv.org/html/2602.11988v1 — Evaluating AGENTS.md, ETH Zurich (content_hash:c1a2abfb)'
  tier: PRIMARY
- text: 'arxiv.org/html/2601.20404v1 — On the Impact of AGENTS.md Files (content_hash:447b9490)'
  tier: PRIMARY
- text: 'infoq.com/news/2026/03/agents-context-file-value-review/ (content_hash:9599849d)'
  tier: SECONDARY
created: '2026-04-03'
disconfirmation: 'Searched for evidence that auto-generated context always helps.
  Found the opposite: ETH Zurich shows LLM-generated files hurt when docs exist. But
  also found the second study showing human-written files DO help on efficiency (-28%
  wall time, -20% tokens). And practitioner feedback that proprietary codebases benefit
  more than open-source. The truth is nuanced: context helps when it''s non-redundant,
  human-curated, and minimal. This directly shapes myelin''s design constraints.'
---

## Claim

Two empirical studies on AGENTS.md reveal a nuanced picture critical for myelin's design:

ETH Zurich (arxiv 2602.11988, AGENTbench 138 tasks, 4 agents including Claude Code): LLM-generated context files reduce success by 2-3% and increase costs 20%+. Human-written files improve success by 4% but ALSO increase costs 19%. Key finding: when docs are removed, LLM-generated files HELP (+2.7%) — the problem is redundancy, not content quality. Tool specifications are the #1 helpful content type (usage jumped from &lt;0.01 to 1.6x when tools mentioned). Codebase overviews didn't help at all.

Second study (arxiv 2601.20404, Codex on 124 PRs): With AGENTS.md, wall-clock time decreased 28.6%, output tokens decreased 20%. Benefits concentrated in high-cost runs, not uniform.

Practitioner nuance: For proprietary codebases with legacy constraints and undocumented decisions, context files deliver substantially more value than the 4% measured on small open-source repos.

IMPLICATIONS FOR MYELIN: (1) Only surface tool specs, constraints, and non-inferable knowledge — never codebase overviews. (2) Human curation gate is essential — auto-generated tactics will hurt like auto-generated AGENTS.md. (3) Anti-patterns (what NOT to do) are more valuable than positive guidance. (4) Myelin should target the high-cost sessions where context files help most. (5) Cost overhead of ~20% per tactic is real — keep retrieval minimal (GUARD-005: max 5 items at boot).

## Supporting Evidence

> **Source [PRIMARY]:** medium.com/@addyosmani/stop-using-init-for-agents-md (content_hash:2454d556), retrieved 2026-04-03

## Disconfirmation Search

Searched for evidence that auto-generated context always helps. Found the opposite: ETH Zurich shows LLM-generated files hurt when docs exist. But also found the second study showing human-written files DO help on efficiency (-28% wall time, -20% tokens). And practitioner feedback that proprietary codebases benefit more than open-source. The truth is nuanced: context helps when it's non-redundant, human-curated, and minimal. This directly shapes myelin's design constraints.

## Caveats

None identified yet.
