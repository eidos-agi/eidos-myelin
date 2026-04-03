---
locked: true
locked_date: '2026-04-03'
---
# Decision Criteria

## correctness (weight: 0.25)
Does the architecture produce accurate, non-garbage tactics? Can it avoid the -3% AGENTS.md failure mode (finding 0015)?

## implementation_effort (weight: 0.15)
How much new code, how many repos touched, how long to MVP?

## self_improvement (weight: 0.20)
Can the system improve its own distillation, retrieval, and thresholds over time (finding 0018)?

## safety (weight: 0.25)
Resistance to garbage tactics, prompt injection (finding 0007), and harmful auto-generation. Human gate integrity (finding 0015).

## ecosystem_fit (weight: 0.15)
How well does it integrate with commons, resume-resume, the daemon, and the existing Eidos toolchain (finding 0002)?
