---
type: Experiment
title: R0a — 0/1 thresholded submission (the bug)
description: Same model, predicted via predictor.predict() (hard labels) instead of predict_proba() — Public LB dropped 0.07.
tags: [bug, submission-format, threshold, AUC]
timestamp: 2026-06-14T11:50:00Z
---

# R0a — 0/1 thresholded submission (the bug)

After training, I (the agent) saved a submission by running `predictor.predict(test)` which returns
class labels, then thresholded to 0/1. For an AUC-evaluated competition, this is wrong.

## What happened
- Same model as R0 (OOF 0.95554)
- Submission file: `submission_autogluon.csv` (270K rows, values 0/1)
- **Public LB: 0.88403** ❌
- Private LB: 0.88643

## Root cause
- AUC ranks predictions. 0/1 has no rank information → equivalent to random.
- AutoGluon's `predict()` returns class labels; `predict_proba()` is needed for AUC.

## Fix
See [R0b — probability submission](../experiments/submission_proba.md) — same model, correct
file format, LB recovered to 0.95357.

## Related
- This discovery led to a new skill: [submission-format-by-metric](../lessons/submission_format_skill.md).
- Refines [cv-lb-gap-acknowledgment](../lessons/cv_lb_gap_skill.md) — 0.05-0.10 gap is *not* overfitting.
