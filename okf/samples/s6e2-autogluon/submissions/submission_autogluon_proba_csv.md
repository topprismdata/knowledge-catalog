---
type: Submission
title: submission_autogluon_proba.csv (probability)
description: Correct format for AUC — Public LB 0.95357, Private LB 0.95510.
resource: file://~/projects/s6e2-autogluon-rerun/submission_autogluon_proba.csv
tags: [kaggle, s6e2, correct, proba, submission-format]
timestamp: 2026-06-14T11:51:54Z
---

# submission_autogluon_proba.csv

## What
AutoGluon's `predictor.predict_proba(test)['Presence']` — float values in [0, 1]. Correct for AUC.

## LB scores
- **Public**: 0.95357 ✅
- **Private**: 0.95510

## Comparison with 0/1 version
| File | Format | Public LB | Private LB |
|---|---|---|---|
| submission_autogluon.csv | 0/1 | 0.88403 | 0.88643 |
| submission_autogluon_proba.csv | proba | **0.95357** | **0.95510** |

## Used in
- [R0b — probability submission](../experiments/submission_proba.md)

## Lesson
[submission-format-by-metric skill](../lessons/submission_format_skill.md)
