---
type: "literature-note"
title: "Astra: General Interactive World Model with Autoregressive Denoising"
aliases: ["Astra: General Interactive World Model with Autoregressive Denoising"]
zotero_keys: ["CMM8GA8N"]
year: 2026
authors: ["Yixuan Zhu", "Jiaqi Feng", "Wenzhao Zheng", "Yuan Gao", "Xin Tao", "Pengfei Wan", "Jie Zhou", "Jiwen Lu"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2512.08931"
url: "http://arxiv.org/abs/2512.08931"
collections: ["04 World Models/Video-Based Interactive Simulation"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition", "Computer Science - Machine Learning"]
tags: ["zotero", "literature", "concept/动作接口与逆动力学", "concept-primary/动作接口与逆动力学"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Astra: General Interactive World Model with Autoregressive Denoising

[Zotero 条目 CMM8GA8N](zotero://select/library/items/CMM8GA8N)

[DOI 原文](https://doi.org/10.48550/arxiv.2512.08931)

[来源网页](http://arxiv.org/abs/2512.08931)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

概念地图：[[Zotero Knowledge/Concepts/动作接口与逆动力学|动作接口与逆动力学]]

## 原始摘要

Recent advances in diffusion transformers have empowered video generation models to generate high-quality video clips from texts or images. However, world models with the ability to predict long-horizon futures from past observations and actions remain underexplored, especially for general-purpose scenarios and various forms of actions. To bridge this gap, we introduce Astra, an interactive general world model that generates real-world futures for diverse scenarios (e.g., autonomous driving, robot grasping) with precise action interactions (e.g., camera motion, robot action). We propose an autoregressive denoising architecture and use temporal causal attention to aggregate past observations and support streaming outputs. We use a noise-augmented history memory to avoid over-reliance on past frames to balance responsiveness with temporal coherence. For precise action control, we introduce an action-aware adapter that directly injects action signals into the denoising process. We further develop a mixture of action experts that dynamically route heterogeneous action modalities, enhancing versatility across diverse real-world tasks such as exploration, manipulation, and camera control. Astra achieves interactive, consistent, and general long-term video prediction and supports various forms of interactions. Experiments across multiple datasets demonstrate the improvements of Astra in fidelity, long-range prediction, and action alignment over existing state-of-the-art world models.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Accepted in ICLR 2026. Code is available at: https://github.com/EternalEvan/Astra

[在 Zotero 查看](zotero://select/library/items/QXKCHQP3)

Comment: Accepted in ICLR 2026. Code is available at: https://github.com/EternalEvan/Astra

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/2I7IP3NA)

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/PAIMDSSG)

[批注 H8CYBHRL · 第 1 页](zotero://open-pdf/library/items/PAIMDSSG?annotation=H8CYBHRL&page=1)

> owever, world models with the ability to predict long-horizon futures from past observations and actions remain underexplored, especially for general-purpose scenarios and various forms of actions.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
