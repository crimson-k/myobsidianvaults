---
type: "literature-note"
title: "LongScape: Advancing Long-Horizon Embodied World Models with Context-Aware MoE"
aliases: ["LongScape: Advancing Long-Horizon Embodied World Models with Context-Aware MoE"]
zotero_keys: ["472MNJRH"]
year: 2025
authors: ["Yu Shang", "Lei Jin", "Yiding Ma", "Xin Zhang", "Chen Gao", "Wei Wu", "Yong Li"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2509.21790"
url: "http://arxiv.org/abs/2509.21790"
collections: ["04 World Models/Video-Based Interactive Simulation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# LongScape: Advancing Long-Horizon Embodied World Models with Context-Aware MoE

[Zotero 条目 472MNJRH](zotero://select/library/items/472MNJRH)

[DOI 原文](https://doi.org/10.48550/arxiv.2509.21790)

[来源网页](http://arxiv.org/abs/2509.21790)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

## 原始摘要

Video-based world models hold significant potential for generating high-quality embodied manipulation data. However, current video generation methods struggle to achieve stable long-horizon generation: classical diffusion-based approaches often suffer from temporal inconsistency and visual drift over multiple rollouts, while autoregressive methods tend to compromise on visual detail. To solve this, we introduce LongScape, a hybrid framework that adaptively combines intra-chunk diffusion denoising with inter-chunk autoregressive causal generation. Our core innovation is an action-guided, variable-length chunking mechanism that partitions video based on the semantic context of robotic actions. This ensures each chunk represents a complete, coherent action, enabling the model to flexibly generate diverse dynamics. We further introduce a Context-aware Mixture-of-Experts (CMoE) framework that adaptively activates specialized experts for each chunk during generation, guaranteeing high visual quality and seamless chunk transitions. Extensive experimental results demonstrate that our method achieves stable and consistent long-horizon generation over extended rollouts. Our code is available at: https://github.com/tsinghua-fib-lab/Longscape.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: 13 pages, 8 figures

[在 Zotero 查看](zotero://select/library/items/C6EXFUJU)

Comment: 13 pages, 8 figures

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/W5QWLZAA)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/UT3D44X2)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
