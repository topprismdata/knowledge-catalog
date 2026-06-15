---
type: Model
title: LightGBM BAG L1
description: Second strongest single model. OOF AUC 0.95523.
resource: file://~/projects/s6e2-autogluon-rerun/ag_models_best/models/LightGBM_BAG_L1/
tags: [lightgbm, gradient-boosting, s6e2]
timestamp: 2026-06-14T11:50:00Z
---

# LightGBM BAG L1

## Metrics
- **OOF AUC**: 0.95523
- **Training time**: 29.16s
- **Validation time**: 20.57s
- **Ensemble weight**: 0.062 (small but non-zero)

## Notes
- Fastest training among the strong models
- Slightly behind CatBoost BAG L1 (0.95523 vs 0.95550), consistent with catboost-first-skill evidence
- Useful for ensemble diversity (different family from CatBoost)

## Trained in
[R0 — AutoGluon best_quality rerun](../experiments/autogluon_best_quality_rerun.md)
