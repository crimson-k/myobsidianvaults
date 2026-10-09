---
type: "literature-note"
title: "Representation Alignment for Generation: Training Diffusion Transformers Is Easier Than You Think"
aliases: ["Representation Alignment for Generation: Training Diffusion Transformers Is Easier Than You Think"]
zotero_keys: ["AWA338G8"]
year: 2024
authors: ["Sihyun Yu", "Sangkyung Kwak", "Huiwon Jang", "Jongheon Jeong", "Jonathan Huang", "Jinwoo Shin", "Saining Xie"]
venue: "arXiv"
venue_field: "repository"
doi: "10.48550/ARXIV.2410.06940"
url: "https://arxiv.org/abs/2410.06940"
collections: ["06 Alignment & Reliability/Representation Alignment"]
source_tags: ["Computer Vision and Pattern Recognition (cs.CV)", "FOS: Computer and information sciences", "Machine Learning (cs.LG)"]
tags: ["zotero", "literature", "concept/物理一致性与表征对齐", "concept-primary/物理一致性与表征对齐"]
reading_status: "unreviewed-import"
imported_at: "2026-10-02T23:59:30+08:00"
---

# Representation Alignment for Generation: Training Diffusion Transformers Is Easier Than You Think

[Zotero 条目 AWA338G8](zotero://select/library/items/AWA338G8)

[DOI 原文](https://doi.org/10.48550/arxiv.2410.06940)

[来源网页](https://arxiv.org/abs/2410.06940)

## 主题与知识联系

- [[Zotero Knowledge/Topics/06 Alignment & Reliability/Representation Alignment/索引|06 Alignment & Reliability/Representation Alignment]]

概念地图：[[Zotero Knowledge/Concepts/物理一致性与表征对齐|物理一致性与表征对齐]]

补充阅读入口：[[Zotero Knowledge/Topics/01 Foundations/索引|01 Foundations]]

## 原始摘要

Recent studies have shown that the denoising process in (generative) diffusion models can induce meaningful (discriminative) representations inside the model, though the quality of these representations still lags behind those learned through recent self-supervised learning methods. We argue that one main bottleneck in training large-scale diffusion models for generation lies in effectively learning these representations. Moreover, training can be made easier by incorporating high-quality external visual representations, rather than relying solely on the diffusion models to learn them independently. We study this by introducing a straightforward regularization called REPresentation Alignment (REPA), which aligns the projections of noisy input hidden states in denoising networks with clean image representations obtained from external, pretrained visual encoders. The results are striking: our simple strategy yields significant improvements in both training efficiency and generation quality when applied to popular diffusion and flow-based transformers, such as DiTs and SiTs. For instance, our method can speed up SiT training by over 17.5×, matching the performance (without classifier-free guidance) of a SiT-XL model trained for 7M steps in less than 400K steps. In terms of final generation quality, our approach achieves state-of-the-art results of FID=1.42 using classifier-free guidance with the guidance interval.

## Zotero 已有笔记

> 以下为原库笔记的导入内容，可能含既有机器生成分析；保留来源，不作为本次核读结论。

### Other

[在 Zotero 查看](zotero://select/library/items/WJMFXJT9)

## Other
ICLR 2025 (Oral). Project page: https://sihyun.me/REPA

## 附件与批注

### PDF

[打开 PDF](zotero://open-pdf/library/items/NSB5VYKQ)

[批注 XYPZYCN7 · 第 3 页](zotero://open-pdf/library/items/NSB5VYKQ?annotation=XYPZYCN7&page=3)

> distills the pretrained self-supervised visual representation y∗ of a clean image x into the diffusion transformer representation h of a noisy input x ̃.

## 我的阅读与思考

<!-- 自己的研究问题、方法比较、复现结果和引用计划写在这里。导入区是一次性快照。 -->

[[Zotero Knowledge/知识库首页|返回知识库首页]]

<!-- content-relations:start -->
## 相关文献：基于内容的关联

> 以下为标题、摘要及现有笔记推断的阅读关联，不代表已核实的引用或方法依赖。相关性分数仅用于库内排序。

- [[Zotero Knowledge/Papers/ZK-7TDQKU5X - VideoREPA  Learning Physics for Video Generation through Relational Alignment with Fo|VideoREPA: Learning Physics for Video Generation through Relational Alignment with Foundation Models]] — 强关联；对方摘要提到模型 REPA（仅确认名称提及）。
- [[Zotero Knowledge/Papers/ZK-VAQCDKF8 - MoAlign  Motion-Centric Representation Alignment for Video Diffusion Models|MoAlign: Motion-Centric Representation Alignment for Video Diffusion Models]] — 强关联；比较生成模型的外部表征监督与视频运动专属对齐。

<!-- content-relations:end -->
