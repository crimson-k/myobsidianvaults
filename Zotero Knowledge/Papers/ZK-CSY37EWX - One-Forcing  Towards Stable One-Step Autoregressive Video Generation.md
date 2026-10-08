---
type: "literature-note"
title: "One-Forcing: Towards Stable One-Step Autoregressive Video Generation"
aliases: ["One-Forcing: Towards Stable One-Step Autoregressive Video Generation"]
zotero_keys: ["CSY37EWX"]
year: 2026
authors: ["Jiaqi Feng", "Justin Cui", "Yuanhao Ban", "Cho-Jui Hsieh"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2605.23458"
url: "http://arxiv.org/abs/2605.23458"
collections: ["03 Visual Generation/General Video Generation"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature", "concept/视频生成的因果化与流式推理", "concept-primary/视频生成的因果化与流式推理"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# One-Forcing: Towards Stable One-Step Autoregressive Video Generation

[Zotero 条目 CSY37EWX](zotero://select/library/items/CSY37EWX)

[DOI 原文](https://doi.org/10.48550/arxiv.2605.23458)

[来源网页](http://arxiv.org/abs/2605.23458)

## 主题与知识联系

- [[Zotero Knowledge/Topics/03 Visual Generation/General Video Generation/索引|03 Visual Generation/General Video Generation]]

概念地图：[[Zotero Knowledge/Concepts/视频生成的因果化与流式推理|视频生成的因果化与流式推理]]

## 原始摘要

Recent advances have substantially improved real-time interactive video generation in the autoregressive regime. However, most existing few-step autoregressive video generation methods, often distilled from a corresponding many-step teacher, default to a 4-step sampling configuration, which still incurs considerable latency during deployment and suffers from severe quality degradation when the number of sampling steps is further reduced, particularly in the one-step setting. Trajectory-style consistency distillation methods often produce videos with weak dynamics, while DMD-based approaches, such as Self-Forcing, tend to yield blurry frames. To address this challenge, we propose One-Forcing, a simple yet effective approach which augments the DMD objective with an auxiliary GAN loss for high-quality and efficient one-step video generation. Experiments on VBench show that One-Forcing achieves a total score of 83.76, establishing state-of-the-art performance among one-step causal video generation methods and remaining competitive with strong many-step approaches. We further demonstrate that one-step framewise autoregressive generation can be achieved stably with merely one-third of the training cost of the chunkwise model, a setting that prior methods have failed to achieve successfully.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Comment: Work in Progress. Project Page: https://aurora-edu.github.io/one-forcing/, Code: https://github.com/Aurora-edu/

[在 Zotero 查看](zotero://select/library/items/Z8ZZVZ7L)

Comment: Work in Progress. Project Page: https://aurora-edu.github.io/one-forcing/, Code: https://github.com/Aurora-edu/One-Forcing

## 附件与批注

### Full Text PDF

[打开 PDF](zotero://open-pdf/library/items/K7UKZPRW)

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/WNIAXQ49)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]
