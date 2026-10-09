---
type: "literature-note"
title: "Geometry Forcing: Marrying Video Diffusion and 3D Representation for Consistent World Modeling"
aliases: ["Geometry Forcing: Marrying Video Diffusion and 3D Representation for Consistent World Modeling"]
zotero_keys: ["HD5LCZ33"]
year: 2026
authors: ["Haoyu Wu", "Diankun Wu", "Tianyu He", "Junliang Guo", "Yang Ye", "Yueqi Duan", "Jiang Bian"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2507.07982"
url: "http://arxiv.org/abs/2507.07982"
collections: ["06 Alignment & Reliability/Representation Alignment"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature", "concept/几何先验与跨视角生成", "concept-primary/几何先验与跨视角生成"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Geometry Forcing: Marrying Video Diffusion and 3D Representation for Consistent World Modeling

[Zotero 条目 HD5LCZ33](zotero://select/library/items/HD5LCZ33)

[DOI 原文](https://doi.org/10.48550/arxiv.2507.07982)

[来源网页](http://arxiv.org/abs/2507.07982)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]

概念地图：[[Zotero Knowledge/Concepts/几何先验与跨视角生成|几何先验与跨视角生成]]

## 原始摘要

Videos inherently represent 2D projections of a dynamic 3D world. However, our analysis suggests that video diffusion models trained solely on raw video data often fail to capture meaningful geometric-aware structure in their learned representations. To bridge the gap between video diffusion models and the underlying 3D nature of the physical world, we propose Geometry Forcing, a simple yet effective method that encourages video diffusion models to internalize 3D representations. Our key insight is to guide the model's intermediate representations toward geometry-aware structure by aligning them with features from a geometric foundation model. To this end, we introduce two complementary alignment objectives: Angular Alignment, which enforces directional consistency via cosine similarity, and Scale Alignment, which preserves scale-related information by regressing geometric features from normalized diffusion representations. We evaluate Geometry Forcing on both camera-view conditioned and action-conditioned video generation tasks. Experimental results demonstrate that our method substantially improves visual quality and 3D consistency over the baseline methods. Project page: https://GeometryForcing.github.io.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: 24 pages, project page: https://GeometryForcing.github.io

[在 Zotero 查看](zotero://select/library/items/4FYF23YK)

Comment: 24 pages, project page: https://GeometryForcing.github.io

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/7DJXJ4YE)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/C9AWMU7Z)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-7TDQKU5X - VideoREPA  Learning Physics for Video Generation through Relational Alignment with Fo|VideoREPA: Learning Physics for Video Generation through Relational Alignment with Foundation Models]] — 强关联；均以外部表征约束视频生成；比较三维几何结构与物理 token 关系。
- [[Zotero Knowledge/Papers/ZK-V4F8I7PZ - WristWorld  Generating Wrist-Views via 4D World Models for Robotic Manipulation|WristWorld: Generating Wrist-Views via 4D World Models for Robotic Manipulation]] — 强关联；均把几何表征作为视频生成约束；比较腕部跨视角重建与生成表征对齐。
- [[Zotero Knowledge/Papers/ZK-P3MHR9KR - CamGeo  Sparse Camera-Conditioned Image-to-Video Generation with 3D Geometry Priors|CamGeo: Sparse Camera-Conditioned Image-to-Video Generation with 3D Geometry Priors]] — 中关联；共同研究内容：几何与三维重建。
- [[Zotero Knowledge/Papers/ZK-HF5UN3ZL - VGGRPO  Towards World-Consistent Video Generation with 4D Latent Reward|VGGRPO: Towards World-Consistent Video Generation with 4D Latent Reward]] — 中关联；共同研究内容：几何与三维重建、扩散生成架构。

<!-- content-relations:end -->
