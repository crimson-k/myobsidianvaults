---
type: "literature-note"
title: "Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture"
aliases: ["Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture"]
zotero_keys: ["PZKQUJNM"]
year: 2023
authors: ["Mahmoud Assran", "Quentin Duval", "Ishan Misra", "Piotr Bojanowski", "Pascal Vincent", "Michael Rabbat", "Yann LeCun", "Nicolas Ballas"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2301.08243"
url: "http://arxiv.org/abs/2301.08243"
collections: ["02 Representation & Perception/Visual Representation Learning"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning", "Electrical Engineering and Systems Science - Image and Video Processing"]
tags: ["zotero", "literature", "concept/表征学习与世界模型", "concept-primary/表征学习与世界模型"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture

[Zotero 条目 PZKQUJNM](zotero://select/library/items/PZKQUJNM)

[DOI 原文](https://doi.org/10.48550/arxiv.2301.08243)

[来源网页](http://arxiv.org/abs/2301.08243)

## 主题与知识联系

- [[Zotero Knowledge/Topics/02 Representation & Perception/Visual Representation Learning/索引|02 Representation & Perception/Visual Representation Learning]]

概念地图：[[Zotero Knowledge/Concepts/表征学习与世界模型|表征学习与世界模型]]

## 原始摘要

This paper demonstrates an approach for learning highly semantic image representations without relying on hand-crafted data-augmentations. We introduce the Image-based Joint-Embedding Predictive Architecture (I-JEPA), a non-generative approach for self-supervised learning from images. The idea behind I-JEPA is simple: from a single context block, predict the representations of various target blocks in the same image. A core design choice to guide I-JEPA towards producing semantic representations is the masking strategy; specifically, it is crucial to (a) sample target blocks with sufficiently large scale (semantic), and to (b) use a sufficiently informative (spatially distributed) context block. Empirically, when combined with Vision Transformers, we find I-JEPA to be highly scalable. For instance, we train a ViT-Huge/14 on ImageNet using 16 A100 GPUs in under 72 hours to achieve strong downstream performance across a wide range of tasks, from linear classification to object counting and depth prediction.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: 2023 IEEE/CVF International Conference on Computer Vision

[在 Zotero 查看](zotero://select/library/items/2YL4EMW6)

Comment: 2023 IEEE/CVF International Conference on Computer Vision

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/KXV3N2P9)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/PUSGTZSH)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-SRGTDGP2 - Revisiting Feature Prediction for Learning Visual Representations from Video|Revisiting Feature Prediction for Learning Visual Representations from Video]] — 强关联；共同采用表征预测而非像素重建；比较图像与视频的自监督目标。
- [[Zotero Knowledge/Papers/ZK-EJEPANDU - V-JEPA 2  Self-Supervised Video Models Enable Understanding, Prediction and Planning|V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning]] — 中关联；共同研究内容：表征预测 / JEPA、视觉自监督。

<!-- content-relations:end -->
