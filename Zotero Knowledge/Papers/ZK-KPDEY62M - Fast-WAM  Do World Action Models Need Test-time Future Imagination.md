---
type: "literature-note"
title: "Fast-WAM: Do World Action Models Need Test-time Future Imagination?"
aliases: ["Fast-WAM: Do World Action Models Need Test-time Future Imagination?"]
zotero_keys: ["KPDEY62M"]
year: 2026
authors: ["Tianyuan Yuan", "Zibin Dong", "Yicheng Liu", "Hang Zhao"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/arXiv.2603.16666"
url: "http://arxiv.org/abs/2603.16666"
collections: ["05 Robot Learning/World-Action Models"]
source_tags: ["Computer Science - Artificial Intelligence", "Computer Science - Computer Vision and Pattern Recognition"]
tags: ["zotero", "literature", "concept/世界动作模型与未来预测的作用", "concept-primary/世界动作模型与未来预测的作用"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Fast-WAM: Do World Action Models Need Test-time Future Imagination?

[Zotero 条目 KPDEY62M](zotero://select/library/items/KPDEY62M)

[DOI 原文](https://doi.org/10.48550/arxiv.2603.16666)

[来源网页](http://arxiv.org/abs/2603.16666)

## 主题与知识联系

- [[Zotero Knowledge/Topics/05 Robot Learning/World-Action Models/索引|05 Robot Learning/World-Action Models]]

概念地图：[[Zotero Knowledge/Concepts/世界动作模型与未来预测的作用|世界动作模型与未来预测的作用]]

## 原始摘要

World Action Models (WAMs) have emerged as a promising alternative to Vision-Language-Action (VLA) models for embodied control because they explicitly model how visual observations may evolve under action. Most existing WAMs follow an imagine-then-execute paradigm, incurring substantial test-time latency from iterative video denoising, yet it remains unclear whether explicit future imagination is actually necessary for strong action performance. In this paper, we ask whether WAMs need explicit future imagination at test time, or whether their benefit comes primarily from video modeling during training. We disentangle the role of video modeling during training from explicit future generation during inference by proposing \textbf{Fast-WAM}, a WAM architecture that retains video co-training during training but skips future prediction at test time. We further instantiate several Fast-WAM variants to enable a controlled comparison of these two factors. Across these variants, we find that Fast-WAM remains competitive with imagine-then-execute variants, while removing video co-training causes a much larger performance drop. Empirically, Fast-WAM achieves competitive results with state-of-the-art methods both on simulation benchmarks (LIBERO and RoboTwin) and real-world tasks, without embodied pretraining. It runs in real time with 190ms latency, over 4$\times$ faster than existing imagine-then-execute WAMs. These results suggest that the main value of video prediction in WAMs may lie in improving world representations during training rather than generating future observations at test time. Project page: https://yuantianyuan01.github.io/FastWAM/

## 附件与批注

### Snapshot

[在 Zotero 查看附件](zotero://select/library/items/BTB4MS97)

### Preprint PDF

[打开 PDF](zotero://open-pdf/library/items/ZCV8J2ZZ)

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-YHITUAUN - GaussianDream  A Feed-Forward 3D Gaussian World Model for Robotic Manipulation|GaussianDream: A Feed-Forward 3D Gaussian World Model for Robotic Manipulation]] — 强关联；均保留训练期未来建模的收益，并省去推理期显式未来预测。
- [[Zotero Knowledge/Papers/ZK-MUJ47Y8T - DiT4DiT  Jointly Modeling Video Dynamics and Actions for Generalizable Robot Control|DiT4DiT: Jointly Modeling Video Dynamics and Actions for Generalizable Robot Control]] — 强关联；比较视频建模与动作生成的耦合方式，以及是否需要显式重建未来帧。
- [[Zotero Knowledge/Papers/ZK-X3ILM5TW - Making Foresight Actionable  Repurposing Representation Alignment in World Action Mod|Making Foresight Actionable: Repurposing Representation Alignment in World Action Models]] — 强关联；共同追问可生成未来的表征如何转化为有效动作；比较训练监督与动作接口。

<!-- content-relations:end -->
