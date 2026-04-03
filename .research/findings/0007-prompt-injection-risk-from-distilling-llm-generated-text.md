---
id: '0007'
title: 'Prompt injection risk from distilling LLM-generated text'
status: open
evidence: LOW
sources:
- text: 'GPT-5.2: treat transcripts as untrusted input'
  tier: SECONDARY
created: '2026-04-03'
---

## Claim

Session transcripts contain LLM-generated text. Distilling tactics from this is training on model output — a prompt injection vector. Need denylist and safe-format rewriter. Tactics must never introduce tool permissions, secrets handling, or instruction-override content.

## Supporting Evidence

> **Source [SECONDARY]:** GPT-5.2: treat transcripts as untrusted input, retrieved 2026-04-03

## Caveats

None identified yet.
