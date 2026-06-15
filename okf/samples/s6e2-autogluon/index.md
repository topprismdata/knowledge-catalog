---
type: Bundle
title: S6E2 Heart Disease — AutoGluon Rerun
description: Mini OKF bundle documenting the 2026-06-14 AutoGluon-first rerun of Playground Series S6E2 (Heart Disease). Validates autogluon-first, catboost-first, and cv-lb-gap-acknowledgment skills; surfaces a new lesson on submission format.
tags: [kaggle, s6e2, autogluon, okf-demo]
timestamp: 2026-06-15T00:00:00Z
---

# S6E2 Heart Disease — AutoGluon Rerun

A demonstration OKF bundle for an ML competition's full experiment trail.

## Subdirectories

* [experiments](experiments/index.md) — Each major run/iteration as its own concept.
* [models](models/index.md) — Individual trained models (CatBoost, LightGBM, ensemble).
* [submissions](submissions/index.md) — Files submitted to the Kaggle LB.
* [lessons](lessons/index.md) — Skills / principles discovered or validated by this work.

## How to view

```bash
enrichment-agent visualize --bundle /tmp/s6e2-okf-bundle
# Opens an interactive force-directed graph of all concepts + links.
```

## Provenance

- **Repo**: `~/projects/s6e2-autogluon-rerun/`
- **Run date**: 2026-06-14
- **Best private LB**: 0.95510 (vs user's prior best 0.95516)
- **OOF AUC**: 0.95554
