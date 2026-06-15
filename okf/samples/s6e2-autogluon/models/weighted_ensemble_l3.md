---
type: Model
title: Weighted Ensemble L3
description: Final stacked ensemble. OOF AUC 0.95554 — basically tied with CatBoost BAG L1 alone.
resource: file://~/projects/s6e2-autogluon-rerun/ag_models_best/models/WeightedEnsemble_L3/
tags: [ensemble, stacking, s6e2, best-model]
timestamp: 2026-06-14T11:50:00Z
---

# Weighted Ensemble L3

## Metrics
- **OOF AUC**: 0.95554
- **Ensemble weights**:
  - CatBoost BAG L1: 0.688
  - RandomForestGini BAG L2: 0.125
  - RandomForestEntr BAG L2: 0.125
  - LightGBM BAG L1: 0.062

## Observation
Ensemble OOF (0.95554) is only +0.00004 over the best single model CatBoost BAG L1 (0.95550).
Stacking is hitting the ceiling here — the 14 individual models are too similar to add
diversity. This is consistent with the `multi-level-aggregation-overfitting` warning.

## Trained in
[R0 — AutoGluon best_quality rerun](../experiments/autogluon_best_quality_rerun.md)

## Components
- [CatBoost BAG L1](catboost_bag_l1.md) (0.688)
- [LightGBM BAG L1](lightgbm_bag_l1.md) (0.062)
- RandomForestGini BAG L2, RandomForestEntr BAG L2 (0.125 each)
