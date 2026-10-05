---
type: "literature-note"
title: "VGGRPO: Towards World-Consistent Video Generation with 4D Latent Reward"
aliases: ["VGGRPO: Towards World-Consistent Video Generation with 4D Latent Reward"]
zotero_keys: ["HF5UN3ZL"]
year: 2026
authors: ["Zhaochong An", "Orest Kupyn", "Théo Uscidda", "Andrea Colaco", "Karan Ahuja", "Serge Belongie", "Mar Gonzalez-Franco", "Marta Tintore Gazulla"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2603.26599"
url: "https://arxiv.org/abs/2603.26599"
collections: ["06 Alignment & Reliability/Physics Grounding & Rollout Verification"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature", "highlight"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# VGGRPO: Towards World-Consistent Video Generation with 4D Latent Reward

[Zotero 条目 HF5UN3ZL](zotero://select/library/items/HF5UN3ZL)

[DOI 原文](https://doi.org/10.48550/arxiv.2603.26599)

[来源网页](https://arxiv.org/abs/2603.26599)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Physics Grounding & Rollout Verification/索引|06 Alignment & Reliability/Physics Grounding & Rollout Verification]]

概念地图：[[Zotero Knowledge/Concepts/物理一致性与表征对齐|物理一致性与表征对齐]]

## 原始摘要

Large-scale video diffusion models achieve impressive visual quality, yet often fail to preserve geometric consistency. Prior approaches improve consistency either by augmenting the generator with additional modules or applying geometry-aware alignment. However, architectural modifications can compromise the generalization of internet-scale pretrained models, while existing alignment methods are limited to static scenes and rely on RGB-space rewards that require repeated VAE decoding, incurring substantial compute overhead and failing to generalize to highly dynamic real-world scenes. To preserve the pretrained capacity while improving geometric consistency, we propose VGGRPO (Visual Geometry GRPO), a latent geometry-guided framework for geometry-aware video post-training. VGGRPO introduces a Latent Geometry Model (LGM) that stitches video diffusion latents to geometry foundation models, enabling direct decoding of scene geometry from the latent space. By constructing LGM from a geometry model with 4D reconstruction capability, VGGRPO naturally extends to dynamic scenes, overcoming the static-scene limitations of prior methods. Building on this, we perform latent-space Group Relative Policy Optimization with two complementary rewards: a camera motion smoothness reward that penalizes jittery trajectories, and a geometry reprojection consistency reward that enforces cross-view geometric coherence. Experiments on both static and dynamic benchmarks show that VGGRPO improves camera stability, geometry consistency, and overall quality while eliminating costly VAE decoding, making latent-space geometry-guided reinforcement an efficient and flexible approach to world-consistent video generation.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/HM5XDWRY)

## Other
Accepted at ECCV 2026. Project Page: https://zhaochongan.github.io/projects/VGGRPO

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/PN6YCQNJ)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
