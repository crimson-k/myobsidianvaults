---
type: "literature-note"
title: "4DIFF: 3D-Aware Diffusion Model for Third-to-First Viewpoint Translation"
aliases: ["4DIFF: 3D-Aware Diffusion Model for Third-to-First Viewpoint Translation"]
zotero_keys: ["GKL8V5LR"]
year: 2025
authors: ["Feng Cheng", "Mi Luo", "Huiyu Wang", "Alex Dimakis", "Lorenzo Torresani", "Gedas Bertasius", "Kristen Grauman"]
venue: "Computer Vision – ECCV 2024"
venue_field: "bookTitle"
doi: "10.1007/978-3-031-72691-0_23"
url: "https://link.springer.com/10.1007/978-3-031-72691-0_23"
collections: ["03 Visual Generation/Cross-View & Ego-Exo Generation"]
source_tags: []
tags: ["zotero", "literature", "concept/几何先验与跨视角生成", "concept-primary/几何先验与跨视角生成"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# 4DIFF: 3D-Aware Diffusion Model for Third-to-First Viewpoint Translation

[Zotero 条目 GKL8V5LR](zotero://select/library/items/GKL8V5LR)

[DOI 原文](https://doi.org/10.1007/978-3-031-72691-0_23)

[来源网页](https://link.springer.com/10.1007/978-3-031-72691-0_23)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Cross-View & Ego-Exo Generation/索引|03 Visual Generation/Cross-View & Ego-Exo Generation]]

概念地图：[[Zotero Knowledge/Concepts/几何先验与跨视角生成|几何先验与跨视角生成]]

## 原始摘要

We present 4Diff, a 3D-aware diffusion model addressing the exo-to-ego viewpoint translation task — generating first-person (egocentric) view images from the corresponding third-person (exocentric) images. Building on the diffusion model’s ability to generate photorealistic images, we propose a transformer-based diffusion model that incorporates geometry priors through two mechanisms: (i) egocentric point cloud rasterization and (ii) 3D-aware rotary cross-attention. Egocentric point cloud rasterization converts the input exocentric image into an egocentric layout, which is subsequently used by a diffusion image transformer. As a component of the diffusion transformer’s denoiser block, the 3D-aware rotary cross-attention further incorporates 3D information and semantic features from the source exocentric view. Our 4Diff achieves stateof-the-art results on the challenging and diverse Ego-Exo4D multiview dataset and exhibits robust generalization to novel environments not encountered during training. Our code, processed data, and pretrained models are publicly available at https://klauscc.github.io/4diff.

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/INRN6J28)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-5IAAN6WR - Exocentric-to-Egocentric Video Generation|Exocentric-to-Egocentric Video Generation]] — 中关联；共同研究内容：扩散生成架构、第一 / 第三人称变换。
- [[Zotero Knowledge/Papers/ZK-ZYMGZC8K - Exo2EgoSyn  Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric|Exo2EgoSyn: Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric Video Synthesis]] — 中关联；共同研究内容：几何与三维重建、第一 / 第三人称变换。
- [[Zotero Knowledge/Papers/ZK-4FTGIUC9 - Put Myself in Your Shoes  Lifting the Egocentric Perspective from Exocentric Videos|Put Myself in Your Shoes: Lifting the Egocentric Perspective from Exocentric Videos]] — 中关联；共同研究内容：第一 / 第三人称变换。

<!-- content-relations:end -->
