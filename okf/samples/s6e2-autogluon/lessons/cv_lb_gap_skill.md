---
type: Lesson
title: cv-lb-gap-acknowledgment — refined
description: CV-LB gap has a bigger range than 0.005-0.01; submission format errors can cause 0.05-0.10+ gaps.
resource: file://~/projects/cultivating-ml-agent/skills/examples/cv-lb-gap-acknowledgment/SKILL.md
tags: [skill, cv-lb-gap, refined, s6e2]
timestamp: 2026-06-14T11:51:00Z
---

# cv-lb-gap-acknowledgment — refined

## Original claim
CV-LB gap is typically 0.005-0.01 on tabular competitions. Always validate on LB.

## New finding
CV-LB gap can be 0.05-0.10+ when the **submission format is wrong** (e.g., 0/1 instead of
probability for AUC). This is *not* overfitting to OOF noise — it's a completely different bug.

## Decomposed gap sources
1. **Submission format error** (0/1 vs probability): 0.05-0.10+ gap, looks like model failure
2. **Real CV-LB gap** (overfitting / distribution shift): 0.002-0.01 typical, 0.01-0.05 concerning
3. **Tie-break noise** in leaderboard: ~0.0001-0.001

## Decision tree
- LB much lower than OOF → **first check submission format** before assuming overfitting
- LB slightly lower than OOF (≤0.01) → normal, blend with prior submissions
- LB higher than OOF → test set easier (rare but happens)

## Evidence
- [R0a — 0/1 thresholded submission](../experiments/submission_0_1_threshold.md) — same model, gap 0.07
- [R0b — probability submission](../experiments/submission_proba.md) — same model, gap 0.002

## Related
This refinement led to a new skill: [submission-format-by-metric](submission_format_skill.md)
