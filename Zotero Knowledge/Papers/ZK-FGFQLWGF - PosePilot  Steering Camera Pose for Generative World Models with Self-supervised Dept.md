---
type: "literature-note"
title: "PosePilot: Steering Camera Pose for Generative World Models with Self-supervised Depth"
aliases: ["PosePilot: Steering Camera Pose for Generative World Models with Self-supervised Depth"]
zotero_keys: ["FGFQLWGF"]
year: 2025
authors: ["Bu Jin", "Weize Li", "Baihan Yang", "Zhenxin Zhu", "Junpeng Jiang", "Huan-ang Gao", "Haiyang Sun", "Kun Zhan", "Hengtong Hu", "Xueyang Zhang", "Peng Jia", "Hao Zhao"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2505.01729"
url: "https://arxiv.org/abs/2505.01729"
collections: ["03 Visual Generation/Camera & Motion Control"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# PosePilot: Steering Camera Pose for Generative World Models with Self-supervised Depth

[Zotero 条目 FGFQLWGF](zotero://select/library/items/FGFQLWGF)

[DOI 原文](https://doi.org/10.48550/arxiv.2505.01729)

[来源网页](https://arxiv.org/abs/2505.01729)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Camera & Motion Control/索引|03 Visual Generation/Camera & Motion Control]]

## 原始摘要

Recent advancements in autonomous driving (AD) systems have highlighted the potential of world models in achieving robust and generalizable performance across both ordinary and challenging driving conditions. However, a key challenge remains: precise and flexible camera pose control, which is crucial for accurate viewpoint transformation and realistic simulation of scene dynamics. In this paper, we introduce PosePilot, a lightweight yet powerful framework that significantly enhances camera pose controllability in generative world models. Drawing inspiration from self-supervised depth estimation, PosePilot leverages structure-from-motion principles to establish a tight coupling between camera pose and video generation. Specifically, we incorporate self-supervised depth and pose readouts, allowing the model to infer depth and relative camera motion directly from video sequences. These outputs drive pose-aware frame warping, guided by a photometric warping loss that enforces geometric consistency across synthesized frames. To further refine camera pose estimation, we introduce a reverse warping step and a pose regression loss, improving viewpoint precision and adaptability. Extensive experiments on autonomous driving and generaldomain video datasets demonstrate that PosePilot significantly enhances structural understanding and motion reasoning in both diffusion-based and auto-regressive world models. By steering camera pose with self-supervised depth, PosePilot sets a new benchmark for pose controllability, enabling physically consistent, reliable viewpoint synthesis in generative world models.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/QRRGH4PW)

## Other
Accepted at IEEE/RSJ IROS 2025

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/2I9GUX56)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-3X7CKIBU - Motion Forcing  A Decoupled Framework for Robust Video Generation in Motion Dynamics|Motion Forcing: A Decoupled Framework for Robust Video Generation in Motion Dynamics]] — 中关联；共同研究内容：基准与数据合成、物理可信度、自动驾驶。

<!-- content-relations:end -->
