---
type: Submission
title: submission_autogluon.csv (0/1 thresholded)
description: WRONG format for AUC — Public LB 0.88403, Private LB 0.88643.
resource: file://~/projects/s6e2-autogluon-rerun/submission_autogluon.csv
tags: [kaggle, s6e2, bug, threshold, submission-format]
timestamp: 2026-06-14T11:50:00Z
---

# submission_autogluon.csv

## What
AutoGluon's `predictor.predict(test)` returns class labels, thresholded to 0/1. Wrong for AUC.

## LB scores
- **Public**: 0.88403 ❌
- **Private**: 0.88643

## Same model, different format
See [submission_autogluon_proba.csv](submission_autogluon_proba_csv.md) — LB recovered to 0.95510.

## Used in
- [R0a — 0/1 thresholded submission](../experiments/submission_0_1_threshold.md)

## Lesson
[submission-format-by-metric skill](../lessons/submission_format_skill.md)
