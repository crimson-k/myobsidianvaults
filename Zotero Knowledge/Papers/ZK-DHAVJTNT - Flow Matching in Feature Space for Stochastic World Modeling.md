---
type: "literature-note"
title: "Flow Matching in Feature Space for Stochastic World Modeling"
aliases: ["Flow Matching in Feature Space for Stochastic World Modeling"]
zotero_keys: ["DHAVJTNT"]
year: 2026
authors: ["Francois Porcher", "Nicolas Carion", "Karteek Alahari", "Shizhe Chen"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2606.29059"
url: "https://arxiv.org/abs/2606.29059"
collections: ["04 World Models/Latent & Object-Centric Dynamics"]
source_tags: ["Artificial Intelligence (cs.AI)", "Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences"]
tags: ["zotero", "literature", "highlight"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Flow Matching in Feature Space for Stochastic World Modeling

[Zotero 条目 DHAVJTNT](zotero://select/library/items/DHAVJTNT)

[DOI 原文](https://doi.org/10.48550/arxiv.2606.29059)

[来源网页](https://arxiv.org/abs/2606.29059)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Latent & Object-Centric Dynamics/索引|04 World Models/Latent & Object-Centric Dynamics]]

概念地图：[[Zotero Knowledge/Concepts/表征学习与世界模型|表征学习与世界模型]]

## 原始摘要

World modeling requires forecasting uncertain futures while preserving information useful for
 downstream perception. Existing visual world models often struggle to satisfy both goals:
 VAE-based stochastic models operate in low-dimensional reconstruction latents, which can
 limit perception performance, while deterministic predictors using strong pretrained features
 collapse multimodal futures into a single blurry mean. In this work, we propose FlowWM, a
 stochastic world model that performs flow matching directly within pretrained feature space
 (e.g., DINOv3). This is challenging because pretrained features are substantially
 high-dimensional, making standard diffusion recipes suboptimal. To address this, we
 investigate the design choices needed for feature-space flow matching and introduce a
 differentiable one-step projection mechanism that enables efficient training with temporal
 consistency and task-driven objectives. We evaluate FlowWM on two benchmarks: a synthetic
 benchmark for systematic evaluation of accuracy and diversity, and a real-world benchmark
 FuturePerception. FlowWM improves perception performance, mode coverage, and horizon
 robustness, validating our proposed design for stochastic world modeling in high-dimensional
 feature spaces.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/8SRXD3KL)

## Other
24 pages, 18 figures, 6 tables

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/DS3ASEAD)

[批注 ENVLSI9G · 第 1 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=ENVLSI9G&page=1)

> FlowWM, a stochastic world model that performs flow matching directly within pretrained feature space

[批注 GXKYRBLD · 第 1 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=GXKYRBLD&page=1)

> VAE latents are optimized for pixel-wise reconstruction rather than geometry or semantics, and thus are inadequate for perception tasks that are critical for high-level planning such as object localization, detection, and tracking

[批注 FW95BVGC · 第 1 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=FW95BVGC&page=1)

> Deterministic predictors trained with standard regression losses tend to average over these possibilities, producing predictions that may correspond to no valid future

[批注 NRSC2EQI · 第 2 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=NRSC2EQI&page=2)

> FlowWM, a stochastic world model that leverages flow matching in high-dimensional feature spaces

[批注 U62AJYKZ · 第 2 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=U62AJYKZ&page=2)

> a differentiable one-step projection mechanism that supervises predicted future features without backpropagating through the full sampling trajectory.

[批注 VZ3R5F4G · 第 2 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=VZ3R5F4G&page=2)

> task-driven training via one-step projection.

[批注 YNJ62NQU · 第 3 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=YNJ62NQU&page=3)

> While this yields high visual fidelity, strong VAE bottlenecks discard fine-grained semantic structure, making the resulting representations poorly suited for dense perception and planning tasks

[批注 6CMTTXQN · 第 3 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=6CMTTXQN&page=3)

> ecent works incorporate task-driven objectives by backpropagating differentiable rewards through the diffusion inference process

[批注 276PQQ7W · 第 3 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=276PQQ7W&page=3)

> we use a one-step projection that applies downstream supervision at the endpoint, avoiding backpropagation through time while remaining stable and efficient.

[批注 X8CH2M8T · 第 3 页](zotero://open-pdf/library/items/DS3ASEAD?annotation=X8CH2M8T&page=3)

> Recent work has shown that diffusion models can operate directly in high-dimensional latent spaces

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
