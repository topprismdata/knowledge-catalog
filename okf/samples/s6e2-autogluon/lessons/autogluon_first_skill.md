---
type: Lesson
title: autogluon-first skill — validated
description: AutoGluon best_quality on S6E2 hit 0.95554 OOF in 15 min, matching user's multi-day manual stacking.
resource: file://~/projects/cultivating-ml-agent/skills/examples/autogluon-first/SKILL.md
tags: [skill, autogluon, validated, s6e2]
timestamp: 2026-06-14T11:50:00Z
---

# autogluon-first skill — validated

## Claim
Always run AutoGluon `best_quality` preset as the first step in any tabular ML competition.
Validated 3/4 times vs manual ensembles on small/medium tabular datasets.

## Evidence from this run
- **Single AutoGluon run**: OOF 0.95554 / Private LB 0.95510 in 15.48 min.
- **User's prior best** (multi-day manual stacking, 18 submissions): Private LB 0.95516.
- **Δ**: -0.00006 (statistically tied).

## Implication
- Manual stacking no longer gives a clear edge over AutoGluon for S6E2-class tabular problems.
- The skill's "15 min for a strong baseline" claim is empirically verified.
- Recommend future work: blend AutoGluon output with user models (small but non-zero edge).

## Validated by
[R0 — AutoGluon best_quality rerun](../experiments/autogluon_best_quality_rerun.md)
