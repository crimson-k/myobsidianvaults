---
type: "literature-note"
title: "LagerNVS: Latent Geometry for Fully Neural Real-time Novel View Synthesis"
aliases: ["LagerNVS: Latent Geometry for Fully Neural Real-time Novel View Synthesis"]
zotero_keys: ["CAIJSNQV"]
year: 2026
authors: ["Stanislaw Szymanowicz", "Minghao Chen", "Jianyuan Wang", "Christian Rupprecht", "Andrea Vedaldi"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2603.20176"
url: "https://arxiv.org/abs/2603.20176"
collections: ["02 Representation & Perception/3D Reconstruction & Novel Views"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature", "concept/几何先验与跨视角生成", "concept-primary/几何先验与跨视角生成"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# LagerNVS: Latent Geometry for Fully Neural Real-time Novel View Synthesis

[Zotero 条目 CAIJSNQV](zotero://select/library/items/CAIJSNQV)

[DOI 原文](https://doi.org/10.48550/arxiv.2603.20176)

[来源网页](https://arxiv.org/abs/2603.20176)

## 主题与知识联系

- [[Zotero Knowledge/Topics/02 Representation & Perception/3D Reconstruction & Novel Views/索引|02 Representation & Perception/3D Reconstruction & Novel Views]]

概念地图：[[Zotero Knowledge/Concepts/几何先验与跨视角生成|几何先验与跨视角生成]]

## 原始摘要

Recent work has shown that neural networks can perform 3D tasks such as Novel View Synthesis (NVS) without explicit 3D reconstruction. Even so, we argue that strong 3D inductive biases are still helpful in the design of such networks. We show this point by introducing LagerNVS, an encoder-decoder neural network for NVS that builds on ‘3D-aware’ latent features. The encoder is initialized from a 3D reconstruction network pre-trained using explicit 3D supervision. This is paired with a lightweight decoder, and trained end-to-end with photometric losses. LagerNVS achieves state-of-the-art deterministic feed-forward Novel View Synthesis (including 31.4 PSNR on Re10k), with and without known cameras, renders in real time, generalizes to in-the-wild data, and can be paired with a diffusion decoder for generative extrapolation. See szymanowiczs.github.io/lagernvs for code, models, and examples.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/VQY87PRU)

## Other
IEEE CVF Conference on Computer Vision and Pattern Recognition 2026. Project page with code, models and examples: szymanowiczs.github.io/lagernvs

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/EMUBZ5XV)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-N3JDF44L - VGGT  Visual Geometry Grounded Transformer|VGGT: Visual Geometry Grounded Transformer]] — 强关联；共同研究内容：几何与三维重建、相机与新视角。
- [[Zotero Knowledge/Papers/ZK-XBJS4F2B - NeoVerse  Enhancing 4D World Model with in-the-wild Monocular Videos|NeoVerse: Enhancing 4D World Model with in-the-wild Monocular Videos]] — 中关联；共同研究内容：几何与三维重建、相机与新视角。
- [[Zotero Knowledge/Papers/ZK-ZYMGZC8K - Exo2EgoSyn  Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric|Exo2EgoSyn: Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric Video Synthesis]] — 中关联；共同研究内容：几何与三维重建、相机与新视角。
- [[Zotero Knowledge/Papers/ZK-P3MHR9KR - CamGeo  Sparse Camera-Conditioned Image-to-Video Generation with 3D Geometry Priors|CamGeo: Sparse Camera-Conditioned Image-to-Video Generation with 3D Geometry Priors]] — 中关联；共同研究内容：几何与三维重建。

<!-- content-relations:end -->
