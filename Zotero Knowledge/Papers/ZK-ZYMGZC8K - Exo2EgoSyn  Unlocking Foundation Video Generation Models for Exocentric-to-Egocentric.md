---
type: "literature-note"
title: "Exo2EgoSyn: Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric Video Synthesis"
aliases: ["Exo2EgoSyn: Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric Video Synthesis"]
zotero_keys: ["ZYMGZC8K"]
year: 2025
authors: ["Mohammad Mahdi", "Yuqian Fu", "Nedko Savov", "Jiancheng Pan", "Danda Pani Paudel", "Luc Van Gool"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2511.20186"
url: "https://arxiv.org/abs/2511.20186"
collections: ["03 Visual Generation/Cross-View & Ego-Exo Generation"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature", "concept/几何先验与跨视角生成", "concept-primary/几何先验与跨视角生成"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Exo2EgoSyn: Unlocking Foundation Video Generation Models for Exocentric-to-Egocentric Video Synthesis

[Zotero 条目 ZYMGZC8K](zotero://select/library/items/ZYMGZC8K)

[DOI 原文](https://doi.org/10.48550/arxiv.2511.20186)

[来源网页](https://arxiv.org/abs/2511.20186)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Cross-View & Ego-Exo Generation/索引|03 Visual Generation/Cross-View & Ego-Exo Generation]]

概念地图：[[Zotero Knowledge/Concepts/几何先验与跨视角生成|几何先验与跨视角生成]]

## 原始摘要

Foundation video generation models such as WAN 2.2 exhibit strong text- and image-conditioned synthesis abilities but remain constrained to the same-view generation setting. In this work, we introduce Exo2EgoSyn, an adaptation of WAN 2.2 that unlocks Exocentric-to-Egocentric (Exo2Ego) cross-view video synthesis. Our framework consists of three key modules. Ego-Exo View Alignment (EgoExo-Align) enforces latent-space alignment between exocentric and egocentric first-frame representations, reorienting the generative space from the given exo view toward the ego view. Multi-view Exocentric Video Conditioning (MultiExoCon) aggregates multi-view exocentric videos into a unified conditioning signal, extending WAN 2.2 beyond its vanilla single-image or text conditioning. Furthermore, Pose-Aware Latent Injection (PoseInj) injects relative exo-to-ego camera pose information into the latent state, guiding geometry-aware synthesis across viewpoints. Together, these modules enable high-fidelity egoview video generation from third-person observations without retraining from scratch. Experiments on ExoEgo4D validate that Exo2EgoSyn significantly improves Ego2Exo synthesis, paving the way for scalable cross-view video generation with foundation models. Source code and models will be released publicly.

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/2R4E6YET)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-ZR2LFUNE - Wan  Open and Advanced Large-Scale Video Generative Models|Wan: Open and Advanced Large-Scale Video Generative Models]] — 强关联；本篇摘要提到模型 WAN 2.2（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-GKL8V5LR - 4DIFF  3D-Aware Diffusion Model for Third-to-First Viewpoint Translation|4DIFF: 3D-Aware Diffusion Model for Third-to-First Viewpoint Translation]] — 中关联；共同研究内容：几何与三维重建、第一 / 第三人称变换。
- [[Zotero Knowledge/Papers/ZK-L4HN4GWD - EgoWorld  Translating Exocentric View to Egocentric View using Rich Exocentric Observ|EgoWorld: Translating Exocentric View to Egocentric View using Rich Exocentric Observations]] — 中关联；共同研究内容：相机与新视角、第一 / 第三人称变换。
- [[Zotero Knowledge/Papers/ZK-CAIJSNQV - LagerNVS  Latent Geometry for Fully Neural Real-time Novel View Synthesis|LagerNVS: Latent Geometry for Fully Neural Real-time Novel View Synthesis]] — 中关联；共同研究内容：几何与三维重建、相机与新视角。

<!-- content-relations:end -->
