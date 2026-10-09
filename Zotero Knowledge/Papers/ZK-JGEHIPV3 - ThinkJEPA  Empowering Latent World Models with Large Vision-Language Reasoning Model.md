---
type: "literature-note"
title: "ThinkJEPA: Empowering Latent World Models with Large Vision-Language Reasoning Model"
aliases: ["ThinkJEPA: Empowering Latent World Models with Large Vision-Language Reasoning Model"]
zotero_keys: ["JGEHIPV3"]
year: 2026
authors: ["Haichao Zhang", "Yijiang Li", "Shwai He", "Tushar Nagarajan", "Mingfei Chen", "Jianglin Lu", "Ang Li", "Yun Fu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2603.22281"
url: "http://arxiv.org/abs/2603.22281"
collections: ["04 World Models/Latent & Object-Centric Dynamics"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computation and Language", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning", "Computer Science - Robotics"]
tags: ["zotero", "literature", "concept/表征学习与世界模型", "concept-primary/表征学习与世界模型"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# ThinkJEPA: Empowering Latent World Models with Large Vision-Language Reasoning Model

[Zotero 条目 JGEHIPV3](zotero://select/library/items/JGEHIPV3)

[DOI 原文](https://doi.org/10.48550/arxiv.2603.22281)

[来源网页](http://arxiv.org/abs/2603.22281)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Latent & Object-Centric Dynamics/索引|04 World Models/Latent & Object-Centric Dynamics]]

概念地图：[[Zotero Knowledge/Concepts/表征学习与世界模型|表征学习与世界模型]]

补充阅读入口：[[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]]

## 原始摘要

Recent progress in latent world models (e.g., V-JEPA2) has shown promising capability in forecasting future world states from video observations. Nevertheless, dense prediction from a short observation window limits temporal context and can bias predictors toward local, low-level extrapolation, making it difficult to capture long-horizon semantics and reducing downstream utility. Vision--language models (VLMs), in contrast, provide strong semantic grounding and general knowledge by reasoning over uniformly sampled frames, but they are not ideal as standalone dense predictors due to compute-driven sparse sampling, a language-output bottleneck that compresses fine-grained interaction states into text-oriented representations, and a data-regime mismatch when adapting to small action-conditioned datasets. We propose a VLM-guided JEPA-style latent world modeling framework that combines dense-frame dynamics modeling with long-horizon semantic guidance via a dual-temporal pathway: a dense JEPA branch for fine-grained motion and interaction cues, and a uniformly sampled VLM \emph{thinker} branch with a larger temporal stride for knowledge-rich guidance. To transfer the VLM's progressive reasoning signals effectively, we introduce a hierarchical pyramid representation extraction module that aggregates multi-layer VLM representations into guidance features compatible with latent prediction. Experiments on hand-manipulation trajectory prediction show that our method outperforms both a strong VLM-only baseline and a JEPA-predictor baseline, and yields more robust long-horizon rollout behavior.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: 10 pages, 5 figures

[在 Zotero 查看](zotero://select/library/items/6E675V6L)

Comment: 10 pages, 5 figures

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/WUWT3EJM)

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/7EXZWCNL)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-EJEPANDU - V-JEPA 2  Self-Supervised Video Models Enable Understanding, Prediction and Planning|V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning]] — 强关联；本篇摘要提到模型 V-JEPA2（仅确认名称提及）。

<!-- content-relations:end -->
