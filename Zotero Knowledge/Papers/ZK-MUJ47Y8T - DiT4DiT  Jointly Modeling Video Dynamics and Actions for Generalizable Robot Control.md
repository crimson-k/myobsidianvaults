---
type: "literature-note"
title: "DiT4DiT: Jointly Modeling Video Dynamics and Actions for Generalizable Robot Control"
aliases: ["DiT4DiT: Jointly Modeling Video Dynamics and Actions for Generalizable Robot Control"]
zotero_keys: ["MUJ47Y8T"]
year: 2026
authors: ["Teli Ma", "Jia Zheng", "Zifan Wang", "Chunli Jiang", "Andy Cui", "Junwei Liang", "Shuo Yang"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2603.10448"
url: "http://arxiv.org/abs/2603.10448"
collections: ["05 Robot Learning/World-Action Models"]
source_tags: ["Computer Science - Robotics"]
tags: ["zotero", "literature", "highlight", "concept/世界动作模型与未来预测的作用", "concept-primary/世界动作模型与未来预测的作用"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# DiT4DiT: Jointly Modeling Video Dynamics and Actions for Generalizable Robot Control

[Zotero 条目 MUJ47Y8T](zotero://select/library/items/MUJ47Y8T)

[DOI 原文](https://doi.org/10.48550/arxiv.2603.10448)

[来源网页](http://arxiv.org/abs/2603.10448)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/World-Action Models/索引|05 Robot Learning/World-Action Models]]

概念地图：[[Zotero Knowledge/Concepts/世界动作模型与未来预测的作用|世界动作模型与未来预测的作用]]

## 原始摘要

Vision-Language-Action (VLA) models have emerged as a promising paradigm for robot learning, but their representations are still largely inherited from static image-text pretraining, leaving physical dynamics to be learned from comparatively limited action data. Generative video models, by contrast, encode rich spatiotemporal structure and implicit physics, making them a compelling foundation for robotic manipulation. But their potentials are not fully explored in the literature. To bridge the gap, we introduce DiT4DiT, an end-to-end Video-Action Model that couples a video Diffusion Transformer with an action Diffusion Transformer in a unified cascaded framework. Instead of relying on reconstructed future frames, DiT4DiT extracts intermediate denoising features from the video generation process and uses them as temporally grounded conditions for action prediction. We further propose a dual flow-matching objective with decoupled timesteps and noise scales for video prediction, hidden-state extraction, and action inference, enabling coherent joint training of both modules. Across simulation and real-world benchmarks, DiT4DiT achieves state-of-the-art results, reaching average success rates of 98.6% on LIBERO and 50.8% on RoboCasa GR1 while using substantially less training data. On the Unitree G1 robot, it also delivers superior real-world performance and strong zero-shot generalization. Importantly, DiT4DiT improves sample efficiency by over 10x and speeds up convergence by up to 7x, demonstrating that video generation can serve as an effective scaling proxy for robot policy learning. We release code and models at https://dit4dit.github.io/.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: https://dit4dit.github.io/

[在 Zotero 查看](zotero://select/library/items/DRJRFNYD)

Comment: https://dit4dit.github.io/

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/Q5RRWBWG)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/X3GK8ZMG)

[批注 99TQ7AKS · 第 6 页](zotero://open-pdf/library/items/X3GK8ZMG?annotation=99TQ7AKS&page=6)

> Dual Flow-Matching mechanism

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
