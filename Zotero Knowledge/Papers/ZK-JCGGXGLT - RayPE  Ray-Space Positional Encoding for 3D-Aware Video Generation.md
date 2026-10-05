---
type: "literature-note"
title: "RayPE: Ray-Space Positional Encoding for 3D-Aware Video Generation"
aliases: ["RayPE: Ray-Space Positional Encoding for 3D-Aware Video Generation"]
zotero_keys: ["JCGGXGLT"]
year: 2026
authors: ["Minghao Yin", "Jiahao Lu", "Wenbo Hu", "Wang Zhao", "Shan Ying", "Kai Han"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2606.27345"
url: "http://arxiv.org/abs/2606.27345"
collections: ["03 Visual Generation/Camera & Motion Control"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# RayPE: Ray-Space Positional Encoding for 3D-Aware Video Generation

[Zotero 条目 JCGGXGLT](zotero://select/library/items/JCGGXGLT)

[DOI 原文](https://doi.org/10.48550/arxiv.2606.27345)

[来源网页](http://arxiv.org/abs/2606.27345)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Camera & Motion Control/索引|03 Visual Generation/Camera & Motion Control]]

概念地图：[[Zotero Knowledge/Concepts/几何先验与跨视角生成|几何先验与跨视角生成]]

## 原始摘要

Modern video diffusion transformers position their tokens through RoPE on the (u,v,t) axes -- a description of the camera's sampling grid that says nothing about the 3D structure of the scene. We observe that the geometric relation between two camera rays is captured by the Plucker reciprocal product, which is bilinear in the two rays -- the same algebraic form as the dot product in Transformer attention. Building on this analogy, we propose RayPE, a positional-encoding extension that injects per-token 6D Plucker coordinates additively into the queries and keys of self-attention, with a query/key flip arrangement under which the symmetric identity configuration coincides exactly with the reciprocal product. The injection is additive, the resulting attention score decomposes into a content term, a geometry term, and two content and geometry cross-terms -- all of which our experiments find individually necessary. To make the encoding stable across video data with heterogeneous camera-translation scales (SfM, deep SLAM, metric), we further decouple ray direction from moment magnitude, gate the encoding by a learned function of the log-magnitude, and apply RMSNorm to align it with the QKNorm-normalized content branch. The full module adds less than 0.1% parameters to a pretrained video DiT, is zero-initialized to start from the pretrained weights, and improves camera controllability, cross-frame 3D consistency, and overall video quality on a four-dataset training mixture.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project page: https://raype-project.github.io/

[在 Zotero 查看](zotero://select/library/items/SDRL3RNL)

Comment: Project page: https://raype-project.github.io/

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/XDZ6QMH4)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/F7F3YB5Z)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
