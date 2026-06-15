---
type: Model
title: CatBoost BAG L1
description: Top single model in the AutoGluon ensemble. OOF AUC 0.95550, 68.8% ensemble weight.
resource: file://~/projects/s6e2-autogluon-rerun/ag_models_best/models/CatBoost_BAG_L1/
tags: [catboost, gradient-boosting, best-single-model, s6e2]
timestamp: 2026-06-14T11:50:00Z
---

# CatBoost BAG L1

## Metrics
- **OOF AUC**: 0.95550
- **Training time**: 174.13s
- **Validation time**: 0.32s
- **Ensemble weight**: 0.688 (dominant in L3 weighted ensemble)

## Why CatBoost won
- Native categorical handling (S6E2 has many discrete medical features)
- Ordered boosting prevents target leakage
- Robust defaults — less hyperparameter tuning needed

## Trained in
[R0 — AutoGluon best_quality rerun](../experiments/autogluon_best_quality_rerun.md)

## Supports
[catboost-first skill](../lessons/catboost_first_skill.md) — empirically validated on S6E2.
