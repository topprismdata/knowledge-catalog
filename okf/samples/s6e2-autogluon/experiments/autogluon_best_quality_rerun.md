---
type: Experiment
title: R0 — AutoGluon best_quality rerun
description: 15-minute full ensemble run that validated the autogluon-first skill on S6E2.
tags: [autogluon, best_quality, rerun, baseline]
timestamp: 2026-06-14T11:33:12Z
---

# R0 — AutoGluon best_quality rerun

Single AutoGluon `best_quality` preset run, time_limit=900s, on 10-core CPU (no GPU).

## Result
- **OOF AUC**: 0.95554
- **Total runtime**: 15.48 min
- **Best single model**: CatBoost BAG L1 (OOF 0.95550)
- **Best ensemble**: WeightedEnsemble L3 (OOF 0.95554)

## Trained models (14)
1. LightGBMXT BAG L1 — 0.94609
2. LightGBM BAG L1 — 0.95523
3. RandomForestGini BAG L1 — 0.95257
4. RandomForestEntr BAG L1 — 0.95264
5. CatBoost BAG L1 — **0.95550** ⭐
6. ExtraTreesGini BAG L1 — 0.95111
7. XGBoost BAG L1 — 0.94784
8-13. L2 stackings + WeightedEnsemble L2/L3

## Related
- Trained [CatBoost BAG L1](../models/catboost_bag_l1.md), [LightGBM BAG L1](../models/lightgbm_bag_l1.md), and [Weighted Ensemble L3](../models/weighted_ensemble_l3.md).
- Produced [submission_autogluon.csv](../submissions/submission_autogluon_csv.md) and [submission_autogluon_proba.csv](../submissions/submission_autogluon_proba_csv.md).
- Validates [autogluon-first skill](../lessons/autogluon_first_skill.md) and [catboost-first skill](../lessons/catboost_first_skill.md).
