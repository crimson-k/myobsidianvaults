---
type: "literature-note"
title: "Motion Forcing: A Decoupled Framework for Robust Video Generation in Motion Dynamics"
aliases: ["Motion Forcing: A Decoupled Framework for Robust Video Generation in Motion Dynamics"]
zotero_keys: ["3X7CKIBU"]
year: 2026
authors: ["Tianshuo Xu", "Zhifei Chen", "Leyi Wu", "Hao Lu", "Ying-cong Chen"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2603.10408"
url: "http://arxiv.org/abs/2603.10408"
collections: ["03 Visual Generation/Camera & Motion Control"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Motion Forcing: A Decoupled Framework for Robust Video Generation in Motion Dynamics

[Zotero 条目 3X7CKIBU](zotero://select/library/items/3X7CKIBU)

[DOI 原文](https://doi.org/10.48550/arxiv.2603.10408)

[来源网页](http://arxiv.org/abs/2603.10408)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/Camera & Motion Control/索引|03 Visual Generation/Camera & Motion Control]]

## 原始摘要

The ultimate goal of video generation is to satisfy a fundamental trilemma: achieving high visual quality, maintaining rigorous physical consistency, and enabling precise controllability. While recent models can maintain this balance in simple, isolated scenarios, we observe that this equilibrium is fragile and often breaks down as scene complexity increases (e.g., involving collisions or dense traffic). To address this, we introduce \textbf{Motion Forcing}, a framework designed to stabilize this trilemma even in complex generative tasks. Our key insight is to explicitly decouple physical reasoning from visual synthesis via a hierarchical \textbf{``Point-Shape-Appearance''} paradigm. This approach decomposes generation into verifiable stages: modeling complex dynamics as sparse geometric anchors (\textbf{Point}), expanding them into dynamic depth maps that explicitly resolve 3D geometry (\textbf{Shape}), and finally rendering high-fidelity textures (\textbf{Appearance}). Furthermore, to foster robust physical understanding, we employ a \textbf{Masked Point Recovery} strategy. By randomly masking input anchors during training and enforcing the reconstruction of complete dynamic depth, the model is compelled to move beyond passive pattern matching and learn latent physical laws (e.g., inertia) to infer missing trajectories. Extensive experiments on autonomous driving benchmarks show that Motion Forcing significantly outperforms state-of-the-art baselines, maintaining trilemma stability across complex scenes. Evaluations on physics and robotics further confirm our framework's generality.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: https://tianshuo-xu.github.io/Motion-Forcing/

[在 Zotero 查看](zotero://select/library/items/JJI5429G)

Comment: https://tianshuo-xu.github.io/Motion-Forcing/

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/N7CINUYE)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/MI377GIL)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-VAQCDKF8 - MoAlign  Motion-Centric Representation Alignment for Video Diffusion Models|MoAlign: Motion-Centric Representation Alignment for Video Diffusion Models]] — 强关联；都聚焦运动动力学与物理合理性，比较运动/外观解耦与运动子空间对齐。
- [[Zotero Knowledge/Papers/ZK-FGFQLWGF - PosePilot  Steering Camera Pose for Generative World Models with Self-supervised Dept|PosePilot: Steering Camera Pose for Generative World Models with Self-supervised Depth]] — 中关联；共同研究内容：基准与数据合成、物理可信度、自动驾驶。

<!-- content-relations:end -->
