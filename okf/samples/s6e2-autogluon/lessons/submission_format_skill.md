---
type: Lesson
title: submission-format-by-metric — NEW skill (PR #5)
description: New skill shipped to cultivating-ml-agent: match submission format to the competition metric. Discovered from S6E2 rerun.
resource: https://github.com/topprismdata/cultivating-ml-agent/pull/5
tags: [skill, new, submission-format, s6e2, shipped]
timestamp: 2026-06-15T00:00:00Z
---

# submission-format-by-metric — NEW skill (PR #5)

## Discovery
The S6E2 AutoGluon rerun surfaced a sneaky bug: same model (OOF 0.95554) scored Public LB
0.88403 with 0/1 submission and 0.95357 with probability submission. **0.07 LB drop from
format alone, not from real CV-LB divergence.**

## Skill content
- Decision tree: ranking metrics (AUC, log_loss, MAP, NDCG) need continuous probability files
- Framework cheatsheet: AutoGluon `predict_proba()`, sklearn/xgboost/lightgbm/catboost equivalents
- How to read `sample_submission.csv` correctly (0/1 values are target format, not submission format)
- Why this is a sneaky bug (OOF looks fine, error only on LB)
- Verification checklist before submitting

## Shipped to
PR #5 to `topprismdata/cultivating-ml-agent` on 2026-06-15.

## Evidence
- [R0a — 0/1 thresholded submission](../experiments/submission_0_1_threshold.md) (bad)
- [R0b — probability submission](../experiments/submission_proba.md) (good)
- [submission_autogluon.csv](../submissions/submission_autogluon_csv.md)
- [submission_autogluon_proba.csv](../submissions/submission_autogluon_proba_csv.md)

## Related
Refines [cv-lb-gap-acknowledgment](cv_lb_gap_skill.md).
