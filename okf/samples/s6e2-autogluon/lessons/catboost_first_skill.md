---
type: Lesson
title: catboost-first skill — validated
description: CatBoost was the dominant single model (68.8% ensemble weight) on S6E2.
resource: file://~/projects/cultivating-ml-agent/skills/examples/catboost-first-tabular/SKILL.md
tags: [skill, catboost, validated, s6e2]
timestamp: 2026-06-14T11:50:00Z
---

# catboost-first skill — validated

## Claim
When manual GBDT is needed, start with CatBoost. CatBoost has native categorical handling,
robust to overfitting, and consistently outperforms other GBDTs on small/medium tabular
datasets with categorical features.

## Evidence from this run
- **CatBoost BAG L1** OOF: 0.95550
- **LightGBM BAG L1** OOF: 0.95523
- **XGBoost BAG L1** OOF: 0.94784
- **Ensemble weight**: CatBoost = **0.688** (dominant), LightGBM = 0.062.

## Implication
For S6E2 (14 medical features, many categorical), CatBoost was the right starting point —
even before stacking. Validates the skill's recommendation.

## Validated by
- [R0 — AutoGluon best_quality rerun](../experiments/autogluon_best_quality_rerun.md)
- [CatBoost BAG L1](../models/catboost_bag_l1.md)
