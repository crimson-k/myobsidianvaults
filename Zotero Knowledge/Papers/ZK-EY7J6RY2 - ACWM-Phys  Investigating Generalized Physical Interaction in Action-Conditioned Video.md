---
type: "literature-note"
title: "ACWM-Phys: Investigating Generalized Physical Interaction in Action-Conditioned Video World Models"
aliases: ["ACWM-Phys: Investigating Generalized Physical Interaction in Action-Conditioned Video World Models"]
zotero_keys: ["EY7J6RY2"]
year: 2026
authors: ["Haotian Xue", "Yipu Chen", "Liqian Ma", "Zelin Zhao", "Lama Moukheiber", "Yuchen Zhu", "Yongxin Chen"]
venue: "arXiv.org"
venue_field: "websiteTitle"
doi: ""
url: "https://arxiv.org/abs/2605.08567v2"
collections: ["07 Evaluation & Data/World Model Benchmarks"]
source_tags: []
tags: ["zotero", "literature", "concept/世界模型评测与功能有效性", "concept-primary/世界模型评测与功能有效性"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# ACWM-Phys: Investigating Generalized Physical Interaction in Action-Conditioned Video World Models

[Zotero 条目 EY7J6RY2](zotero://select/library/items/EY7J6RY2)

[来源网页](https://arxiv.org/abs/2605.08567v2)

## 主题与知识联系

- [[Zotero Knowledge/Topics/07 Evaluation & Data/World Model Benchmarks/索引|07 Evaluation & Data/World Model Benchmarks]]

概念地图：[[Zotero Knowledge/Concepts/世界模型评测与功能有效性|世界模型评测与功能有效性]]

## 原始摘要

Action-conditioned world models (ACWMs) have shown strong promise for video prediction and decision-making. However, existing benchmarks are largely restricted to egocentric navigation or narrow, task-specific robotics datasets, offering only limited coverage of the rich physical interactions required for generalized world understanding. We introduce ACWM-Phys, a new benchmark for evaluating action-conditioned prediction under diverse physical dynamics in a clean, controllable simulation environment with a carefully designed action space. ACWM-Phys contains training and evaluation data spanning rigid-body dynamics, kinematics, deformable-object interactions, and particle dynamics. To evaluate both interpolation and generalization, we design in-distribution and out-of-distribution protocols with controlled shifts in interaction patterns or scene configurations. By building the benchmark in a fully controllable simulator, ACWM-Phys enables precise data collection, reproducible evaluation, and systematic analysis of model capabilities for physically grounded world modeling. Through systematic experiments on ACWM-DiT, we find that OoD generalization depends not only on the physical regime but also on effective task complexity: models generalize well on visually simple, low-dimensional interactions with clear geometric structure, but suffer larger drops on deformable contacts, high-dimensional control, and complex articulated motion. This suggests that the model still relies heavily on visual appearance patterns instead of fully learning the underlying physics. Ablations show that cross-attention improves high-dimensional action conditioning, causal VAEs outperform frame-wise encoders, and larger action spaces are harder to model but can improve generalization by providing richer control signals. These findings guide the design of physically grounded world models.

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/HB4UARGD)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
