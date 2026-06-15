---
type: Experiment
title: R0b — Probability submission (the fix)
description: Same model, predicted via predictor.predict_proba() — Public LB recovered to 0.95357.
tags: [fix, submission-format, proba, AUC]
timestamp: 2026-06-14T11:51:54Z
---

# R0b — Probability submission (the fix)

Resubmission of R0 using `predictor.predict_proba(test)['Presence']` instead of thresholded
class labels. 30-second fix; 0.07 LB recovery.

## Result
- Submission: `submission_autogluon_proba.csv` (270K rows, float values in [0, 1])
- **Public LB: 0.95357** ✅
- **Private LB: 0.95510**
- CV-LB gap: ~0.002 (very small, normal)

## Comparison
| Submission | Format | Public LB | Private LB | OOF |
|---|---|---|---|---|
| submission_autogluon.csv | 0/1 | 0.88403 | 0.88643 | 0.95554 |
| submission_autogluon_proba.csv | proba | 0.95357 | **0.95510** | 0.95554 |

## Takeaway
Always check the metric before choosing submission format. For ranking metrics (AUC, log_loss,
MAP, NDCG), submit probabilities.

See [submission-format-by-metric skill](../lessons/submission_format_skill.md).
