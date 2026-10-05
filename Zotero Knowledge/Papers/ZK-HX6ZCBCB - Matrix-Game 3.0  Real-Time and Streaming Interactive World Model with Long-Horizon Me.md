---
type: "literature-note"
title: "Matrix-Game 3.0: Real-Time and Streaming Interactive World Model with Long-Horizon Memory"
aliases: ["Matrix-Game 3.0: Real-Time and Streaming Interactive World Model with Long-Horizon Memory"]
zotero_keys: ["HX6ZCBCB"]
year: 2026
authors: ["Zile Wang", "Zexiang Liu", "Jiaxing Li", "Kaichen Huang", "Baixin Xu", "Fei Kang", "Mengyin An", "Peiyu Wang", "Biao Jiang", "Yichen Wei", "Yidan Xietian", "Jiangbo Pei", "Liang Hu", "Boyi Jiang", "Hua Xue", "Zidong Wang", "Haofeng Sun", "Wei Li", "Wanli Ouyang", "Xianglong He", "Yang Liu", "Yangguang Li", "Yahui Zhou"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2604.08995"
url: "http://arxiv.org/abs/2604.08995"
collections: ["04 World Models/Video-Based Interactive Simulation"]
source_tags: ["Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Matrix-Game 3.0: Real-Time and Streaming Interactive World Model with Long-Horizon Memory

[Zotero 条目 HX6ZCBCB](zotero://select/library/items/HX6ZCBCB)

[DOI 原文](https://doi.org/10.48550/arxiv.2604.08995)

[来源网页](http://arxiv.org/abs/2604.08995)

## 主题与知识联系

- [[Zotero Knowledge/Topics/04 World Models/Video-Based Interactive Simulation/索引|04 World Models/Video-Based Interactive Simulation]]

## 原始摘要

With the advancement of interactive video generation, diffusion models have increasingly demonstrated their potential as world models. However, existing approaches still struggle to simultaneously achieve memory-enabled long-term temporal consistency and high-resolution real-time generation, limiting their applicability in real-world scenarios. To address this, we present Matrix-Game 3.0, a memory-augmented interactive world model designed for 720p real-time longform video generation. Building upon Matrix-Game 2.0, we introduce systematic improvements across data, model, and inference. First, we develop an upgraded industrial-scale infinite data engine that integrates Unreal Engine-based synthetic data, large-scale automated collection from AAA games, and real-world video augmentation to produce high-quality Video-Pose-Action-Prompt quadruplet data at scale. Second, we propose a training framework for long-horizon consistency: by modeling prediction residuals and re-injecting imperfect generated frames during training, the base model learns self-correction; meanwhile, camera-aware memory retrieval and injection enable the base model to achieve long horizon spatiotemporal consistency. Third, we design a multi-segment autoregressive distillation strategy based on Distribution Matching Distillation (DMD), combined with model quantization and VAE decoder pruning, to achieve efficient real-time inference. Experimental results show that Matrix-Game 3.0 achieves up to 40 FPS real-time generation at 720p resolution with a 5B model, while maintaining stable memory consistency over minute-long sequences. Scaling up to a 2x14B model further improves generation quality, dynamics, and generalization. Our approach provides a practical pathway toward industrial-scale deployable world models.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Project page: https://matrix-game-v3.github.io/

[在 Zotero 查看](zotero://select/library/items/BL6LUQ2I)

Comment: Project page: https://matrix-game-v3.github.io/

## 附件与批注

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/Y5MKZJSR)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/9FV22N7U)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
