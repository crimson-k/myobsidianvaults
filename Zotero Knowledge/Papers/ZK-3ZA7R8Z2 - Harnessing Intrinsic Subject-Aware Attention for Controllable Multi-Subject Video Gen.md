---
type: "literature-note"
title: "Harnessing Intrinsic Subject-Aware Attention for Controllable Multi-Subject Video Generation"
aliases: ["Harnessing Intrinsic Subject-Aware Attention for Controllable Multi-Subject Video Generation"]
zotero_keys: ["3ZA7R8Z2"]
year: 2026
authors: ["Niange Yu", "Ye Tian", "Biaolong Chen", "Miao Lu", "Aixi Zhang", "Hao Jiang", "Yunhai Tong", "Pipei Huang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2609.11507"
url: "https://arxiv.org/abs/2609.11507"
collections: ["03 Visual Generation/Editing & Identity Control"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Harnessing Intrinsic Subject-Aware Attention for Controllable Multi-Subject Video Generation

[Zotero 条目 3ZA7R8Z2](zotero://select/library/items/3ZA7R8Z2)

[DOI 原文](https://doi.org/10.48550/arxiv.2609.11507)

[来源网页](https://arxiv.org/abs/2609.11507)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Editing & Identity Control/索引|03 Visual Generation/Editing & Identity Control]]

## 原始摘要

Multi-subject video generation faces two key challenges: uncontrollable fidelity strength and potential semantic drift. We address these by analyzing the internal mechanisms of Diffusion Transformers (DiTs). We found that certain attention blocks naturally form an Intrinsic Spatial Grounding Map (ISGM) that precisely locates reference subjects. Building on this insight, we propose Dual-phase Intrinsic Attention Leveraging (DIAL), a framework that uses these internal signals for both training and inference. In low-noise stages, we use ISGM to guide the attention mechanism, allowing precise control over fidelity strength during inference without retraining. In high-noise stages, we use these same maps to automatically build preference pairs at no additional cost for Reinforcement Learning (RL). This RL procedure effectively anchors the model’s attention to reference subjects and mitigates semantic drift. Extensive experiments show that DIAL significantly outperforms baseline models on the OpenS2V-Eval benchmark, consistently improving identity consistency and enabling controllable fidelity strength.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/DANZVZS3)

## Other
23 pages, 11 figures, 4 tables

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/IYEGETQ3)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
