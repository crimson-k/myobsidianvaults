---
type: "literature-note"
title: "WorldGym: World Model as An Environment for Policy Evaluation"
aliases: ["WorldGym: World Model as An Environment for Policy Evaluation"]
zotero_keys: ["3TP5FDZ4"]
year: 2025
authors: ["Julian Quevedo", "Ansh Kumar Sharma", "Yixiang Sun", "Varad Suryavanshi", "Percy Liang", "Sherry Yang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2506.00613"
url: "http://arxiv.org/abs/2506.00613"
collections: ["05 Robot Learning/Simulation for Training & Evaluation"]
source_tags: ["Artificial Intelligence (cs.AI)", "Computer Science - Artificial Intelligence", "Computer Science - Robotics", "FOS: Computer and information sciences", "Robotics (cs.RO)", "notion"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# WorldGym: World Model as An Environment for Policy Evaluation

[Zotero 条目 3TP5FDZ4](zotero://select/library/items/3TP5FDZ4)

[DOI 原文](https://doi.org/10.48550/arxiv.2506.00613)

[来源网页](http://arxiv.org/abs/2506.00613)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/Simulation for Training & Evaluation/索引|05 Robot Learning/Simulation for Training & Evaluation]]

概念地图：[[Zotero Knowledge/Concepts/世界模型评测与功能有效性|世界模型评测与功能有效性]]

补充阅读入口：[[Zotero Knowledge/Topics/07 Evaluation & Data/World Model Benchmarks/索引|07 Evaluation & Data/World Model Benchmarks]]

## 原始摘要

Evaluating robot control policies is difficult: real-world testing is costly, and handcrafted simulators require manual effort to improve in realism and generality. We propose a world-model-based policy evaluation environment (WorldGym), an autoregressive, action-conditioned video generation model which serves as a proxy to real world environments. Policies are evaluated via Monte Carlo rollouts in the world model, with a vision-language model providing rewards. We evaluate a set of VLA-based real-robot policies in the world model using only initial frames from real robots, and show that policy success rates within the world model highly correlate with real-world success rates. Moreoever, we show that WorldGym is able to preserve relative policy rankings across different policy versions, sizes, and training checkpoints. Due to requiring only a single start frame as input, the world model further enables efficient evaluation of robot policies' generalization ability on novel tasks and environments. We find that modern VLA-based robot policies still struggle to distinguish object shapes and can become distracted by adversarial facades of objects. While generating highly realistic object interaction remains challenging, WorldGym faithfully emulates robot motions and offers a practical starting point for safe and reproducible policy evaluation before deployment.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/2RWUD2ZA)

## Other
https://world-model-eval.github.io

### Comment: https://world-model-eval.github.io

[在 Zotero 查看](zotero://select/library/items/KBVYCKWL)

Comment: https://world-model-eval.github.io

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/7PN5F8A5)

### Notion

[在 Zotero 查看附件](zotero://select/library/items/Z4FAJC69)

附件笔记：

## Do not modify or delete!

This link attachment serves as a reference for
[Notero](https://github.com/dvanoni/notero)
so that it can properly update the Notion page for this item.

Last synced: 2026/5/27 20:11:34

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
